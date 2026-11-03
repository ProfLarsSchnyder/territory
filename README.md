# Territory Clash 🎮

Ein mobiles Strategiespiel mit KI und lokalem Zweispielermodus. Komplett ohne Framework, der Spielcode liegt in `index.html`.

## Online spielen

GitHub Pages in **Settings → Pages → Deploy from a branch → main / (root)** aktivieren.

Nach der Veröffentlichung: https://proflarsschnyder.github.io/territory/

## Aktuelles Regelwerk

- **Runden**: Blau beginnt die Partie mit 1 Kampfaktion, danach erhalten Rot und Blau abwechselnd jeweils 2 Kampfaktionen pro Zug.
- **Kampfaktionen**: Ein angrenzendes neutrales Feld erobern oder ein angrenzendes schwächeres gegnerisches Feld angreifen. Nur diese Aktionen zählen zum Zuglimit. Nach Verbrauch aller Kampfaktionen erfolgt automatisch der Spielerwechsel.
- **Stärke**: Jedes Feld besitzt eine Stärke. Beim Angriff muss die Stärke des Angreifers diejenige des Ziels übertreffen. Der Angreifer verliert 1 Stärke, das eroberte Feld beginnt mit Stärke 1.
- **Münzen**: Beide starten mit 8 Münzen und erhalten ab ihrem nächsten Zug 2 Münzen Grundeinkommen je Zug. Münzen sind die einzige Ressource.
- **Verstärken**: Eigenes Feld auswählen, dann **Verstärken**. Jede Verstärkung kostet 2 Münzen und gibt +1 Stärke. Es gibt weder ein Stärkelimit noch ein Limit für solche Käufe je Zug, nur der Münzvorrat begrenzt sie.
- **Mine (⛏)**: Bringt jede eigene Runde Münzen, anfänglich 1 pro Zug. Die Mine kann bis Stufe 4 ausgebaut werden. Kosten für die Stufen 2, 3, 4: 3, 5, 8 Münzen. Der Ausbau verbraucht keine Kampfaktion.
- **Schatz (✦)**: Bringt bei der ersten Eroberung 5 Münzen, unabhängig davon, wer ihn zuerst entdeckt. Anschliessende Rückeroberungen zahlen nicht erneut.
- **Sieg**: Wer das gegnerische Hauptquartier erobert, gewinnt sofort. Ansonsten gewinnt nach 15 Runden die Seite mit der höheren **Gesamtstärke** (Summe aller eigenen Feldstärken). Gleichstand ergibt Unentschieden. Keine separaten Siegpunkte.

## Spielmodi

- Gegen die einfache KI
- Zwei Spieler auf demselben Handy

## Noch in Diskussion, nicht implementiert

Baubare Upgrades: Festung, Kaserne, Machtzentrum, Schildgenerator und ein noch auszuwählendes Reichweitenupgrade. Weitere Spezialfelder werden erst nach der Auswahl ergänzt.

## Technik

HTML, CSS, Vanilla JavaScript. Mobile-First im Hochformat mit Touch-Steuerung.
