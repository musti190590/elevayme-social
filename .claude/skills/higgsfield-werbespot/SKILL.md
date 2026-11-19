---
name: higgsfield-werbespot
description: Plant realistische KI-Werbespots für Higgsfield, von der Idee bis zum Schnitt. Zerlegt eine Idee in Storyboard und Shots, schreibt Prompts für Charakter-Sheets, Locations, Props und Video-Shots, plant Credits und prüft Ergebnisse auf typische KI-Fehler. Verwenden, wenn ein Werbespot, Reel, Ad oder Social-Video mit Higgsfield (Soul, Soul Cinema, Nano Banana, Seedance, Kling, Cinema Studio) entstehen soll, oder bei "Storyboard", "Shotliste", "Video-Prompts", "Higgsfield-Prompt", "Frame korrigieren".
---

# Higgsfield-Werbespot

Workflow nach dem Higgsfield-Tutorial „How I Get Perfect AI Realism in Every Shot (3 Steps)“: erst billig planen und testen, dann teure Video-Credits ausgeben.

Grundregel: **Kein Video-Credit, bevor Storyboard, Assets und Frames freigegeben sind.** Jede Phase endet mit einer Freigabe durch den Nutzer.

Referenzen (bei Bedarf lesen):
- `references/modelle-und-credits.md`: welches Modell wofür, Credit-Kosten, Budgetrechnung
- `references/prompt-vorlagen.md`: Prompt-Bausteine für Sheets, Locations, Props, Shots und Fixes
- `references/fehler-checkliste.md`: Prüfliste für generierte Bilder und Clips
- `references/elevayme-marke.md`: Marke, Zielgruppe und Look von Elevayme (für Elevayme-Spots immer lesen)

## Phase 0: Briefing

Hol die Idee so detailliert wie möglich ein. Spracheingabe ist ausdrücklich erwünscht, denn viel Detail ist besser als wenig.

Kläre nur, was fehlt:
1. Was wird beworben, und welche **eine** Botschaft soll hängen bleiben?
2. Zielgruppe und Plattform: 9:16 für Reels/TikTok, 16:9 für YouTube, 1:1 bzw. 4:5 für den Feed
3. Länge: Standard 15–20 s. Länger nur, wenn das Budget reicht (siehe Credit-Plan)
4. Tonalität: humorvoll, emotional oder clean-premium
5. Echte Produktfotos, Screens oder Logo vorhanden? Ohne Referenz erfindet die KI das Produkt.
6. Credit-Budget: Bei verbundenem Higgsfield-MCP mit `balance` prüfen.

Ergebnis: ein Absatz als **Creative Brief** (Botschaft, Hook, Story in drei Sätzen, CTA).

## Phase 1: Storyboard und Shotliste

Zerlege die Story in Shots von 3–8 s. Pro Shot gibt es genau eine Aktion. Für jeden Shot notierst du:

| Feld | Inhalt |
|---|---|
| Nr. / Dauer | z. B. S03 · 4 s |
| Zweck | Hook, Problem, Wendepunkt, Lösung oder Packshot |
| Einstellung | Totale, Halbnah, Nah oder Detail, plus Winkel |
| Kamera | statisch, Push-in, Schwenk, Handheld; nur **eine** Bewegung |
| Aktion | was physisch passiert, Schritt für Schritt |
| Acting | Emotion, Körpersprache, Mimik, Spannungsbogen im Shot |
| Licht / Farbe | Tageszeit, Lichtquelle, Farbstimmung |
| Assets | `@Name` des Charakters, der Location und der Props |
| Schnitt-Anschluss | welche Bewegung oder Blickrichtung in den nächsten Shot trägt |
| Ton | Atmo, SFX, Voiceover, Musik |

Regeln:
- **Hook in den ersten 1,5 s:** Bewegung, Konflikt oder eine überraschende Situation, kein Logo.
- **Durchgehende Bewegung an Schnitten:** Wenn eine Handlung über einen Schnitt läuft (Wischbewegung, Griff, Blick), beschreibe sie in beiden Shots, damit das Auge geführt wird.
- **Produktbedienung exakt beschreiben:** nicht „benutzt das Handy“, sondern „tippt mit dem Daumen auf die grüne Benachrichtigung oben, der Bildschirm wechselt zur Kalenderansicht“.
- **Packshot am Ende:** kleine Kamerabewegung, dann 1–2 s Stillstand. Marke und Text kommen im Schnitt als Overlay dazu, nicht aus dem Videomodell.
- Text, UI und Logos **nie** vom Videomodell rendern lassen. Sie kommen ins Overlay im Schnitt oder als korrigierter Startframe.

### Schwarz-Weiß-Storyboard (Pflicht vor Video)

Pro Shot ein günstiges Standbild als S/W-Skizze, damit Framing und Lesbarkeit geprüft werden. Vorlage: `prompt-vorlagen.md` → „S/W-Storyboard-Frame“. Ein günstiges Modell reicht (siehe Credit-Datei). Zeig dem Nutzer alle Frames als Raster und lass Framing, Reihenfolge und Lesbarkeit freigeben. Erst danach geht es weiter.

