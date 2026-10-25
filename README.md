# Feldzug – Mittelalter-Strategie (Prototyp)

Rundenbasiertes Strategiespiel im freien Fantasie-Mittelalter. Zwei Parteien, je ein Heer.
Entschieden wird nicht auf dem Schlachtfeld, sondern beim **Nachschub**: Verpflegung und Munition gehen aus.

Eine einzige Datei (`index.html`), kein Build nötig – läuft im Browser und später als Android-App (Capacitor).

## Starten

- Lokal: `index.html` im Browser öffnen.
- GitHub Pages: Repo → *Settings → Pages → Deploy from branch → `main` / root*.

## Bedienung

- Ort antippen → Marschbefehl. Die gelben Zahlen zeigen, wo das Heer am Ende des 1., 2., … Zuges steht.
- **Zug beenden** → Bewegung, Versorgung und Gegnerzug laufen ab.
- **Plündern** (nur in fremden/neutralen Dörfern), **Halt** (Marschbefehl löschen).
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

- Späher (große Sichtweite, schnell, kämpfen nicht)
- Pioniere: Straßen bauen, Brücken, Wachtürme/Schanzen, Gebiet erweitern
- Wirtschaft: Dörfer und Regionen liefern Getreide und Gold; Plündern wirkt auf die Wirtschaft
- Tross-Kapazität (mehr Munition = langsamerer Heer), Jahreszeiten, Söldner
- Android-APK über Capacitor
- Balancing (die Burg-Verteidigung ist aktuell sehr stark)

## Debug

`window.__game` gibt in der Browser-Konsole Zugriff auf Spielzustand und Funktionen (z. B. `__game.G`).
