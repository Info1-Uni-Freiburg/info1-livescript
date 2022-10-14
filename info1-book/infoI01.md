# 1. Grundlagen
## Inhalt der Vorlesung
Wir vermitteln in dieser Vorlesung Grundkenntnisse und Grundfähigkeiten in
den Bereichen

- Programmierung (Python):  
  Grundkenntnisse der Programmierung
- Modellierung  
  Wie modelliere ich ein Problem bevor ich es in ein Programm umsetze?
- Programmentwicklung  
  Techniken zu Programmentwicklung, z.B. Testen
- Analyse
- Grundlagen (Berechnungsmodelle, Programmiersprachenparadigmen,
  ...)  

- **Denken wie ein Informatiker/eine Informatikerin**  
  Grundsätzliches Ziel der Vorlesung

## Was ist Informatik?
### Versuch der Definition 
````{admonition} **Informatik-Duden:** 
:class: definition 
Wissenschaft von der systematischen Verarbeitung von Informationen, besonders der automatischen Verarbeitung mit Hilfe von Digitalrechnern (Computern).
````

````{admonition} **Gesellschaft für Informatik**  
Das Wort **Informatik** setzt sich aus den Wörtern **Information** und
**Automatik** zusammen und bezeichnet die Wissenschaft von der
systematischen Verarbeitung von Informationen mit Hilfe von
Rechenanlagen.
````



Aber:

>Computer science is no more about computers than astronomy is about telescopes! (Dijkstra)

````{admonition} **Association of Computing Machinery**  
Computer science and engineering is the systematic study of algorithmic processes---their theory, analysis, design, efficiency, implementation, and application---that describe and transform information. The fundamental question underlying all of computing is: What can be (efficiently) automated?
````

Auch hier wird wieder der Begriff "systematisch" eingebracht.


Die entscheidende Frage hinter all diesen Definitionen ist:  
  **Was kann man tatsächlich automatisieren?**



### Einordnung
Die Einordnung der Informatik als Wissenschaft fällt schwer, da sie unter verschiedene Kategorien fällt.

- Informatik beschäftigt sich mit der Analyse von Strukturen und ist insofern eine 
**Strukturwissenschaft**
- verwandt mit der Mathematik; verwendet die Sprache der Mathematik

- Informatik beschäftig sich mit dem Design von Artefakten und ist insofern eine 
**Ingenieurwissenschaft**

Hinter allen Definitionen steckt die systematische Herangehensweise.

### Teilgebiete (frei nach der GI)
````{glossary}
Theoretische Informatik
  Die Theoretische Informatik erforscht und entwickelt Konzepte zur
  Darstellung von Geräten und Prozessen als formal logische Systeme;
  damit ist sie die Grundlage für die Programmierung. 
  Die theoretische Informatik befasst sich insbesondere mit der Geschwindigkeit und dem Speicherverbrauch solcher Algorithmen.
  - Was ist überhaupt **berechenbar**?
  - P = NP?

Praktische Informatik
  Die Praktische Informatik entwickelt grundlegende Lösungskonzepte für die wichtigsten Anwendungsbereiche der Informatik. Sie beschäftigt sich besonders mit der Entwicklung von Computerprogrammen mit Hilfe spezieller Programmiersprachen und deren Nutzung in großen Softwaresystemen. Damit beeinhaltet sie z.B. Softwaretechnik.

  nötig? -> tolles Bild!
  ```{image} ./pics/eclipse.jpg
  :alt: eclipse
  :class: bg-primary mb-1
  :width: 500px
  :align: center
  ```

Technische Informatik
  ```{image} ./pics/pyboard.jpg
  :alt: pyboard
  :class: bg-primary mb-1
  :width: 150px
  :align: right
  ```
  Jedes Computersystem besteht aus drei funktional voneinander
  getrennten Einheiten: Dateneingabe, Datenbearbeitung und
  Datenausgabe. Die Entwicklung der hierfür erforderlichen Hardware ist der Kernbereich der Technischen Informatik.

