---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.13.8
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# 2. Erste Schritte in Python
## Allgemeines
### Programmiersprachen
Programmiersprachen gibt es wie Sand am Meer...
```{admonition} Beispiele
Ada, Basic, C, C++, C#, Cobol, Curry, F#, Fortran, Go,
Gödel, HAL, Haskell, Java, JavaScript, Kotlin, Lisp,
Lua, Mercury, Miranda, ML, OCaml, Pascal, Perl, PHP, Python, Prolog, R, Ruby, Scheme, 
Shakespeare, Smalltalk, Swift, TypeScript, Visual Basic, u.v.m.
```

Wir verwenden **Python** (genauer Python 3), eine

- objektorientierte,
- dynamisch getypte,  
  (Überprüfung von Typen findet erst zur Laufzeit statt)
- interpretierte und interaktive
  $\rightarrow$ Man kann mit Python wie mit einem Taschenrechner interagieren, dh. Befehle werden beim Eingeben ausgeführt
- höhere Programmiersprache.
 
````{admonition} Die Programmiersprache Python 
```{figure} ./pics/photoVanRossum.jpg
---
scale: 20%
align: right
---
Guido Van Rossum
```
- Anfang der 90er Jahre als
  Skriptsprache für das verteilte Betriebssystem Amoeba in Holland entwickelt;
- gilt als einfach zu erlernen;
- wurde kontinuierlich von Guido van Rossum bei Google (seit 2013
Dropbox; seit 2019 i.R.) weiterentwickelt.
- bezieht sich auf die Komikertruppe *Monty Python*.
````



### Literatur
````{admonition} Lehrbücher zu Python3
- Allen Downey, *Think Python: How to Think Like a
    Computer Scientist*, O'Reilly, 2nd edition, 2015
- als PDF herunterladbar oder als HTML lesbar (Green Tea Press): https://greenteapress.com/wp/think-python-2e/
- als deutsche Version: Programmieren lernen mit Python, O'Reilly,
  2013.
- Mark Lutz, *Learning Python*, O'Reilly, 2013 (deutsche
  Ausgabe ist veraltet!)
- Michael Weigend, *Python gepackte Referenz*, mit Verlag,
  8. Auflage 2020 (als Nachschlagwerk, V3.8)
- Viele Videos und Online-Kurse
- Allgemeiner Hintergrund: Perdita Stevens, *How to Write
    Good Programs. A Guide for Students*, Cambridge University Press, 2020.
````

## Warum Python?
### Warum Python benutzen?

````{glossary}
Softwarequalität
  - Lesbarkeit
  - Software-Reuse-Mechanismen (wie OOP)

Programmierer-Produktivität
  - Python-Programme sind oft 50\% kürzer als vergleichbare Java oder C++-Programme.
  - Kein Edit-Compile-Test-Zyklus, sondern direkte Tests

Portabilität
  $\rightarrow$ läuft auf allen Betriebssystemen und im Web

Support-Bibliotheken (Batterien sind enthalten)
  $\rightarrow$ es gibt zu allem Bibliotheken

Komponenten-Integrierbarkeit 
  (Java, .Net, COM, Silverlight, SOAP, CORBA, ...)
````


Die Statistik zeigt, dass Python als Einsteigersprache allgemein beliebt ist.
```{image} ./pics/top39.jpg
:alt: usa
:class: bg-primary mb-1
:width: 325px
:align: left
```

#### Wer benutzt Python?
- Google: Web search, App engine, YouTube
- Dropbox
- CCP Games: EVE Online
- 2kgames: Civilization IV (SDK)
- Industrial Light \& Magic: Workflow-Automatisierung
- ESRI: Für Nutzerprogrammierung des GIS
- Intel, Cisco, HP, Seagate: Hardwaretesting
- NASA, JPL, Alamos: Scientific Computing

- ... http://www.python.org/about/success/

#### Was geht nicht?
- Python ist langsamer als Java und C++
  $\rightarrow$ nicht für Performance-kritische Situationen geeignet
- Wieviel langsamer?  
  https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html
- Eignet sich nicht für das Schreiben von Gerätetreibern
- Eignet sich nicht direkt für die Programmierung von (kleinen)
    Mikrocontrollern (*bare metal programming*) 
- ``Python is not considered ideal for mobile app
    development and game development due to the consumption of more
    memory and its slow processing speed while compared to other
    programming languages.''   
    https://squareboat.com/blog/advantages-and-disadvantages-of-python

#### Quellen
Unter http://python.org/ befinden sich die aktuelle Dokumentation und
Links zum Herunterladen (uns interessiert Python 3.X, $X\ge9$) für

