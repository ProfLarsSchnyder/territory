# Territory Clash 🎮

Mobile-First Strategiespiel in einer einzigen `index.html`. Spielbar gegen KI oder zu zweit an einem Handy.

## Spielen

GitHub Pages unter **Settings → Pages → Deploy from a branch → main / (root)** aktivieren.

Danach: https://proflarsschnyder.github.io/territory/

## Die wichtigsten Regeln

**Kampfaktionen:** Blau beginnt mit **1** Eroberung oder Angriff. Danach hat jeder Spieler pro Zug **2** Kampfaktionen. Eine **Eroberung eines neutralen Felds** verbraucht 1 Kampfaktion. Ein **erfolgreicher Angriff** setzt die dafür eingesetzte Kampfaktion unmittelbar zurück (**Reset**), sodass erfolgreiche Angriffe hintereinander möglich sind, solange noch ausreichende Stärke und erreichbare Ziele vorhanden sind. Es gibt keine zusätzliche Kettenangriffsaktion. Sobald alle Kampfaktionen verbraucht sind, bleibt der Spieler am Zug und kann weiterhin mit Münzen bauen und verstärken. **Nur der Button «ZUG BEENDEN» wechselt den Spieler.** Die KI beendet ihre Züge selbst.

**Stärke und Münzen:** Eigene Felder lassen sich für 2 Münzen um +1 Stärke verstärken, ohne Stärkeobergrenze und ohne Kampfaktionskosten. **Wandernde Stärke:** Erobert ein Feld mit Stärke 5 ein neutrales Feld, bleibt das Ausgangsfeld bei Stärke 1, das neue erhält Stärke 4. Bei Angriffen reduziert die gegnerische Verteidigungsstärke die ankommende Stärke: Stärke 5 gegen Verteidigung 2 ergibt ein neues Feld mit Stärke 3 und das Ausgangsfeld bleibt bei 1. Voraussetzung für einen Angriff ist höhere effektive Angriffsstärke als die Verteidigung. Ein Ausgangsfeld mit Stärke 1 kann weiterhin expandieren, dabei bleiben beide Felder auf 1. Bonuswerte sind direkt auf den Kacheln sichtbar (⚔ orange, 🛡 türkis, beide violett).

**Goldminen ⛏:** Die einzige Spezialfeldart mit ausbaubaren Stufen. Pro Stufe gibt es 1 Münze pro eigenem Zug. Upgrade-Kosten steigen: **3, 6, 10, 15, 21, ... Münzen**. Minen können über das Feld-Auswahlmenü aufgewertet werden, ohne Kampfaktion. Keine feste Stufenobergrenze.

**Schatzfelder 🪙:** Die erste Eroberung bringt einmalig 5 Münzen. Anschliessende Rückeroberungen bringen nichts.

**Warpfelder 🌀:** Vier neutral gelegene Warpfelder bilden für jede Fraktion ein Netzwerk. Wenn ein Spieler mehrere Warpfelder kontrolliert, kann er von einem eigenen Warpfeld aus auch Ziele neben den anderen eigenen Warpfeldern erreichen. **Ein Verstärken aller eigenen Warpfelder kostet insgesamt nur 2 Münzen**, auch wenn drei oder vier Felder verbunden sind. Gebäude werden auf freie eigene Warpfelder gespiegelt; dafür gelten weiterhin die ausgewiesenen Gebäudekosten pro bebautem Feld.

**Bauen:** Fünf Gebäude verfügbar, **maximal eines pro Feld**. «Bauen» drücken und ein eigenes Feld wählen, oder erst ein eigenes Feld wählen und danach «Bauen» drücken. Das Baumenü zeigt Effekt und Preis. Der Bau kostet nur Münzen, keine Kampfaktion.

| Gebäude | Wirkung | Münzen |
| --- | --- | ---: |
| 🛡 Festung | +3 Verteidigung auf dem Feld | 4 |
| ⚔ Kaserne | Angriffe von diesem Feld verlieren 1 Stärke weniger durch gegnerischen Widerstand | 6 |
| 🔮 Machtzentrum | +2 Angriff für benachbarte eigene Felder | 7 |
| 💠 Schildgenerator | +2 Verteidigung für benachbarte eigene Felder | 7 |
| 🏹 Wachturm | Kann in gerader Linie über zwei Felder angreifen | 6 |

## Siegbedingungen

1. **Drei der vier Ecken** gleichzeitig kontrollieren, sofortiger Sieg.
2. **Gegnerisches Hauptquartier** erobern, sofortiger Sieg.
3. Falls bis zum Ende von **30 Runden** niemand gewinnt, gewinnt die Seite mit der grösseren **Gesamtstärke** aller eigenen Felder. Keine separaten Siegpunkte.

## Technik und Bedienung

HTML, CSS, Vanilla JavaScript ohne externe Frameworks. Hochformat-Layout, Touch-Steuerung, responsive Kacheln, Feld-Informationsanzeige und optionaler Ton. Die fünf Gebäude sind einmalige Spezialisierungen, keine ausbaubaren Stufen. Aktuell sind drei Spezialfeldtypen festgelegt: Goldmine, Schatzfeld und Warp. Zwei weitere Spezialfeldtypen sind noch offen. Das Spielbalancing ist noch ein Prototyp.