Angewandte Informatik
  ```{image} ./pics/pr2.jpg
  :alt: pr2
  :class: bg-primary mb-1
  :width: 100px
  :align: right
  ```
  Die Angewandte Informatik untersucht, inwieweit Abläufe durch den Einsatz von Computern automatisiert werden können. Verfahren der Simulation und Computergraphik, der Bild- und Sprachverarbeitung sowie der Modellierung schaffen konkrete Anwendungsmöglichkeiten für die Automatisierung.

Informatik und Gesellschaft
  ```{image} ./pics/social.png
  :alt: social
  :class: bg-primary mb-1
  :width: 200px
  :align: right
  ```
  Der Bereich Informatik und Gesellschaft umfasst Soziologie, Philosophie, Jura und Politologie und ermöglicht eine umfassende Technikfolgenabschätzung für Computeranwendungen in der modernen Gesellschaft. Themen sind etwa Datenschutz, Softwarepatente, gesellschaftliche Bewegungen wie Open Source und ihr Verhältnis zum Urheberrecht.


  ```{image} ./pics/logoGI.png
  :alt: logogi
  :class: bg-primary mb-1
  :width: 50px
  :align: right
  ```
    **Exkurs: GI**  
    Die *Gesellschaft für Informatik e.V. (GI)* ist die größte
    Vereinigung von Informatikerinnen und Informatikern im
    deutschsprachigen Raum. Sie versteht sich als Plattform für
    Informatikfachleute aus Wissenschaft und Wirtschaft, Lehre und
    Öffentlicher Verwaltung und versammelt eine geballte Konzentration
    an Wissen, Innovation und Visionen. Rund 20.000 persönliche
    Mitglieder, darunter 1.500 Studierende und knapp 300 Unternehmen und
    Institutionen, profitieren von unserem Netzwerk.  
    **Mitgliedschaft**
    Kostenlos für Studenten!


  ```{image} ./pics/logoACM.png
  :alt: logo
  :class: bg-primary mb-1
  :width: 50px
  :align: right
  ```
    **Exkurs: ACM**  
    *Association for Computing Machinery  (ACM)*, the world’s largest educational and scientific computing society, delivers resources that advance computing as a science and a profession. ACM provides the computing field's premier Digital Library and serves its members and the computing profession with leading-edge publications, conferences, and career resources.  
    **Membership**
    USD 19 / year for students. Mandatory if you want to be a CS researcher.
````


## Was gehört zu Informatik?
- Computer
- Algorithmen
- Programme und Programmiersprachen
- Berechnungsprozess

### Computer
Als Computer wurden zunächst Menschen bezeichnet, die Berechnungen durchführten.
```{image} ./pics/computer-etymology.png
:alt: ety
:class: bg-primary mb-1
:width: 600px
:align: center
```

- Filmtipp: Hidden Figures – Unerkannte Heldinnen

#### Computer
> Wie tauch(t)en Computer in unserem täglichen Leben auf? 


```{image} ./pics/human_computers.jpg
:alt: human
:class: bg-primary mb-1
:width: 200px
:align: left
```

```{image} ./pics/PDP10.jpg
:alt: PDP10
:class: bg-primary mb-1
:width: 200px
:align: right
```

```{image} ./pics/desktop_computer.jpg
:alt: desktop
:class: bg-primary mb-1
:width: 250px
:align: center
```

```{image} ./pics/iphone.jpg
:alt: iphone
:class: bg-primary mb-1
:width: 225px
:align: left
```

```{image} ./pics/pi.jpg
:alt: pi2
:class: bg-primary mb-1
:width: 200px
:align: right
```

```{image} ./pics/Dashboard.jpg
:alt: dash
:class: bg-primary mb-1
:width: 225px
:align: center
```

> Kann man den Begriff präzise definieren?

#### Was ist ein Computer?
- **Informatik Duden**: „(engl.: to compute = rechnen,
  berechnen; ursprünglich aus dem lat. computare = berechnen ...):
  Universell einsetzbares Gerät zur automatischen Verarbeitung von
  Daten.“

