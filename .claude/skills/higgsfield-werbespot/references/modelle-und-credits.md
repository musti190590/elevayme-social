# Modelle und Credits

Stand: Higgsfield-Preisseite und Modellkatalog, 19.11.2026. Preise ändern sich oft, deshalb vor größeren Läufen mit `models_list` / `models_get` bzw. auf higgsfield.ai/pricing gegenprüfen.

## Welches Modell wofür

| Aufgabe | Erste Wahl | Alternative | Warum |
|---|---|---|---|
| S/W-Storyboard-Frames | Nano Banana 2 (1k) | Seedream 5.0 Flash, Z Image | billig, schnell, Framing reicht |
| Charakter-Sheet | Soul Cinema | Soul 2.0 | realistische Haut, kein Plastik-Look |
| Locations | Soul Location | Nano Banana Pro | Räume im 3/4-Winkel |
| Produkt / glänzende Props | Nano Banana Pro | GPT Image 2 | Material, Reflexe, Text im Bild |
| Detail-Fix an Frames | Nano Banana 2 (Inpaint mit Maske) | Nano Banana Pro | lokale Korrektur, Rest bleibt gleich |
| Startframe (Komposition) | Nano Banana Pro (bis 14 Referenzen) | Seedream 4.5 | kombiniert Charakter, Location und Prop |
| Video-Test | Seedance 2.0 Mini / 2.0 Fast 720p | Kling 3.0 720p | günstig, Referenzen möglich |
| Video final | Seedance 2.0 / 2.5 (1080p) | Cinema Studio Video 3.0 | Identität konsistent, Referenzbilder, Ton |
| Werbespot aus Produkt per Klick | Marketing Studio Video | – | nur für schnelle UGC-Formate, wenig Kontrolle |

## Credit-Kosten (Auszug)

| Modell | Credits |
|---|---|
| Soul 2.0 | 0,12 / Bild |
| Soul (Cinema) | ~0,25 / Bild |
| Nano Banana 2 / Pro | 2 / Bild (Pro 4K: 4) |
| GPT Image 2 | 2 / Bild |
| Seedream 5.0 Flash | 0,5 / Bild |
| Seedance 2.0 Fast 720p | ~12 / 5 s |
| Seedance 2.0 720p / 1080p | ~22 / ~60 pro 5 s |
| Seedance 2.5 720p / 1080p | 35 / 80 pro 5 s |
| Kling 3.0 720p / 1080p | ~7 / ~8 pro 5 s |

**Wichtig:** Unlimited-Modelle und Gratis-Generierungen (z. B. 5.000 Soul-Gens im Plus-Plan) gelten **nur auf higgsfield.ai**, nicht über MCP oder CLI. Über MCP kostet jede Generierung Credits.

## Budgetrechnung (Faustregel)

```
Bilder:  (Shots × 2 S/W-Frames) + (Charakter 6) + (Locations 3 × 4) + (Props 4) + (Startframes Shots × 3) + Fixes 10
Video:   Shots × Dauer/5 × Credits pro 5 s × Takes (Test 2 + final 1)
Puffer:  +30 %
```

Beispiel: 20-s-Reel, 5 Shots à 4 s, Tests mit Seedance 2.0 Fast 720p, final Seedance 2.0 1080p:
- Bilder: ca. 60 Stück × 2 = ~120 Credits (über die Website mit Gratis-Soul deutlich weniger)
- Video-Tests: 5 × 2 Takes × ~12 = ~120
- Video final: 5 × ~60 = ~300, plus 1 Nachdreh pro Shot ≈ 600
- Summe mit Puffer: **~1.100 Credits**

Ein 60-s-Spot mit vielen Iterationen landet schnell bei 5.000–6.000 Credits. So viel hat auch der Creator im Tutorial verbraucht.