## Phase 2: Assets bauen und testen

Reihenfolge: Charakter → Locations → Props → Kombinationstest.

1. **Charakter-Sheet (Hero)**
   - Soul Cinema oder Soul 2.0, für realistische Haut statt Plastik-Look
   - **grauer Studiohintergrund** (verhindert Überstrahlung und Farbstiche)
   - **drei Ansichten auf einem Sheet:** Gesicht nah, Ganzkörper von vorne, Ganzkörper von hinten
   - Alter, Ethnie, Haar, Outfit mit Farben und Material, Schmuck, Grundemotion
   - 4–6 Varianten erzeugen, eine auswählen und als `@Name` benennen
2. **Locations** (Soul Location oder Nano Banana Pro)
   - im **3/4-Winkel**, damit das Videomodell den Raum versteht und bei Schwenks nichts erfinden muss
   - Licht und Farbwelt passend zum Storyboard
   - Folge-Locations mit der ersten Location als Referenz erzeugen, damit die Welt zusammenpasst
3. **Props und Produkt**
   - einzeln, auf neutralem Grund. Bei echten Produkten ein Foto als Referenz nehmen.
   - glänzende oder technische Objekte und alles mit Text: Nano Banana Pro bzw. GPT Image 2
4. **Kombinationstest:** Charakter in jeder Location als Standbild. Aussortieren bei künstlichem Licht, Farbstich, schwacher Ausstrahlung oder falschen Proportionen.
5. **Asset-Register** anlegen und ab jetzt in jedem Prompt verwenden:
   ```
   @Lena       – Charakter-Sheet v3 (Soul Cinema), Outfit: …
   @Werkstatt  – Location v2, 3/4-Winkel, Abendlicht
   @Handy      – Prop v1, Samsung-artig, ohne Logo
   ```

## Phase 3: Video-Shots

1. Pro Shot ein **Startframe**: Charakter + Location + Props kombiniert, im finalen Format. Das ist die wichtigste Stellschraube für Konsistenz.
2. Video-Prompt nach Vorlage `prompt-vorlagen.md` → „Video-Shot“. Erst Identität (wer, wo, wie sieht es aus), dann Bewegung (was passiert, in welcher Reihenfolge, Kamera).
3. **Testlauf günstig:** 720p bzw. die Fast- oder Mini-Variante, kürzeste sinnvolle Dauer, 1–2 Takes.
4. Prüfen mit `fehler-checkliste.md`.
5. **Fix-Schleife statt Neu-Würfeln:**
   - Fehler im Detail (Text, Outfitfarbe, Hand, Lenkrad, Beschriftung): Frame exportieren, nur diese Stelle im Bildmodell korrigieren, korrigierten Frame als neuen Startframe einspeisen
   - Fehler im Acting: Körpersprache und Spannungsaufbau genauer beschreiben, Emotion in Zwischenschritte zerlegen
   - Fehler in der Mechanik: Bedienung Schritt für Schritt beschreiben
   - Nach 3 Fehlversuchen: Shot vereinfachen (weniger Aktion, ruhigere Kamera) statt weiter zu würfeln
6. Erst der freigegebene Take wird in finaler Auflösung gerendert.

## Phase 4: Schnitt

- Pro Shot den besten Take aus allen Batches auswählen
- Reihenfolge laut Storyboard, Schnitt auf Bewegung
- Overlays: Logo, Claim, CTA, Untertitel (80 % schauen ohne Ton)
- Ton: Atmo, SFX, Musik, gegebenenfalls Voiceover
- Export im Plattformformat, Sicherheitsbereiche für die Reels-UI beachten (oben ca. 14 %, unten ca. 20 % frei lassen)

## Ausgabeformat

Lege pro Projekt einen Ordner `spots/<projektname>/` an mit:
- `brief.md`: Creative Brief
- `storyboard.md`: Shotliste und alle Prompts, nach Phase gegliedert
- `assets.md`: Asset-Register mit Status (offen / getestet / freigegeben)
- `credits.md`: geplante und verbrauchte Credits

Jeder Prompt steht in einem eigenen Codeblock, damit er sich direkt kopieren lässt. Über jedem Prompt stehen Modell, Seitenverhältnis, Dauer, Auflösung und geschätzte Credits.

## Ausführung über das Higgsfield-MCP

- Mit voller Higgsfield-Verbindung (Claude Desktop/Web): Vor jeder Generierung Modellschema mit `models_get` prüfen. Wenn möglich, Kosten vorab abfragen. Generierungen nur nach Freigabe des Nutzers starten, mit Angabe der Credits.
- Ist die Verbindung nur lesend (kein Generate-Tool sichtbar): Prompts ausgeben, der Nutzer generiert auf higgsfield.ai. Dort laufen auch die Gratis- und Unlimited-Kontingente, die per MCP **nicht** gelten.