- Die prinzipiellen Fähigkeiten und Beschränkungen von
  idealisierten Computern
  werden durch das Automatenmodell der **universellen Turing-Maschine**
  beschrieben ($\rightarrow$ Theoretische Informatik).
  ````{note} 
  Die Turing-Maschine ist ein primitiver Rechner, der im Grunde alles enthält was ein moderner Höchstleistungsrechner kann.
  ````

- Der prinzipielle technische Aufbau eines (heutigen) Computers wird gut durch
  die **von-Neumann-Architektur** beschrieben ($\rightarrow$ Technische Informatik). Allerdings nutzen heutige Rechner sehr viel Parallelisierung, während die *von-Neumann-Architektur* einen sequenzielle Rechner darstellt.

#### Was tut ein Computer?
Um uns dieser Frage zu nähern, sollten wir vier Konzepte verstehen und
unterscheiden:  

- Ein-/Ausgabe
- Algorithmus
- Programm
- (Berechnungs)prozess.


Eine hilfreiche Analogie ist das Kochen...

### Algorithmen
#### Algorithmen und Kochen
##### Ein-/Ausgabe
```{image} ./pics/pizzazutaten.jpg
:alt: pizza
:class: bg-primary mb-1
:width: 300px
:align: left
```

```{image} ./pics/pizza_capricciosa.jpg
:alt: pizza2
:class: bg-primary mb-1
:width: 350px
:align: center
```


Hier interessiert nur: 

  - Welche Zutaten stehen zur Verfügung?
  - Wie sieht die fertige Pizza aus?  

Diese Pizza Analogie beinhaltet eine sogenannte *Spezifikation*: zu dieser Eingabe (bestimmte Zutaten) wird eine bestimmte Ausgabe (fertige Pizza) erwartet.

##### Algorithmus
- Wie wird die Pizza zubereitet? 

- Ich folge einem Rezept (= **Algorithmus**).

````{admonition} Wichtiger Unterschied
:class: warning

Wenn ich die Reihenfolge, in der die Paprika und die Pilze auf den
Teig gelegt werden, ändere, kommt immer noch eine Pizza raus. Bei Pizza ist also nur die grobe Reihenfolge der Schritte relevant.  
Bei einem Algorithmus muss die Reihenfolge der Schritte exakt eingehalten werden. Wird die Reihenfolge geändert, handelt es sich um einen anderen Algorithmus.
````

##### Unsere Vorstellung vom Kochen
Die Analogie ist nicht perfekt: 

- Kochrezepte sind meistens nicht *idiotensicher*. Sie lassen
Freiheiten, und sie setzen manches Wissen voraus.
- Die meisten Rezepte sind für festgelegte Mengen von festgelegten
Zutaten geschrieben.  
Für einen Algorithmus müssten zum Beispiel alle Mengenangaben in Abhängigkeit von der Personenanzahl angegeben werden.



Tatsächlich ist das Konzept eines Algorithmus ja nicht für die
Zubereitung von Pizzen sondern für die **Durchführung einer
  Berechnung** entwickelt worden (geht zurück auf  **Muhammed
  al-Chwarizmi** (ca. 780-850)).

#### Beispiel

````{prf:algorithm} Multiplikation zweier natürlicher Zahlen mithilfe von Addition und Subtraktion
:label: mul

**Eingabe**: Zwei natürliche Zahlen $L$ und $R$  
**Ausgabe**: Das Produkt von $L$ und $R$

1. Setze $P$ auf 0.
2. Falls $R = 0$, gebe $P$ als Ergebnis zurück.
3. Addiere $L$ zu $P$ hinzu.
4. Reduziere $R$ um 1.
5. Mache bei Schritt 2 weiter.
````

#### Eigenschaften

Ein Algorithmus ist eine Vorschrift zur Durchführung einer Berechnung
(Folge von einzelnen Schritten) mit folgenden Eigenschaften:

|Eigenschaft | Beschreibung |
--- | ---
| Präzision | Die Bedeutung jedes Schritts ist eindeutig festgelegt. |
| Effektivität | Jeder Schritt ist ausführbar. |
| Finitheit (statisch) | Die Vorschift ist ein endlicher Text. |
| Finitheit (dynamisch) | Zur Ausführung wird nur endlich viel Speicher benötigt.|
| Terminierung | Die Berechnung endet nach endlich vielen Schritten -- für alle legalen Eingaben |



