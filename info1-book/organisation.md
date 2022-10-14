# Organisation
Hier sind noch einmal ein paar wichtige organisatorische Dinge zusammen gefasst.
Aktuelle Informationen kann man auf der [Webseite](http://proglang.informatik.uni-freiburg.de/teaching/info1/2022/)
nachschauen.

## Vorlesung
### Wann
Dienstag 10:15-11:45 Uhr, Mittwoch 12:15-13:00 Uhr

### Weihnachtspause
Donnerstag, 23.12.2021 bis Freitag, 6.1.2022

### Ende der Vorlesungszeit
Samstag, 11.2.2023

### Wo
- Gebäude 101, Hörsaal 00-026
- Online per Livestream (siehe [Webseite](http://proglang.informatik.uni-freiburg.de/teaching/info1/2022/))

## Übungen
- Ein Übungsblatt per Woche
- 14 Übungsblätter
- Ausgabe der Übungsblätter: jeweils bis zur Dienstagsvorlesung auf der Webseite der Vorlesung
- Bearbeitungszeit in der Regel sechs Tage (Termin laut Blatt)
- Einreichen der Übungen:
  jeweils montags, bis 9:00 Uhr morgens, über [Online-System](https://git.laurel.informatik.uni-freiburg.de/)
- Bearbeitung der Aufgaben in **der Regel einzeln**, außer designierte
  Gruppenaufgaben

## Git
Für die Abgabe der Übungsblätter verwenden wir das Versionsverwaltungstool `git`.
Da dies der Standard in vielen Projekten der Informatik ist gibt es hier ein
kleiner Überblick über die wichtigsten Dinge.
Ein Videotutorial zu der Übungsabgabe kann man [hier](https://youtu.be/n6fJp2u6Ws0) finden.

### Funktionsweise
Git ist ein Versionsverwaltungstool d.h. man fängt bei einer initialen Version an und
"hängt" an diese neue Versionen an.
Dies kann man auch als gerichteten azyklischen Graph sehen (mehr dazu in Graphentheorie).
Git speichert dabei immer die Änderungen zu der vorherigen Version.  
Der Arbeitsfluss sieht in der Regel folgendermaßen aus: man dupliziert die Version welche Online verfügbar ist, teilt Git die Änderungen mit welche man
vorgenommen hat, erstellt eine neue Version (Commit) und läd dann diese Änderung wieder hoch.

### Begrifflichkeiten
Hier sind ein paar Begrifflichkeiten welche man im Bezug auf Git häufig findet.
- Repository: Ein Depot in dem sich alle Dateien sowie Versionsinformationen befinden.
- Commit: Eine Version welche Änderungen, ein Kommentar, Autor und weitere Informationen beinhaltet.
- Branch: Kann man als Zweig oder Linie sehen. Ist für uns nicht so relevant da die Übungsabgaben nur einen Branch nutzen.
  Bei größeren Projekten lässt das z.B. parallele Entwicklung zweier Versionen oder Features zu.
  In unserem Fall gibt es ein Standardbranch welcher in der Regel `master` genannt wird. Wenn man besonders politisch korrekt sein möchte kann man ihn auch `main` nennen.

Ein kleiner Spickzettel über häufig verwendete Befehle kann man [hier](https://training.github.com/downloads/de/github-git-cheat-sheet/) finden.
Besonders wichtig sind folgende Subcommands: `clone`, `add`, `commit`, `push` und `pull`