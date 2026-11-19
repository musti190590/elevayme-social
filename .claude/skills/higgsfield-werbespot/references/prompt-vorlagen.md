# Prompt-Vorlagen

Prompts auf **Englisch** schreiben, weil die Modelle das am zuverlässigsten umsetzen. Erklärungen für den Nutzer auf Deutsch.

Aufbau jedes Prompts: **Subjekt → Aussehen/Material → Umgebung → Licht → Kamera/Optik → Stil → Ausschlüsse.**
Konkrete, sichtbare Details statt Adjektive: nicht „schön“, sondern „matte sage-green linen shirt, sleeves rolled to the elbow“.

## Charakter-Sheet

```
Character reference sheet, three views on one canvas, plain neutral mid-grey studio background (#808080), soft even studio light, no harsh highlights.
Left: tight close-up portrait of the face, neutral-to-[EMOTION] expression.
Middle: full body, front view, standing relaxed, arms at sides.
Right: full body, back view.
Subject: [AGE]-year-old [GENDER/ETHNICITY], [HAIR: colour, length, style], [SKIN: natural texture, visible pores, light freckles], [BUILD].
Wearing: [TOP: colour, material, fit], [BOTTOM], [SHOES], [ACCESSORIES].
Photorealistic, 85mm lens, natural skin, no retouching, no makeup glow, consistent outfit across all three views.
No text, no labels, no watermark.
```
Modell: Soul Cinema · 16:9 oder 3:2 · 4–6 Varianten

## Location (3/4-Winkel)

```
Empty interior of [ROOM], photographed from a three-quarter angle showing two walls and the floor, so the full spatial layout is readable.
Details: [FURNITURE, MATERIALS, PROPS IN SCENE, CLUTTER LEVEL].
Lighting: [TIME OF DAY], [LIGHT SOURCE e.g. warm window light from camera left], [COLOR MOOD].
Photorealistic, 24mm lens, eye level, natural imperfections, lived-in.
No people, no text, no logos.
```
Modell: Soul Location oder Nano Banana Pro · Format = Endformat. Folge-Location mit der ersten als Referenz: „same apartment, same materials and color palette as the reference“.

## Prop / Produkt

```
Product shot of [OBJECT], [MATERIAL, FINISH, COLOR], [SIZE CUE], isolated on plain light-grey background, soft box lighting, subtle reflection, accurate proportions, sharp edges.
[If real product: match the attached reference photo exactly, keep shape, buttons, colors.]
No added logos, no text unless specified.
```

## S/W-Storyboard-Frame

```
Black and white storyboard frame, clean pencil-and-grey-wash sketch style, [ASPECT] composition.
Shot: [SHOT SIZE + ANGLE]. [CHARACTER brief description] [ACTION frozen at its key moment] in [LOCATION brief].
Camera: [MOVE as arrow note]. Clear silhouette, readable staging, no fine detail.
```
Modell: Nano Banana 2 · 1k

## Startframe (Komposition)

```
Using the references: @[CHARACTER] (character sheet), @[LOCATION], @[PROP].
Photorealistic still, [ASPECT]. [SHOT SIZE + ANGLE]. @[CHARACTER] [POSE/ACTION start position] in @[LOCATION], [PROP placement].
Lighting matches the location reference: [LIGHT]. [LENS]. Keep face, hair and outfit exactly as in the character sheet.
No text, no logos.
```

## Video-Shot

```
[ASPECT], [DURATION]s, [SHOT SIZE + ANGLE].
Identity: @[CHARACTER] as in the start frame, same outfit and hair. Location: @[LOCATION].
Action (in order):
1. [BEAT 1, physical and specific]
2. [BEAT 2]
3. [BEAT 3 – end position that cuts into next shot]
Acting: [EMOTION ARC, e.g. starts tense, jaw tight → glances at phone → shoulders drop, small relieved exhale, half smile]. Natural, understated, no exaggerated gestures, no talking to camera unless stated.
Camera: [ONE MOVE, e.g. slow push-in], stable, realistic handheld micro-shake [optional].
Light: [LIGHT], consistent with start frame.
Sound: [AMBIENCE, SFX]. [No dialogue / Line: "…"].
Avoid: morphing hands, extra fingers, glowing teeth, flickering clothes, changing outfit, readable text, logos.
```
Modell: Seedance 2.0 (Start-Image + Referenzen) · Test 720p, final 1080p

## Packshot

```
[ASPECT], 4s. Final product/brand shot. [SUBJECT] centered in the lower-middle third, clean background [COLOR].
Camera: very slow push-in for 2 seconds, then holds completely still for the last 2 seconds.
Soft premium light, no people moving, no text (added in edit).
```

## Detail-Fix (Frame-Grab)

```
Edit only the masked area: [WHAT IS WRONG] → [WHAT IT SHOULD BE].
Keep everything else pixel-identical: face, lighting, framing, colors.
```
Modell: Nano Banana 2 mit `is_inpaint` + Maske, sonst Nano Banana Pro mit Referenz. Der korrigierte Frame wird zum neuen Startframe.

## Produktbedienung (Beispiel)

Schlecht: „She uses the app.“
Gut: „She holds the phone in her right hand at chest height, taps the green notification at the top of the screen with her thumb, the screen slides to a calendar view, she nods once.“