##### Gegenbeispiele
- Male ein Haus hin (Präzision). $\rightarrow$ Welche Farbe? Welche Form? Wieviele Stockwerke?
- Teile die Zahl durch 0 (Effektivität). $\rightarrow$ nicht ausführbar
- Unendlich lange Vorschriften sind schwer vorstellbar, aber in
    der Mathematik gibt es unendliche Axiomensysteme (statische Finitheit).
- Schreibe die Zahl $\pi$ mit allen Nachkommastellen hin
    (dynamische Finitheit, Effektivität).
- Ersetze den Test $R=0$ durch $L=0$ (Terminierung nur noch wenn $L=0$!).

##### Weitere wünschenswerte Eigenschaften
|Eigenschaft | Beschreibung |
--- | ---
| Determinismus | Die Folgeschritte sind immer eindeutig festgelegt.
| Determiniertheit | Bei gleicher Eingabe erzeugt die Vorschrift die gleiche Ausgabe.
| Generalität | Die Vorschift kann eine Klasse von Problemen lösen.

Alle Beispiele, die wir in dieser Vorlesung kennen lernen werden,
erfüllen die Bedingungen. Aber auch Vorschriften, die diese Extra-Bedingungen
nicht erfüllen, werden als Algorithmen angesehen.

### Programme und Programmiersprachen
#### Programm
Ein **Programm** ist ein Algorithmus aufgeschrieben in einer 
geeigneten Sprache.  

```{image} ./pics/oliver_kochen.jpg
:alt: kochen
:class: bg-primary mb-1
:width: 300px
:align: left
```

```{image} ./pics/oliver_kochen_ita.jpg
:alt: kochen_ita
:class: bg-primary mb-1
:width: 300px
:align: center
```


Es gibt verschiedene Programmiersprachen, aber sie alle sind 
**formale** Sprachen, d.h., sie sind **exakt**, durch 
strikte Regeln, definiert. Das unterscheidet sie von natürlichen
Sprachen wie Deutsch oder Italienisch.

#### Programmiersprachen
````{glossary}
Systemprogrammiersprachen
  - Nah an der Maschine
  - Abbildung auf Maschine offensichtlich

Höhere Programmiersprachen
  - Idealisiertes Berechnungsmodell (*notional machine*)
  - Abbildung auf Maschine einfach

Deklarative Programmiersprachen
  - Spezifikation der Aufgabe anstelle eines Berechnungsmodells (Was statt Wie)
  - Abbildung auf Maschine anspruchsvoll
````

#### Elemente von Programmiersprachen
So wie **Sätze** in natürlicher Sprache aus *`Wörtern`* und
*`Satzzeichen`* einer bestimmten **`Grammatik`**
zusammengefügt werden,  
so werden **Programme** in einer Programmiersprache aus
*`Grundbausteinen`* unter Verwendung von
**`Kombinationsmitteln`** zusammengefügt.  
````{admonition}  Kombinationsmittel:
- Einfache Anweisungen mehrfach ausführen 
- Anweisungen nur unter bestimmten Bedingungen ausführen
- ...
````

Es kommt noch ein Konzept hinzu: **Abstraktionsmittel**, um
Programmelemente zu benennen.  
  **`Sprache`** $=$ **Syntax** $+$ **Semantik** $+$
  **Pragmatik**

### Berechnungsprozess
#### Prozess
```{image} ./pics/kochenUhrKalender.jpg
:alt: kalender
:class: bg-primary mb-1
:width: 300px
:align: center
```

Der Vorgang des Kochens, also das Ausführen eines Programms, 
an einem bestimmten Ort zu einer bestimmten Zeit.

