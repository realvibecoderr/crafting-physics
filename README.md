# Unit Lab ⚛️

Eine spielerische Lern-App, die zeigt, wie sich physikalische Einheiten aus den SI-Basiseinheiten zusammensetzen. Das Prinzip ähnelt Little Alchemy: Du kombinierst Kacheln und entdeckst dabei immer neue Einheiten.

> Beispiel: Meter ÷ Sekunde = Meter pro Sekunde (Geschwindigkeit)

## Spielprinzip

1. Du startest mit den 7 SI-Basiseinheiten.
2. Ziehe zwei Kacheln auf die Werkbank (oder tippe sie nacheinander an).
3. Wähle die Verknüpfung: **×** (mal), **÷** (geteilt), **x²** / **x³** (Potenz) oder **1/x** (Kehrwert).
4. Ergibt sich eine bekannte Einheit, wird sie entdeckt und mit Erklärung, Formel und Alltagsbeispiel im Sammelbuch gespeichert.
5. Ergibt sich eine gültige, aber unbenannte Einheit (z. B. m²/s²), bleibt sie als Zwischenkachel nutzbar.

### Die Basiseinheiten

| Größe | Einheit | Symbol |
|---|---|---|
| Länge | Meter | m |
| Masse | Kilogramm | kg |
| Zeit | Sekunde | s |
| Stromstärke | Ampere | A |
| Temperatur | Kelvin | K |
| Stoffmenge | Mol | mol |
| Lichtstärke | Candela | cd |

### Beispiele für Entdeckungen

| Einheit | Aufbau |
|---|---|
| Geschwindigkeit | m ÷ s |
| Beschleunigung | (m/s) ÷ s |
| Newton (Kraft) | kg × m/s² |
| Joule (Energie) | N × m |
| Watt (Leistung) | J ÷ s |
| Coulomb (Ladung) | A × s |
| Volt (Spannung) | W ÷ A |
| Ohm (Widerstand) | V ÷ A |

## Funktionen

- Crafting-Mechanik mit Drag & Drop und Tippen (mobilfreundlich)
- Katalog mit abgeleiteten SI-Einheiten in drei Schwierigkeitsstufen
- Lernkarte zu jeder Entdeckung mit Rechenweg, Erklärung und Alltagsbeispiel
- Sammelbuch mit Fortschrittsanzeige
- Tipp-Funktion ohne Lösung zu verraten
- Fortschritt wird lokal im Browser gespeichert

## Wie es funktioniert

Jede Einheit wird intern als Vektor aus sieben Exponenten gespeichert, einer pro Basiseinheit. Beispiel Newton (kg · m · s⁻²):

```
[m: 1, kg: 1, s: -2, A: 0, K: 0, mol: 0, cd: 0]
```

- Multiplizieren addiert die Exponenten.
- Dividieren subtrahiert sie.
- Potenzieren multipliziert sie.

Das Ergebnis wird mit dem Einheitenkatalog verglichen. So funktionieren auch Wege, die niemand vorher als Rezept eingetragen hat (Joule über N · m oder über kg · m²/s²).

## Projektstruktur

```
unit-lab/
├── index.html   # die gesamte App (HTML, CSS, JavaScript)
└── README.md
```

## Starten

Es ist keine Installation nötig.

1. Repository herunterladen oder klonen:
   ```bash
   git clone https://github.com/DEIN-NAME/unit-lab.git
   ```
2. `index.html` im Browser öffnen.

### Online ansehen mit GitHub Pages

1. Im Repository **Settings → Pages** öffnen.
2. Branch `main` und Ordner `/ (root)` auswählen.
3. Die App ist danach unter `https://DEIN-NAME.github.io/unit-lab/` erreichbar.

## Neue Einheiten hinzufügen

Der Katalog ist datengetrieben. Eine neue Einheit braucht nur einen Eintrag mit diesen Feldern:

- Name und Symbol
- Größe (z. B. „Kraft")
- Exponentenvektor
- Formel
- Kurze Erklärung und Alltagsbeispiel
- Schwierigkeitsstufe (1–3)

## Geplante Erweiterungen

- Vorsätze wie kilo, milli und mikro als Bonusstufe
- Rückwärts-Rätsel: Zerlege eine Einheit in Basiseinheiten
- Quizrunden zum Wiederholen

## Lizenz

Noch nicht festgelegt. Mit [MIT](https://choosealicense.com/licenses/mit/) kann jeder die App frei nutzen und weiterentwickeln.
