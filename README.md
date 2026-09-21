# Panda Rätselmission 🐼

Ein kleines digitales Haustier zum Chinesischlernen (Kursbuch *Long neu 龙 A1–A2*).
Schüler:innen adoptieren einen Panda, lösen täglich ein kurzes Rätsel und begleiten ihn
30 Tage lang über eine Karte.

## Für Schüler:innen

1. Panda benennen und adoptieren – mehr braucht es nicht.
2. Jeden Tag mindestens ein Rätsel lösen.
3. Jeder erfolgreiche Tag gibt einen 🥟 Dumpling-Stempel, der Panda rückt ein Feld weiter.
4. Bei 7, 14, 21 und 30 Dumplings wartet ein 🎁 Überraschungsgeschenk.

Kein Login, keine Anmeldung, keine Datenbank. Der Spielstand liegt ausschließlich im Browser
des jeweiligen Geräts (`localStorage`). Mit dem **Speichercode** lässt sich ein Panda auf ein
anderes Gerät mitnehmen.

## Rätseltypen

Zuordnung (Pinyin ↔ Hanzi ↔ Deutsch), 三胞胎 Drillinge, Geheimcode, Code-Scanner, Lückentext,
Koordinaten-Rätsel, Code-Rad, Satzmorph sowie Pinyin- und Hanzi-Sudoku. Schwierigere Typen
schalten sich erst nach 7, 14 bzw. 21 Dumplings frei.

## Für die Lehrkraft

Die Adresse mit `?test=1` aufrufen (z. B. `…/index.html?test=1`) blendet ein Testpanel ein.
Damit lässt sich „+1 Tag simulieren" klicken, um den ganzen 30-Tage-Verlauf in wenigen Sekunden
durchzusehen. Ohne diesen Zusatz ist das Panel unsichtbar.

Am Gerät der Schüler:innen sind auf einen Blick sichtbar: Panda-Name, Geburtsdatum,
Tag X von 30, Stimmung, Kartenfortschritt, gesammelte Dumplings und freigeschaltete Geschenke.

## Aufbau

```
index.html   – die gesamte App (HTML, CSS, JavaScript)
img/         – die acht Panda-Zustandsbilder
```

Die Panda-Illustrationen stammen von der Kursleiterin und werden mit ihrer Erlaubnis verwendet.