#### Berechnungsprozess
- Der Ablauf eines Programms 
auf einem bestimmten Rechner zu einer bestimmten Zeit.
- In dieser Vorlesung spielt der Begriff des Prozesses keine große
Rolle. 
- In **Betriebssystemen** dreht sich alles um Prozesse. Z.B.:
Wieviel Rechenzeit und wieviel Hauptspeicher auf welchem Prozessor
bekommt welcher Prozess wann spendiert?

## Schluss
- Ein **Algorithmus** ist eine Vorschrift zur Durchführung einer Berechnung.
- Ein bestimmtes **Ein-/Ausgabe-Verhalten** kann i.A.~durch verschiedene Algorithmen
erreicht werden.
- Ein **Programm** ist die konkrete Umsetzung eines Algorithmus in
  einer Programmiersprache.
-  Ein Algorithmus kann in verschiedenen **Programmiersprachen** und durch
verschiedene Programme implementiert werden.
- Beliebig viele **Prozesse** können das gleiche Programm auf
  einem oder mehreren Computern auf der ganzen Welt ausführen.

````{admonition} Aphorismus

```{epigraph}
Ein Rechner ist ein Vollidiot mit Spezialbegabung.
Er hat ein großes, präzises Gedächtnis und kann schneller
rechnen als ein Mensch. 

-- Prof. Dr. Gerhard Goos (1962)
```
````

## Exkurs: Think like a computer scientist
### Denken wie ein Informatiker/eine Informatikerin
- Ein Studium vermittelt **Kenntnisse** und **Fähigkeiten**
- Es verändert aber auch die **Sicht auf die Welt**
- Informatiker tendieren dazu, in ihrer Umgebung nach dem
  **algorithmischen Kern** von Problemen zu suchen...
- ... und diesen Kern dann auf dem Computer zu lösen

````{admonition} Beispielszenario: Die gemeinsame Reisekasse
Im Ausland gibt es oft nur eine gemeinschaftliche Rechnung, die einer in der Gruppe bezahlen muss.
````
- Das ist einfacher und wird abwechselnd von den Gruppenmitgliedern übernommen.
- Zum Schluss haben die einen mehr bezahlt, die anderen weniger.  
$\rightarrow$ Es sind **Ausgleichszahlungen** nötig.
- Bei 3-4 Leuten einfach, bei 8-10 Leuten wird es unübersichtlich.

### Beispiel
```{image} ./pics/travel.png
:alt: travel
:class: bg-primary mb-1
:width: 300px
:align: center
```
````{admonition} Nachteil
 U.U. muss jemand mehrere Überweisungen tätigen oder jemand muss auf mehrere Überweisungen warten.
````

### Das Reisekassen-Ausgleichszahlungs-Problem (RAP)
Eine abendliche Diskussion ergab folgende **Anforderungen** für
das RAP:

  Jeder sollte maximal eine Überweisung tätigen und eine
  Überweisung empfangen und der maximal zu überweisende Betrag sollte minimal
  sein. 

D.h. Bestimme, wer wem was zu bezahlen hat:

- Finde eine Reihenfolge der Gruppenmitglieder, sodass die
    Zahlungen von links nach rechts getätigt werden.
- Ansatz: Ausprobieren aller Reihenfolgen.

### Einige mögliche Reihenfolgen
```{image} ./pics/travel_sol.png
:alt: travel_sol
:class: bg-primary mb-1
:width: 300px
:align: center
```

````{prf:algorithm} Reisekassen-Ausgleichszahlungs-Algorithmus
Iteriere über alle Reihenfolgen (Permutationen) und führe für jede Reihenfolge folgendes durch:

- Prüfe ob nur positive Zahlungen erfolgen,
- falls ja, bestimme und merke den Wert der maximalen  Zahlung für diese Reihenfolge.
- Gib eine Reihenfolge mit minimalem Wert zurück.  
````

$\rightarrow$ Es müssen $n! \approx n^n$ Reihenfolgen betrachtet werden, was bei
großem $n$ sehr lange dauern kann.  
$\rightarrow$ Es gibt (vermutlich) keine effiziente
Lösung, da das Problem **NP-schwer** ist.

  
  ***Der Urlaubs-Abschluss ist jedenfalls gerettet.***