- *Windows*,
- *MacOSX*,
- *Unixes* (Quellpakete),
- für aktuelle *Linux-Distributionen* gibt es Packages für
  die jeweilige Distribution, meistens bereits installiert!


Läuft u.a. auch auf dem **Raspberry Pi**!

## Python-Interpreter
### Interpreter- vs. Compiler-Sprachen

**Interpreter-Sprachen:** Zunächst wird Quellcode (in eine Datei) geschrieben, an den Interpreter weitergegeben und dann das Ergebnis ausgegeben.
```{image} ./pics/interpreter.png
:alt: interpreter
:class: bg-primary mb-1
:width: 300px
:align: center
```

**Compiler-Sprachen:** Der Quellcode muss erst durch den Compiler zu Objektcode umgewandelt werden und dieser wird dann ausgeführt.

```{image} ./pics/compiler.png
:alt: compiler
:class: bg-primary mb-1
:width: 450px
:align: center
```

    Python ist eine Interpreter-Sprache.

### Interaktiver und Skript-Modus
Der Python-Interpreter kann auf folgende Arten gestartet werden:

- im **interaktiven Modus** (ohne Angabe von Programm-Parametern)  
  $\rightarrow$ **Ausdrücke** und
  **Anweisungen** können interaktiv eintippt werden, der Interpreter wertet diese aus und
  druckt ggf. das Ergebnis.

- im **Skript-Modus** (unter Angabe einer **Skript-/Programm-Datei**)  
  $\rightarrow$ Ein **Programm** (auch **Skript** genannt) wird eingelesen und dann
  ausgeführt.

#### Interaktives Nutzen der Shell
  Nach Starten des Interpreters erscheint das **Prompt-Zeichen** ('>>>').
  Das Eintippen von **Ausdrücken** wertet diese aus und liefert ein Ergebnis.


  Um dem Interpreter eine Ausgabe zu entlocken, gibt es zwei Methoden:  
  Zum einen wertet der Interpreter jeden eingegebenen Ausdruck aus und gibt das Ergebnis aus:

  ```{code-cell} ipython3
  7 * 6
  ```

  ```{code-cell} ipython3
  "Hello world"
  ```

  ```{code-cell} ipython3
  "spam " * 4
  ```
  $\rightarrow$ Multiplikation eines Strings mit einer Zahl vervielfacht den String.

  Zum anderen kann die `print`-Funktion den Wert eines
  Ausdrucks ausgeben:
  ```{code-cell} ipython3
  print(7 * 6)
  ```

  ```{code-cell} ipython3
  print("Hello world")
  ```

  ```{code-cell} ipython3
  print("spam " * 4)
  ```

  `print` ist der übliche Weg, Ausgaben zu erzeugen und funktioniert
  daher auch in richtigen Programmen.


**Etwas mehr zu *print***
```{code-cell} ipython3
print("2 + 2 =", 2 + 2, "(vier)")
```

  - *print* kann mehrere Ausdrücke durch Kommata getrennt verarbeiten.
  - Die Ergebnisse werden in derselben Zeile
      durch Leerzeichen getrennt ausgegeben.

#### Exkurs: Hello-World-Programme
*Hello-World*-Programme dienen dazu, eine erste Idee vom Stil einer
Programmiersprache zu bekommen.

Python
```{code-cell} ipython3
print("Hello World!")
```

Java
```
class HelloWorld {  
  public static void main(String[] arg) {  
    System.out.println("Hello World!");   
  }  
}
```


Brainfuck

    ++++++++++[>+++++++>++++++++++>+++>+<<<<-]
    >++.>+.+++++++..+++.>++.<<+++++++++++++++.
    >.+++.------.--------.>+.>.



## Rechnen
### Zahlen
Python kennt drei verschiedene Datentypen für Zahlen:

- `int` für ganze Zahlen;
- `float` für Gleitkommazahlen \\(eine verrückte Teilmenge der
    rationalen Zahlen);
- `complex` für komplexe Gleitkommazahlen.

#### *int*
Schreibweise für Konstanten vom Typ `int`:
```{code-cell} ipython3
10
```

```{code-cell} ipython3
-20
```
```{admonition} Syntax
:class: important

Die Schreibweise von Konstanten ist ein Aspekt der **Syntax** einer Programmiersprache.
Sie beschreibt, welche Zeichen erlaubt sind, welche Worte vordefiniert sind und wie Sätze (Programme) in der Programmiersprache aussehen müssen.
```

##### Rechnen mit `int`
Python benutzt für Arithmetik die folgenden Symbole:

