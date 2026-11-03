# Territory Clash 🎮

Mobile-First Strategiespiel in einer einzigen `index.html`. Spielbar gegen KI oder zu zweit an einem Handy.

## Spielen

GitHub Pages unter **Settings → Pages → Deploy from a branch → main / (root)** aktivieren.

Danach: https://proflarsschnyder.github.io/territory/

## Die wichtigsten Regeln

**Kampfaktionen:** Blau beginnt mit **1** Eroberung oder Angriff. Danach hat jeder Spieler pro Zug **2** Kampfaktionen. Jede Eroberung eines neutralen Felds und jeder erfolgreiche Angriff kostet exakt **1** Kampfaktion. Ein erfolgreicher Angriff gibt **keine zusätzliche Aktion**. Sobald alle Kampfaktionen verbraucht sind, bleibt der Spieler am Zug und kann weiterhin mit Münzen bauen und verstärken. **Nur der Button «ZUG BEENDEN» wechselt den Spieler.** Die KI beendet ihre Züge selbst.

**Stärke und Münzen:** Eigene Felder lassen sich für 2 Münzen um +1 Stärke verstärken, ohne Stärkeobergrenze und ohne Kampfaktionskosten. Ein erfolgreicher Angriff erfordert eine höhere effektive Angriffsstärke als Verteidigungsstärke. Die Stärke des Angreifers sinkt normalerweise um 1. Bonuswerte sind direkt auf den Kacheln sichtbar (⚔ orange, 🛡 türkis, beide violett).

**Goldminen ⛏:** Die einzige Spezialfeldart mit ausbaubaren Stufen. Pro Stufe gibt es 1 Münze pro eigenem Zug. Upgrade-Kosten steigen: **3, 6, 10, 15, 21, ... Münzen**. Minen können über das Feld-Auswahlmenü aufgewertet werden, ohne Kampfaktion. Keine feste Stufenobergrenze.

**Schatzfelder ✦:** Die erste Eroberung bringt einmalig 5 Münzen. Anschliessende Rückeroberungen bringen nichts.

**Warpfelder 🌀:** Vier neutral gelegene Warpfelder bilden für jede Fraktion ein Netzwerk. Wenn ein Spieler mehrere Warpfelder kontrolliert, kann er von einem eigenen Warpfeld aus auch Ziele neben den anderen eigenen Warpfeldern erreichen. Eine Verstärkung oder ein Bau auf dem Warpnetz wirkt auf alle betreffenden eigenen Warpfelder, Münzkosten fallen pro Feld an.

**Bauen:** Fünf Gebäude verfügbar, **maximal eines pro Feld**. «Bauen» drücken und ein eigenes Feld wählen, oder erst ein eigenes Feld wählen und danach «Bauen» drücken. Das Baumenü zeigt Effekt und Preis. Der Bau kostet nur Münzen, keine Kampfaktion.

| Gebäude | Wirkung | Münzen |
| --- | --- | ---: |
| 🛡 Festung | +3 Verteidigung auf dem Feld | 4 |
| ⚔ Kaserne | Angriffe vom Feld verbrauchen keine eigene Stärke | 6 |
| 🔮 Machtzentrum | +2 Angriff für benachbarte eigene Felder | 7 |
| 💠 Schildgenerator | +2 Verteidigung für benachbarte eigene Felder | 7 |
| 🏹 Wachturm | Kann in gerader Linie über zwei Felder angreifen | 6 |

## Siegbedingungen

1. **Drei der vier Ecken** gleichzeitig kontrollieren, sofortiger Sieg.
2. **Gegnerisches Hauptquartier** erobern, sofortiger Sieg.
3. Falls bis zum Ende von **30 Runden** niemand gewinnt, gewinnt die Seite mit der grösseren **Gesamtstärke** aller eigenen Felder. Keine separaten Siegpunkte.

## Technik und Bedienung

HTML, CSS, Vanilla JavaScript ohne externe Frameworks. Hochformat-Layout, Touch-Steuerung, responsive Kacheln, Feld-Informationsanzeige und optionaler Ton. Die fünf Bauelemente sind einmalige Spezialisierungen, keine ausbaubaren Stufen. Das Spielbalancing ist noch ein Prototyp.
