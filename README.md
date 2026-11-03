# Territory Clash 🎮

Ein Handy-Strategiespiel mit KI-Modus und lokalem Zweispielermodus. Ohne Framework, das Spiel läuft direkt in `index.html`.

## Auf dem Handy spielen

GitHub Pages unter **Settings → Pages → Deploy from a branch → main / (root)** aktivieren.

Adresse: https://proflarsschnyder.github.io/territory/

## Zugablauf

1. **Blau beginnt mit einer Kampfaktion.** Danach haben beide Seiten jeweils zwei Kampfaktionen pro Zug.
2. **Erobern und Angreifen** kosten je eine Kampfaktion. Erfolgreiche Angriffe geben **keine** Aktion zurück.
3. Auch bei **0 Kampfaktionen** kann man weiterhin für Münzen verstärken, Goldminen ausbauen und Gebäude bauen.
4. **Erst beim Tippen auf „ZUG BEENDEN“** ist der andere Spieler am Zug. Die KI beendet ihre Züge automatisch.

## Münzen und Feldstärke

- Münzen sind die einzige Ressource. Beide Seiten beginnen mit **8 Münzen**.
- Zu Beginn jedes weiteren eigenen Zuges erhält man **2 Münzen Grundeinkommen**, zusätzlich das Einkommen kontrollierter Goldminen.
- **Verstärken** kostet **2 Münzen** für +1 Stärke und verbraucht keine Kampfaktion. Die Feldstärke hat keine Obergrenze.
- Beim Angreifen muss die effektive Angriffsstärke die gegnerische Verteidigungsstärke **übertreffen**. Normalerweise sinkt die Stärke des Ausgangsfelds beim Angriff um 1, das eroberte Feld startet mit Stärke 1.
- Angriffsboni stehen auf den Spielfeldern **orange (⚔)**, Verteidigungsboni **hellblau (🛡)** und bei beiden Bonusarten ist die Stärke **violett**.

## Spezialfelder

Aktuell sind **3 von 5 geplanten Spezialfeldtypen** festgelegt und eingebaut:

- **⛏ Goldmine**: Produziert pro eigenem Zug Münzen entsprechend der Minenstufe. Nur Minen haben ausbaubare Stufen. Upgrade-Kosten steigen: **3, 6, 10, 15, 21 … Münzen** für die Stufen 2, 3, 4, 5, 6 usw. Keine feste Obergrenze.
- **✦ Schatzfeld**: Die erste Eroberung einer Schatzposition gibt einmalig **5 Münzen**.
- **🌀 Warpfeld**: Vier Positionen nahe der Kartenmitte. Alle eigenen Warpfelder bilden ein verbundenes Netzwerk. Beim Verstärken werden alle eigenen Warpfelder gleichzeitig verbessert, die Münzkosten fallen pro Feld an. Gebäude werden auf alle noch freien eigenen Warpfelder übertragen und pro Feld bezahlt.
- Zwei weitere Spezialfeldtypen werden später gemeinsam ausgewählt.

## Baubare Gebäude

Im Spiel sind **5 Gebäude**, jeweils maximal **1 Gebäude pro Feld**. Gebäude kosten Münzen, aber keine Kampfaktion:

| Gebäude | Preis | Effekt |
|---|---:|---|
| 🛡 Festung | 4 | +3 Verteidigung auf dem Feld |
| ⚔ Kaserne | 6 | Erfolgreiche Angriffe von diesem Feld kosten keine eigene Stärke |
| 🔮 Machtzentrum | 7 | +2 Angriff auf benachbarten eigenen Feldern |
| 💠 Schildgenerator | 7 | +2 Verteidigung auf benachbarten eigenen Feldern |
| 🏹 Wachturm | 6 | Angriffe auf 2 Felder Entfernung in gerader freier Linie |

Für die Gebäudeauswahl funktioniert **beide Reihenfolgen**: erst ein eigenes Feld, dann **Bauen**, oder zuerst **Bauen** und danach ein eigenes Feld antippen.

## Drei Siegbedingungen

- **3 Ecken**: Sobald jemand gleichzeitig drei der vier Eckfelder kontrolliert, gewinnt diese Seite sofort.
- **Hauptquartier**: Die Eroberung der gegnerischen Basis beendet das Spiel sofort.
- **Nach 30 Runden**: Wenn noch niemand gewonnen hat, zählt ausschliesslich die gesamte Stärke aller eigenen Felder. Bei Gleichstand endet die Partie unentschieden.

## Technik

HTML, CSS und JavaScript. Für schmale und kurze Handybildschirme optimiert, mit Infobereich für Spezialfelder, Touchsteuerung und animiertem Spielfeld. Das Balancing ist weiterhin im Prototyp-Stadium.
