# Entdecke nutzerzentrierte Erklärbare KI

Der **XAI-Demonstrator** ist eine modulare Plattform, auf der AnwenderInnen live mit XAI-Systemen interagieren können.

**Interesse? Besuche den XAI-Demonstrator: [xaidemo.de](https://www.xaidemo.de)!**

## Was ist Erklärbare KI?

Die Motivation für Explainable Artificial Intelligence (XAI) ist im **Black-Box-Charakter** von Künstlicher Intelligenz (KI) begründet. Die Komplexität von KI-basierten Systemen führt in vielen Fällen dazu, dass algorithmische Entscheidungen aus Sicht des Menschen nicht mehr nachvollzogen und validiert werden können. XAI setzt an diesem Punkt an. Ziel von XAI ist es, automatisiert **für Menschen verständliche Erklärungen und Hilfestellungen** zu generieren, welche die von KI im Einzelfall getroffenen Empfehlungen für die AnwenderInnen nachvollziehbar machen. XAI-Methoden sind zahlreich: Sie können beispielsweise für bestimmte KI-Systeme zugeschnitten sein oder für beliebige KI-Systeme einsetzbar. Sie versorgen AnwenderInnen von KI-Systemen oder Betroffene von KI-Entscheidungen beispielsweise mit Visualisierungen, legen die Funktionsweise der KI offen oder verdeutlichen die Entscheidungsfindung der KI anhand von Gegenbeispielen. Manche XAI-Methoden bilden die gesamte Funktionsweise der KI ab, andere beschränken sich auf Teilbereiche. 

**Ziel von XAI** ist es, AnwenderInnen von KI den Umgang zu erleichtern und Betroffenen von KI-Entscheidungen Nachvollziehbarkeit zu ermöglichen. AnwenderInnen von KI-Systemen können mithilfe von Erklärungen die von KI getroffenen Entscheidungen hinterfragen oder auch widersprechen. Sie können Fehlfunktionen von KI aufdecken. Sie lernen, wann sie der KI vertrauen können und wann nicht. 

XAI hat das Potential, die **Akzeptanz bestehender und neuer KI-Anwendungen zu steigern**. XAI kann der Hebel sein für einen wertstiftenden Einsatz von KI gemäß den Wertvorstellungen einer **menschenzentrierten KI**. 

## Was und für wen ist der XAI-Demonstrator?
Ziel des XAI-Demonstrators ist es, die **Potentiale und Grenzen von XAI erlebbar** zu machen. NutzerInnen des XAI-Demonstrators erfahren die Methoden und Konzepte **aktueller XAI-Forschung** anhand von **leicht zugänglichen Use Cases**. Dabei kommunizieren sie live mit einer echten KI können Erklärungen dazu anfragen.

Zielgruppen des XAI-Demonstrators:

*Unternehmen, Politik und Verwaltung* – erfahren selbst anhand von in der Praxis typischen und relevanten KI-Anwendungsbeispielen, welchen Mehrwert und welche Grenzen XAI für ihre eigene Institution hat. Die dem XAI-Demonstrator zugrundeliegende Implementierung illustriert, wie XAI-Methoden im laufenden Betrieb eingesetzt werden können.

*Studierende* – lernen mit dem XAI-Demonstrator als Tool zum Selbstausprobieren die Konzepte und Methoden von XAI spielerisch kennenzulernen. Die vorhanden technische Struktur erlaubt es Studierenden, auch im begrenzten Rahmen einer Abschlussarbeit selbst XAI-Methoden lauffähig zu implementieren.

*Die breite Öffentlichkeit* – erkundet im gesellschaftlichen Diskurs die Potenziale und Grenzen von XAI auf dem Weg zu einem selbstbestimmten und verantwortungsvollen Umgang mit KI.

*Forschende* – nutzen den XAI-Demonstrator, um neue XAI-Methoden an einfachen Schnittstellen in einen bestehenden Use Case einzubinden, eigene Use Cases zu implementieren oder Nutzerbefragungen durchzuführen. Die technische Dokumentation ([xai-demonstrator.github.io](https://xai-demonstrator.github.io/xai-demonstrator/)) und Implementierung ([github.com/XAI-Demonstrator](https://github.com/XAI-Demonstrator/xai-demonstrator)) ist Open-Source verfügbar.


## Use Case I
In diesem Use Case interagieren AnwenderInnen mit einer KI, die anhand eines **Bewertungstextes** (z. B. Produktreview) die **Stimmung** des Bewertungstextes (Sentiment) vorhersagt.

### Praxisrelevanz
**Textklassifikation** als die dem Use Case zugrundeliegende KI-Anwendung ist in der Praxis bereits seit Jahren etabliert und gewinnt durch das exponentielle Wachstum der Menge an digital verfügbaren Texten zunehmend an Relevanz. 

Textklassifikation wird beispielsweise in folgenden **Bereichen des Alltags und der Wirtschaft** eingesetzt:

*Sentimentanalyse*, bspw. im Kundenservice

*Topic Detection*, bspw. zur Strukturierung von Dokumenten in Due Dilligence Verfahren / Erstellung von Tags zu Filmen oder Forenbeiträgen

*Offensive Language Detection*, bspw. zur Einhaltung von Guidelines auf Social Media Plattformen 

*Wissensexploration*, bspw. in Suchmaschinen zur automatisierten Markierung besonders relevanter Dokumente oder Textabschnitte

XAI ermöglicht in diesem Kontext KI-AnwenderInnen und Betroffenen, mithilfe der Erklärungen selbstbestimmt und informiert die **Entscheidungen der KI zu hinterfragen** und beispielsweise auch zu widersprechen. Übergeordnetes Ziel ist, dass Mensch und Maschine **gemeinsam eine bessere Entscheidung treffen** können als Mensch oder Maschine allein imstande wären.

### User Flow

In diesem Use Case erfahren User den Mehrwert und die Grenzen von für Textklassifikation typische Erklärbarkeit. Der User Flow setzt sich im Wesentlichen aus den Schritten „Bewertung verfassen“, „Klassifizierung erhalten“ und „Erklärung anfordern“ zusammen.

**„Bewertung verfassen“:** Der User gibt einen eigenen Bewertungstext ein. Als Anregung sieht der User eine Einstiegsfrage nach einem eigenen Kundenerlebnis (z. B. Restaurantbesuch, Film, Reise). Um den Zugang niederschwellig zu gestalten, wird zudem ein thematisch passender vorgefertigter Bewertungstext angezeigt. 

**„Klassifizierung erhalten“:** Der User fordert durch einen Klick (im Webbrowser mit der Maus, am Smartphone mit dem Finger) auf den Button *„Wie viel Sterne sollte meine Bewertung erhalten?“* eine Sentiment-Klassifikation des Bewertungstextes durch die KI an. Durch einen angezeigten Ladekreis wird dem User auch visuell deutlich gemacht, dass er live mit einer echten KI kommuniziert. Sobald die Berechnung abgeschlossen ist (in der Regel innerhalb eines Bruch-teils einer Sekunde), sieht der User die entsprechende Klassifikation des Bewertungstextes in Form von Sternen (1-5 *Sterne*, 1 *Stern* ≙ sehr negative Stimmung, 5 *Sterne* ≙ sehr positive Stimmung). 

**„Erklärung anfordern“:** Der User fordert durch einen Klick (im Webbrowser mit der Maus, am Smartphone mit dem Finger) auf den Button *„Wie kommst du zu dieser Einschätzung?“* eine Er-klärung zu der aktuell angezeigten Sentiment-Klassifikation des Bewertungstextes der KI an. Solange die XAI die Erklärung zur Vorhersage der Klassifikation des Bewertungstextes berechnet, wird dem User ein Ladekreis angezeigt. Sobald die Berechnung abgeschlossen ist (meist innerhalb weniger Sekunden), sieht der User zur Erklärung die für die Klassifikation des Bewertungstextes durch die KI zentralen Wörter nach Wichtigkeit und Sentiment als Balkendiagramm aufgelistet sowie zusätzlich im originalen Bewertungstext markiert. 

Der User Flow kann beliebig oft wiederholt werden. Die Schritte „Klassifizierung erhalten“ und „Erklärung anfordern“ werden typischerweise vom User hintereinander ausgeführt. Zusätzlich kann der User aber auch den Schritt „Klassifizierung erhalten“ beliebig oft wiederholen. Ein Refresh-Button am rechten oberen Rand lässt den User jederzeit zum Startbildschirm des Use Cases zurückkehren und erneut mit dem Schritt „Bewertung verfassen“ beginnen. Ein Zurück-Button lässt den User jederzeit zum Startbildschirm des XAI-Demonstrators zurückkehren. 

### KI
Das der Textklassifikation zugrundeliegende KI-Modell baut auf dem von Google entwickelten **BERT-Modell** (**B**idirectional **E**ncoder **R**epresentations from **T**ransformers) auf und stellt ein State-of-the-Art KI-Modell im Kontext von Natural Language Processing (NLP) dar. Das verwendete, auf Basis von über 500.000 Bewertungen in verschiedenen Sprachen trainierte Modell ordnet einen gegebenen Text in eine der fünf Klassen „1 *Stern*“, „2 *Sterne*“,…, „5 *Sterne*“ ein, die das Sentiment des Textes repräsentieren. 

### XAI
Die Erklärungen werden mithilfe der XAI-Methode **SHAP** (**SH**apley **A**dditive ex**P**lanations) erzeugt. Diese stellt eine der vielversprechendsten Methoden zur Erklärung der Entscheidung von KI-Anwendungen zur Textklassifikation dar. Bei der Textklassifikation entspricht die Erklärung dieser XAI-Methode einer **Visualisierung der für die Klassifizierung relevantesten Wörter und deren Einfluss auf die Klassifizierung**. 

Die Grundidee von SHAP ist es, die aus der Spieltheorie bekannten Shapley-Werte für alle Wörter eines Textes zu approximieren. Der verwendete Ansatz erreicht dies für einen gegebenen Datenpunkt durch Berechnung der Gradienten des Modells zu mehreren leicht veränderten zufällig gewählten Datenpunkten (z. B. Texte, die gegenüber dem Bewertungstext nur wenige veränderte Wörter aufweisen).

## Use Case II
In diesem Use Case interagieren AnwenderInnen mit einer KI, die den Gegenstand innerhalb eines Bildausschnitts erkennen kann. 

### Praxisrelevanz
**Bildklassifikation** als die dem Use Case zugrundeliegende KI-Anwendung ist in der Praxis weit verbreitet und hat über das vergangene Jahrzehnt substanzielle Fortschritte durch Weiterentwicklungen im Bereich künstlicher neuronaler Netze erreicht. 

Bildklassifikation wird beispielsweise in folgenden **Bereichen des Alltags und der Wirtschaft** eingesetzt: 

*Objekterkennung*, bspw. beim autonomen Fahren

*Gesichtserkennung*, bspw. zur Identifikation von Personen auf Fotos in Social Media

*Diagnostik in der Medizin*, bspw. zur Diagnose anhand von Röntgenbildern 

*Qualitätssicherung*, bspw. zur Identifikation fehlerhafter Ware

*Digital Commerce*, bspw. zur Suche und Empfehlung von Produkten

Einige dieser Anwendungen, insbesondere in für Menschen **kritischen Bereichen** wie der Medizin oder dem Verkehr, erfordern ein hohes Maß an **Rechenschaftspflicht und Transparenz**. Erklärungen für die algorithmischen Vorhersagen haben zum Ziel, dass AnwenderInnen einer KI ein ausreichendes **Verständnis über das Verhalten des Systems** aufbauen sowie dessen Zuverlässigkeit hinterfragen und rechtfertigen können. 

### User Flow
In diesem Use Case erfahren User den Mehrwert und die Grenzen von für Bildklassifikation typische Erklärbarkeit. Der User Flow setzt sich im Wesentlichen aus einem Startbildschirm und den Schritten „Bildausschnitt wählen“ und „Erklärung anfordern“ zusammen. 

**Startbildschirm:** Der User sieht ein Foto und erkennt intuitiv Gegenstände auf diesem Foto. Ein vordefinierter Bildausschnitt ist vorausgewählt und für diesen Bildausschnitt wird dem User die Klassifikation des enthaltenen Gegenstands der KI angezeigt.

**„Bildausschnitt wählen“:** Der User verändert die Größe des Bildausschnitts oder verschiebt den Bildausschnitt auf eine beliebige Position innerhalb des Bildes (im Webbrowser mit der Maus, am Smartphone mit dem Finger). Sollte für einen Bildausschnitt bereits eine Erklärung erzeugt worden sein, so verschwindet diese zum Zeitpunkt, wenn der User den Bildausschnitt verändert. Sobald der Bildausschnitt steht, sieht der User Ladepunkte an Stelle der Vorhersage der KI, solange die KI die Vorhersage für diesen Bildausschnitt berechnet. Durch die angezeigten Ladepunkte wird dem User auch visuell deutlich gemacht, dass er live mit einer echten KI kommuniziert. Sobald die Berechnung abgeschlossen ist (meist innerhalb eines Bruchteils einer Sekunde), sieht der User die entsprechende Vorhersage der KI für seinen gewählten Bildausschnitt. 

**„Erklärung anfordern“:** Der User fordert durch Klick (im Webbrowser mit der Maus, am Smartphone mit dem Finger) auf den Button *„Woran erkennst du das?“* eine Erklärung zu der aktuell angezeigten Vorhersage der KI an. Nach dem Klick sieht der User Ladepunkte an Stelle des Buttons, solange die XAI die Erklärung zur Vorhersage für den aktuellen Bildausschnitt berechnet. Sobald die Berechnung abgeschlossen ist (meist innerhalb weniger Sekunden), sieht der User zur Erklärung des aktuellen Bildausschnitts die für die Vorhersage der KI zentralen Bildabschnitte markiert. 

Der User Flow kann beliebig oft wiederholt werden. Die Schritte „Bildausschnitt wählen“ und „Erklärung anfordern“ werden typischerweise vom User hintereinander ausgeführt. Zusätzlich kann der User aber auch den Schritt „Bildausschnitt wählen“ beliebig oft wiederholen. Ein Refresh-Button am rechten oberen Rand lässt den User jederzeit zum Startbildschirm des Use Cases zurückkehren. Ein Zurück-Button lässt den User jederzeit zum Startbildschirm des XAI-Demonstrators zurückkehren. 

### KI
Das der Vorhersage zugrundeliegende KI-Modell ist ein **neuronales Netz** in ResNet-Architektur. Das neuronale Netz für die Identifikation von Gegenständen klassifiziert einen gegebenen Bildausschnitt in eine der Klassen, Gegenstände repräsentieren.

### XAI
Die Erklärungen werden mit der XAI-Methode **LIME** (**L**ocal **I**nterpretable **M**odelagnostic **E**xplanations) generiert. Bei der Bildklassifikation entspricht die Erklärung dieser XAI-Methode einer **graphischen Hervorhebung von Bildbereichen**, die für die konkrete Klassifizierung besonders relevant sind. 

Die Grundidee von LIME ist es, ein lineares und damit leicht interpretierbares Modell zu finden, das sich bei der Klassifikation der zu erklärenden Instanz sowie nahegelegene Instanzen ähnlich verhält wie das KI-Modell. Im Falle der Bildklassifikation ist die zu erklärende Instanz das Bild und nahegelegene Instanzen beispielsweise Bilder, bei denen demgegenüber nur wenige Pixel verändert sind. Mithilfe des leicht interpretierbaren Modells werden für die Bildklassifikation Bildbereiche identifiziert, die für die Klassifizierung besonders relevant sind. LIME ist modellagnostisch und daher nicht auf die Anwendung auf bestimmte KI-Modelle beschränkt.

## Weiterführende Links

**Zum XAI-Demonstrator: [xaidemo.de](https://www.xaidemo.de)**

**Zur Forschungsgruppe: [uni-ulm.de/IBA/XAI](https://www.uni-ulm.de/mawi/iba/forschung/forschungsthemen/explainable-artificial-intelligence/)**

**Zur technischen Beschreibung: [xai-demonstrator.github.io](https://xai-demonstrator.github.io/xai-demonstrator/)**
 
**Zum Github-Repository: [github.com/XAI-Demonstrator](https://github.com/XAI-Demonstrator/xai-demonstrator)**


