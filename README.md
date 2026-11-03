# Territory Clash 🎮

Ein schnelles, kostenloses Handy-Strategiespiel mit taktischem Raster und Neon-Optik. Komplett ohne Framework oder externe Abhängigkeiten. Der gesamte Spielcode liegt in `index.html`.

## Online spielen mit GitHub Pages

1. Im Repository **Settings → Pages** öffnen.
2. Unter **Build and deployment** die Quelle **Deploy from a branch** wählen.
3. Branch **main**, Ordner **/(root)**, danach **Save**.
4. Sobald GitHub Pages veröffentlicht hat, ist das Spiel unter **https://proflarsschnyder.github.io/territory/** erreichbar.

Du kannst `index.html` auch direkt in einem Browser öffnen.

## Regeln

- **Erobern**: Eigenes Feld wählen, dann ein angrenzendes neutrales Feld antippen. Kosten: 1 Aktion.
- **Angreifen**: Ein eigenes Feld wählen, Angriff aktivieren, schwächeres feindliches Nachbarfeld antippen. Das eigene Feld verliert 1 Stärke, das eroberte Feld erhält Stärke 1.
- **Verstärken**: Ausgewähltes eigenes Feld um 1 Stärke erhöhen, maximal Stärke 5. Kosten: 1 Aktion.
- **Zugfolge**: Blau macht zu Spielbeginn genau 1 Aktion, danach Rot 2 Aktionen. Anschliessend machen beide abwechselnd genau 2 Aktionen. Jeder Zug endet automatisch nach der letzten Aktion.
- **Kraftfelder (ϟ)**: Wer ein neutrales Kraftfeld erobert, erhält dieses direkt mit Stärke 2 statt 1. Kraftfelder geben keine weiteren Aktionen.
- **Sieg**: Gegners Hauptquartier erobern oder nach 15 Runden mehr Felder kontrollieren. Bei Gleichstand entscheidet die Summe der Feldstärken.

## Spielmodi

- Gegen die KI
- Zwei Spieler am gleichen Handy

## Technik

Reines HTML, CSS und JavaScript, Touch-Bedienung, skalierbares Hochformat und kleine Soundeffekte. Das Balancing und die KI können nach ersten Testspielen weiter angepasst werden.
