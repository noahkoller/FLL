# LeagueSim

Web-App zum Simulieren von Fussball-Ligen. Oben im Header lässt sich zwischen den Ligen umschalten:

- **First Lego League (FLL)** — fiktive Liga mit 20 Teams (20er-Format: Hin-/Rückrunde, Playoffs, 2 Absteiger)
- **Schweizer Super League (SSL)** — 12 Teams im echten Schweizer Modus (Dreifachrunde + Meister-/Abstiegsrunde-Split + Barrage)

Jede Liga speichert ihre Ergebnisse getrennt. Ein Wechsel oben behält die jeweiligen Daten.

## Ligen im Detail

### First Lego League (20 Teams)

- **Tabelle** — berechnet sich automatisch aus den Ergebnissen. Farbzonen mit Legende:
  - Champions League (Platz 1–5, blau)
  - CL-Playoff (Platz 6–7, hellblau)
  - Abstiegs-Playoff (Platz 18, hellrot)
  - Abstieg (Platz 19–20, rot)
- **Spielplan** — komplette Hin- und Rückrunde (38 Spieltage, 380 Spiele) plus zwei Playoff-Spieltage am Saisonende (Hinspiel / Rückspiel), die als normale Spiele auftauchen. Spieltag-Wechsel per Pfeil ‹ ›. Ergebnisse eintragen, spielen oder simulieren — die Tabelle aktualisiert sich sofort. Playoff-Spiele zählen nicht für die Ligatabelle, aber für die Torschützen. Die Playoff-Paarungen (6. vs. 7. und 18. vs. 3. der 2. Liga) ergeben sich automatisch aus der Tabelle; den Namen des 2.-Liga-Gegners trägst du direkt beim Playoff-Spieltag ein. Auf schmalen Bildschirmen (Hochformat) werden statt der vollen Teamnamen die Kürzel neben den Logos gezeigt.
- **Torschützenliste** — wird automatisch aus allen Ergebnissen berechnet (Liga und Playoffs, simuliert wie selbst gespielt). Die Tore jedes Spiels werden auf die drei Kaderspieler des Teams verteilt; offensivere Trikotnummern treffen häufiger. Gleiche Ergebnisse ergeben immer dieselben Torschützen — die Liste ändert sich nur, wenn ein Resultat geändert wird.
- **Mini-Game** — neben jedem Spiel im Spielplan startet ein ▶-Knopf ein kleines Fussballspiel im Club-Legend-Stil: Top-down-Ansicht, Spieler als Punkte mit Trikotnummer und Name. Vor dem Anpfiff wählst du, welches der beiden Teams du selbst steuerst — das andere übernimmt der Computer. Ziehen/Tippen bewegt den aktiven Spieler, um den Ball ins Tor zu schiessen. Über **Ergebnis übernehmen** wandert der Endstand direkt in Tabelle und Spielplan (korrekt der Heim/Auswärts-Seite zugeordnet). Jedes Team hat 3 Spieler im Kader. Die Gegner-Schwierigkeit richtet sich nach der Team-Stärke (gute Teams spielen etwas stärker), bleibt aber bewusst einsteigerfreundlich.
- **Simulation** — der ⚄-Knopf neben jedem Spiel würfelt ein plausibles Ergebnis anhand der Team-Stärken (gut / mittel / underdog) plus kleinem Heimvorteil. Über **Ganzen Spieltag simulieren** lässt sich der komplette Spieltag auf einmal berechnen. Überraschungen sind eingebaut — auch ein Underdog kann mal gewinnen.

Team-Stärken: gut = FLC, BLC, GSF, VAT, SPF, NMC · mittel = RBB, FFS, NOR, SOU, UVAT, WTU, LNI, KEY · underdog = MID, PLT, NHT, FHV, FST, FCC.

### Schweizer Super League (12 Teams)
Echtes Schweizer Format:
- **Grunddurchgang**: 33 Spieltage — jedes Team spielt jedes andere dreimal.
- **Split nach Runde 33**: Die Liga teilt sich in **Meisterrunde** (Top 6) und **Abstiegsrunde** (Plätze 7–12). Die Punkte werden übernommen; jede Gruppe spielt noch 5 Runden.
- **Europa**: Platz 1–2 Champions League, Platz 3–4 Europa/Conference League (farbige Zonen).
- **Abstieg**: Platz 12 steigt direkt ab. Platz 11 spielt die **Barrage** (Hin-/Rückspiel) gegen den 2. der Challenge League.
- **Aufstiegskandidaten** (Barrage-Gegner wählbar): FC Winterthur, FC Rapperswil-Jona, Yverdon Sport FC.

Teams: Grasshopper Club Zürich, FC Zürich, FC Basel, Young Boys, FC Luzern, FC St. Gallen, Servette FC, FC Lausanne-Sport, FC Sion, FC Lugano, FC Vaduz, FC Thun. Stärkeverhältnisse orientieren sich an der aktuellen Realität (Basel/YB/Lugano/St. Gallen/Sion stark, GC/Vaduz eher Abstiegskampf).

**Hinweis zu den Logos**: Echte Vereins- und Ligalogos sind urheberrechtlich/markenrechtlich geschützt und dürfen nicht eingebettet werden. Die Schweizer Klubs nutzen daher schlichte, selbst erzeugte Kürzel-Badges in den jeweiligen Vereinsfarben. Die FLL-Logos sind deine eigenen und weiterhin eingebettet.


Alle Eingaben werden lokal im Browser gespeichert (localStorage) und bleiben nach dem Neuladen erhalten.

## Auf GitHub Pages veröffentlichen
Die Team-Logos sind direkt in die `index.html` eingebettet — du brauchst **nur diese eine Datei** hochzuladen, sonst nichts.

1. Neues Repository auf GitHub erstellen (z. B. `fll`).
2. `index.html` ins Repository hochladen.
3. Im Repository auf **Settings → Pages** gehen.
4. Bei **Source** den Branch `main` und den Ordner `/ (root)` wählen, dann **Save**.
5. Nach kurzer Zeit ist die App unter `https://DEINNAME.github.io/fll/` erreichbar.

## Struktur
```
index.html      → die komplette App inkl. eingebetteter Logos
logos/          → Original-Logos (optional, werden nicht mehr benötigt)
```
