# Feldzug – Mittelalter-Strategie (Prototyp)

Rundenbasiertes Strategiespiel im freien Fantasie-Mittelalter. Zwei Parteien, mehrere Heere pro Seite (max. 5), Wirtschaft und Werkstatt.
Entschieden wird nicht auf dem Schlachtfeld, sondern beim **Nachschub**: Verpflegung und Munition gehen aus.

Eine einzige Datei (`index.html`), kein Build nötig – läuft im Browser und später als Android-App (Capacitor).

## Starten

- Lokal: `index.html` im Browser öffnen.
- GitHub Pages: Repo → *Settings → Pages → Deploy from branch → `main` / root*.

## Version 4 (Echtzeit)

- Läuft in **Echtzeit** (⏸ Pause, 1×/2×/4× Tempo). Menüs halten die Zeit an.
- **Gold, Brot und Eisen** fliegen von den Orten animiert in Schatztruhe, Vorrat und Berg-Symbol.
- **Krieger nur bei Gelegenheit**: Angebote erscheinen zeitlich begrenzt als goldene Kreise an deinen Orten (Burg, Dorf, Markt, Eisenmine).
- **Steuern pro Ort** (niedrig/normal/hoch): mehr Gold, aber sinkende Zufriedenheit und damit weniger Ertrag.
- **Handel**: Händlerwagen pendeln zwischen zwei eigenen Orten und bringen Gold und Waren; feindliche Heere können sie überfallen.
- Marschierende Soldaten, wehende Fahnen, Windmühle, Rauch, Wolkenschatten, Schlacht-Effekte.

## Bedienung

- Ort antippen → Infofeld mit Marschbefehl, Steuern, Handel und Anwerben.
- **Befehle**: abspalten, vereinen, bauen, Marsch stoppen. **Kaufen**: Truppen für Gold.
- Ziehen = Karte verschieben, zwei Finger / Mausrad = Zoomen, ⌖ = auf das eigene Heer zentrieren.

## Regeln im Prototyp

| Thema | Regel |
|---|---|
| Karte | Orte als Knoten, Wege als Kanten. Gelände: Straße, offenes Land, Wald, Hügel, Sumpf, Gebirge, Furten (Fluss ohne Brücke) |
| Marsch | 2,5 Bewegungspunkte pro Zug; Straße ist am schnellsten, Gebirge/Sumpf am langsamsten |
| Verpflegung | Verbrauch pro Zug ≈ Truppenstärke / 60. Ist alles aufgebraucht, desertieren Soldaten |
| Nachschub | Verbindung zur Heimatburg über den günstigsten Weg (geländeabhängig). Je länger/schlechter der Weg, desto weniger kommt an. Steht der Feind auf dem Weg, ist die Linie gekappt |
| Munition | Pfeile (Bogenschützen) und Pulver (Kanoniere). Ohne Munition kämpfen sie kaum noch |
| Plündern | Füllt Verpflegung auf, das Dorf ist danach 8 Züge ausgeblutet, Loyalität sinkt |
| Nebel | Gelände, Burgen, Dörfer und Straßen sind von Anfang an bekannt. Der Feind und aktuelle Dorfzustände nur in Sichtweite. Die KI folgt denselben Sichtregeln |
| Kampf | Treffen sich die Heere, entscheidet eine Formel (Truppen, Waffengattungen, Munition, Versorgung, Gelände, Zufall). Der Verlierer zieht sich zurück |
| Sieg | Gegnerische Burg einnehmen oder das gegnerische Heer aufreiben |

## Geplant

- Brücken bauen, Gebietsgrenzen
- Tross-Kapazität (mehr Munition = langsamerer Heer), Jahreszeiten, Söldner
- Android-APK über Capacitor
- Balancing (die Burg-Verteidigung ist aktuell sehr stark)

## Debug

`window.__game` gibt in der Browser-Konsole Zugriff auf Spielzustand und Funktionen (z. B. `__game.G`).