- Grundrechenarten: `+`, `-`, `*`
    `/`
- Ganzzahlige Division: `//`
- Modulo: `\%`
- Potenz: `**`

```{code-cell} ipython3
14 * 12 + 10
```

```{code-cell} ipython3
 14 * (12 + 10)
```

```{code-cell} ipython3
 13 % 8
```

```{code-cell} ipython3
 11 ** 11
```

```{code-cell} ipython3
```


##### Integer-Division: Ganzzahlig oder nicht?
Der Divisionsoperator `/` liefert das Ergebnis als `float`.  
Der Operator *//* rundet auf die nächste ganze Zahl ab.  
```{code-block} ipython3
20 / 3
```

```{code-block} ipython3
 -20 / 3
```

```{code-block} ipython3
20 // 3
```

```{code-block} ipython3
 -20 // 3
```


#### *float*
Syntax von `float`-Konstanten: mit Dezimalpunkt und optionalem Exponent:  
    `2.44`, `1.0`, `5.`, `1.5e+100` (bedeutet $1,5 \times 10^{100}$)
  

Die arithmetischen Operatoren für `float` und `complex` sind die gleichen wie für die ganzzahligen Typen:  

- Grundrechenarten: `+`, `-`, `*`, `/`, `//`
- Potenz: `**`
- Rest bei Division für ganzzahliges Ergebnis: `\%`

##### Rechnen mit *float*

```{code-cell} ipython3
print(1.23 * 4.56)
```

```{code-cell} ipython3
  print(17 / 2.0)
```

```{code-cell} ipython3
  print(23.1 % 2.7)
```

```{code-cell} ipython3
  print(1.5 ** 100)
```

```{code-cell} ipython3
  print(10 ** 0.5)
```

```{code-cell} ipython3
  print(4.23 ** 3.11)
```


````{warning} 
Wie viel ist $2 - 2.1$?
  - Die meisten Dezimalzahlen können **nicht** exakt als Gleitkommazahlen
      dargestellt werden (!)
  - Programmier-Neulinge finden Ausgaben wie die obige oft verwirrend ---
      die Ursache liegt in der Natur der Gleitkommazahlen und ist unabhängig von der Programmiersprache.
````
```{code-cell} ipython3
2 - 2.1
```

#### *complex*
Syntax von `complex`-Konstanten: Summe von (optionalem) Realteil und Imaginärteil mit imaginärer Einheit `j`:  
    `4+2j`, `2.3+1j`, `2j`, `5.1+0j`

##### Rechnen mit *complex*
```{code-cell} ipython3
print(2+3j + 4-1j)
```

```{code-cell} ipython3
 1+2j * 100
```

```{code-cell} ipython3
 (1+2j) * 100
```

```{code-cell} ipython3
 print((-1+0j) ** 0.5)
```


#### Automatische Typkonversionen
Haben die Operanden
 unterschiedliche Typen, wie in `100 * (1+2j)` oder
 `(-1) ** 0.5`, werden die Operanden vom *kleineren* Typ zum
 *größeren* hin konvertiert. Dabei werden die folgenden Bedingungen der
 Reihe nach geprüft, die erste zutreffende Regel gewinnt:

- Ist einer der Operanden ein `complex`, so wird der
     andere zu
     `complex` konvertiert (falls er das nicht schon ist).
- Ist einer der Operanden ein `float` (und keiner ein
     `complex`), so wird der andere zu `float`
     konvertiert (falls er das nicht schon ist).

#### Überläufe und Unterläufe
- Ganze Zahlen können beliebig groß (und klein) werden. 
- Gleitkommazahlen haben einen eingeschränkten Wertebereich
    (meist gemäß dem IEEE-754 Standard, double precision).
- Durch Interpreter, aber nicht durch Python festgelegt.
  
```{code-cell} ipython3
1e-999
```

```{code-cell} ipython3
1e+999
```

```{code-cell} ipython3
1e+999 - 1e+999
```
    `inf` steht für *infinity* und `nan` für
    *not a number*. Mit beiden kann weiter gerechnet werden!

## Zusammenfassung
- Python ist ein **objektorientierte**, **dynamisch getypte**,
    **interpretierte** und **interaktive höhere** Programmiersprache.
- Python ist sehr **populär** und wird in den USA als die
    **häufigste Anfängersprache** genannt.
    Betriebssystemen.
- Für manche Anwendungen ist Python zu **langsam** und
    **verbraucht zu viel Speicher**.
- Es gibt drei **numerische Typen** in Python: `int`,
    `float`, und `complex`.
- Es werden die üblichen **arithmetischen Operationen** unterstützt.
