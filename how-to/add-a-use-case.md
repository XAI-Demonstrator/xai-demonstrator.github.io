# 🔧 How to Add a Use Case

The _XAI Demonstrator_ is a collection of fully independent use cases.
Each use case aims to illustrate a particular application of XAI methods.

In this document, we show how to add a custom use case to the XAI Demonstrator.
In the process, we discuss some of our fundamental design considerations and give an overview of the architecture. 

## What is a "use case"?

On a technical level, each use case comprises a user interface (frontend) and a stateless microservice (backend).

The frontend is a single-page web application (SPA) that the users interact with on their smartphone.
While the frontend is arguably the component most challenging to design, from a technical perspective, it's a fairly standard and lightweight web app.

The backend, on the other hand, is where the AI predictions and corresponding explanations are generated.
(Throughout this guide, we will assume that "the AI" is some sort of machine-learning model. 
In line with most common machine-learning frameworks, we will refer to all model outputs "predictions".)
The backend provides an HTTP-API that the frontend calls to request and receive predictions and explanations.

> 🔎 **A note on code organization**
>
> The entire code for the _XAI Demonstrator_ lives in one single Git repository, a so-called monorepo.
> Hence, you can just clone [the repository](https://www.github.com/xai-demonstrator/xai-demonstrator) and are good to go.
> 
> Compared to the perhaps more traditional approach of keeping each use case in a separate repository, a monorepo might at first seem daunting and overly complex.
> However, especially when working with a team of varying levels of experience (like [ours](/#Team)), you will probably soon see how convenient it is to keep all the code in one place.
> Everyone can immediately see where changes have been made and how the entire system eventually comes together.
> 
> It is also straightforward to deploy the _XAI Demonstrator_ to your local machine or some cloud infrastructure.
> Indeed, all the required scripts and configuration files live in the monorepo as well, there is no behind-the-scenes magic.
> 
> - `.github/workflows/` GitHub Actions workflows for automated testing and deployment
> - `deployment/` Deployment configurations
> - `landing-page/` A service that provides a common landing page for multiple use cases

Why Docker?

## Adding a use case

Each use case is entirely self-contained and resides in its own top-level directory.
All _XAI Demonstrator_ use cases adhere to this basic structure and naming convention:
```python
use-case/
|
|- case-backend/  # (1)
|  |- case/
|  |  |- __init__.py
|  |  |- main.py
|  |
|  |- requirements.txt
|      
|- case-frontend/  # (2)
|  |- src/
|  |  |- App.vue
|  |
|  |- package.json
|     
|- Dockerfile  # (3)
|- README.md
```
The most important elements, which we will instantiate in the following, are:
1. A microservice built with FastAPI (the backend).
2. A VueJS single-page application (the frontend).
3. A Dockerfile that describes how to assemble backend and frontend into a single container.

> 💡 **A note on the tech stack**
> 
> In principle, you can choose whatever programming language and framework you like.
> As long as you provide a Docker container with an HTTP API, you're good to go.

### Create the backend microservice

We use FastAPI.

```bash
cd case-backend/
uvicorn case.main:app
```

You can access it at http://localhost:8000.

> 💡 **A use case backend should be stateless**
> 
> All _XAI Demonstrator_ backends are stateless.
> Each call to their API is self-contained, i.e., no information is stored within the backend.
> 
> This allows us to run multiple instances of the backends in parallel and distribute the frontends' calls among them.
> In particular, it enables us to deploy the XAI demonstrator to a serverless infrastructure.
> 
> We strongly recommend that you design your backends to be stateless as well.

### Create the frontend

We use VueJS.

```bash
cd use-case
vue-cli case-frontend
```

This generates the basic structure.
You can immediately test that everything was set up correctly:
```bash
cd case-frontend/
npm run
```
You can access it at http://localhost:8080.

> ⚠ **Serving the frontend**
> 
> To be able to operate a use case 

### Assemble the use case

Creating a 
All of this can be described in a single _Dockerfile_, which :

```dockerfile
# FIRST STAGE
FROM node:12-alpine as builder
WORKDIR /

# Copy the frontend code into the container
COPY ./case-frontend/ .

# Install frontend dependencies and build the frontend
RUN npm install && npm run build


# SECOND STAGE
FROM python:3.8-slim
WORKDIR /

# Copy the backend code
COPY case-backend/case /case

# Install all Python dependencies
COPY case-backend/requirements.txt /requirements.txt
RUN pip install --upgrade pip
RUN pip install -r /requirements.txt \
    && rm -rf /root/.cache/pip

# Copy the frontend from the first stage
RUN mkdir /case/static
COPY --from=builder /dist/ /case/static/

# Launch backend service
CMD ["uvicorn", "case.main:app", "--host", "0.0.0.0", "--port", "8000"]
```

With this Docker file, the use case can be built and started:
```bash
cd use-case
docker run
````

### Optional: Configure GitHub Actions

### Optional: Add use case to XAI Demonstrator instance 
