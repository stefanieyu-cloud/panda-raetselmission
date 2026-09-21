# Panda Rätselmission 🐼

Ein digitales Haustier zum Chinesischlernen (Kursbuch *Long neu 龙 A1–A2*).
Schüler:innen adoptieren einen Panda, lösen täglich ein kurzes Rätsel und begleiten ihn
30 Felder weit über eine Karte.

**Live:** https://stefanieyu-cloud.github.io/panda-raetselmission/

## Für Schüler:innen

1. Mit Spitzname und Passwort registrieren, danach immer anmelden.
2. Dem Panda einen Namen geben.
3. Jeden Tag mindestens ein Rätsel lösen. Der erste Treffer des Tages bringt einen
   🥟 Dumpling-Stempel und rückt den Panda ein Feld weiter.
4. Bei 7, 14, 21 und 30 Dumplings wartet ein 🎁 Überraschungsgeschenk.

Dazwischen will der Panda versorgt werden: füttern, spielen, saubermachen. Zwischen
21 und 7 Uhr schläft er — wer ihn weckt, bekommt einen mürrischen Panda.

## Rätseltypen

Zuordnung (Pinyin ↔ Hanzi ↔ Deutsch), 三胞胎 Drillinge, Geheimcode, Code-Scanner, Lückentext,
Koordinaten-Rätsel, Code-Rad, Satzmorph sowie Pinyin- und Hanzi-Sudoku. Die schwierigeren Typen
schalten sich erst nach 7, 14 bzw. 21 Dumplings frei.

## Konten und Daten

Anmeldung über Firebase Authentication, Fortschritt in Firestore. Aus dem Spitznamen wird intern
eine Pseudo-Adresse (`spitzname@panda.local`), es werden also **keine echten E-Mail-Adressen**
erfasst. Gespeichert sind nur Spitzname, Panda-Name, Geburtsdatum, Lernfortschritt und
Pflegewerte — keine Klarnamen, keine Schule, keine Klasse.

Die Firestore-Regeln erlauben jedem Konto ausschließlich den **eigenen** Datensatz zu schreiben;
gelesen wird nur von angemeldeten Nutzer:innen. Ist der Dienst nicht erreichbar, lässt sich ohne
Anmeldung rein lokal weiterüben (`localStorage`).

## Für die Lehrkraft

- `?test=1` an die Adresse hängen blendet ein Testpanel ein. „+1 Tag simulieren" zeigt den ganzen
  30-Tage-Verlauf in wenigen Klicks.
- `?calib=1` zeigt beim Klick auf die Karte die Prozentkoordinaten — nützlich, falls ein
  Feld auf der Karte verschoben werden soll (`MAP_POINTS` in `index.html`).
- Die Bestenliste zeigt Spitzname und Dumpling-Anzahl der besten 25.

## Aufbau

```
index.html   – die gesamte App (HTML, CSS, JavaScript in einer Datei)
img/         – acht Panda-Zustandsbilder und die Kartenillustration
```

Die Panda- und Kartenillustrationen stammen von der Kursleiterin und werden mit ihrer Erlaubnis
verwendet. Die gemalten Zahlen auf der Karte sind fehlerhaft (11, 16 und 25 doppelt, 12 fehlt),
deshalb liegt die tatsächliche Route als eigene Linie mit 30 Feldern darüber.
