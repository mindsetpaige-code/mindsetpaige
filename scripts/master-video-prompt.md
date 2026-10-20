# Velvet Reel Studios — Master Video Prompt

Turns a finished script into a complete, shot-by-shot production pack: character sheets, location sheets, image prompts, video (motion) prompts, and voice direction. Tool-agnostic — works for any image generator (Midjourney, Flux, Nano Banana, Ideogram, etc.) and any image-to-video tool (Kling, Veo, Runway, Hailuo, etc.).

Copy everything inside the block. Fill in the [BRACKETS]. Paste your script at the bottom.

```
You are the director, cinematographer, and AI production lead for VELVET REEL STUDIOS, a YouTube channel that releases feature-length, photorealistic AI-generated cinematic dramas ("THE COMPLETE MOVIE") with an all-Black cast. Turn the script below into a complete, shot-by-shot production pack I can feed directly into image and video generators.

=== MY INPUTS ===
IMAGE TOOL: [e.g. Midjourney / Flux / Nano Banana — or "generic"]
VIDEO TOOL: [e.g. Kling / Veo / Runway — or "generic"]
CLIP LENGTH: [default 5 seconds]
ASPECT RATIO: [default 16:9]
SCENES TO PROCESS: [e.g. "Scenes 1–10" or "all"]

=== VISUAL STYLE PROFILE (apply to every frame) ===
- Art style: photorealistic cinematic film still, premium streaming-drama look, glossy and polished but natural skin texture. Never cartoon, never illustration.
- Palette: warm espresso browns, deep chocolate, black; amber, honey gold, candlelight orange; burgundy/wine-red accents for tension and romance; champagne and rose-gold for luxury; muted teal city-night windows used sparingly. Rich, warm skin tones — never washed out or gray.
- Lighting: low-key interiors lit by warm practicals (lamps, sconces, candles, stained glass); soft 45° key with gentle falloff; golden-hour window light for intimacy and hope; cooler, harsher light for confrontation; subtle rim light separating subjects from dark backgrounds; bokeh city lights at night.
- Camera: cinema camera look (ARRI Alexa), 35mm / 50mm / 85mm primes, shallow depth of field, subtle anamorphic feel.
- Composition: rule of thirds, faces always clearly lit; couples framed with negative space that shrinks as intimacy grows; doorways, windows, and pews as framing devices; a foreground object for depth.
- Mood: emotionally heightened, intimate, warm melodrama. Dark scenes keep one warm light source — hope is always in frame.

STYLE ANCHOR (append to the end of EVERY image prompt, word for word):
"Photorealistic cinematic film still, premium African American drama, shot on ARRI Alexa, [LENS] prime lens, shallow depth of field, warm amber and espresso color grade with burgundy and gold accents, soft directional key light, subtle film grain, rich warm skin tones, highly detailed, [ASPECT RATIO]."

=== STEP 1 — CHARACTER LOCK SHEET ===
For every speaking character, write one fixed description block (age, skin tone, face shape, hair, build, signature wardrobe per act, one signature accessory). Then write a CHARACTER REFERENCE PROMPT for each: front-facing portrait, neutral expression, plain warm-gray backdrop, soft studio light, plus the style anchor — so I can generate one reference image per character and reuse it.
RULE: In every later prompt, paste the character's FULL description block. Never write just a name.

=== STEP 2 — LOCATION LOCK SHEET ===
For every location, write one fixed description block (architecture, materials, colors, key props, light sources, time of day variants). Reuse it word for word in every prompt set there.

=== STEP 3 — SHOT LIST (the main job) ===
Break the script into BEATS. Each beat = one clip of [CLIP LENGTH] seconds max (≈ 8–14 spoken words). Do not skip, merge, or summarize any line of the script. Long lines are split across multiple beats. Silent moments, [music] tags, and reactions also get beats.

For EACH beat output exactly this:

BEAT [scene#].[beat#]
SCRIPT: "[exact script text covered by this beat]"
SPEAKER: [name or "none"]
SHOT: [establishing wide / wide / medium / medium close-up / close-up / extreme close-up / over-the-shoulder / two-shot / insert]
LENS: [35mm / 50mm / 85mm]
IMAGE PROMPT: [fully standalone paragraph: full character description block(s) + exact wardrobe + pose + facial expression + action + full location block + lighting + mood + camera angle + style anchor. Must make sense with zero context from other beats.]
VIDEO PROMPT: [motion only, for image-to-video: subject movement, facial micro-expression, camera move (slow push-in / slow pull-out / gentle handheld / slow pan / static / orbit), environment motion (candle flicker, curtains, rain, city lights), speed ("slow, subtle, cinematic"), duration in seconds. If someone speaks, include: "[name] speaks with natural lip movement." End with: "Maintain face and wardrobe consistency, no morphing, no extra people, no text."]
VOICE: [line to be voiced, emotion, delivery note — e.g. "hurt, quiet, slight crack on 'fifteen years'"]
SFX/MUSIC: [ambient sound, score cue, or "none"]

=== SHOT GRAMMAR RULES ===
- Open every scene with a 1-beat establishing shot (exterior or wide) unless it continues directly from the previous scene.
- Dialogue: alternate medium close-up on the speaker with reaction close-ups on the listener. Use over-the-shoulder for arguments. Use two-shots for intimacy and banter.
- Emotional peaks (confessions, slaps, proposals, reveals): extreme close-up on eyes or hands, slow push-in.
- Power/antagonist moments: low angle on the antagonist, high angle on the victim.
- Use insert shots for key props (receipt, phone screen, ring, hymnal, binder) — these are where plot information lives.
- Never repeat the same shot type more than 3 beats in a row.
- Keep wardrobe identical within a scene; change it only when the script moves to a new day.
- Lighting follows emotion: warm/golden for love and healing, cooler and contrasty for conflict, burgundy accents for betrayal.
- CTA lines: write a single beat showing the channel logo card (rose-gold "VR" monogram on espresso-brown film-grain background) with slow push-in; voice line = the CTA text.

=== STEP 4 — THUMBNAIL & TITLE CARD ===
- 1 title-card prompt: movie title in large ornate gold serif with "A VELVET REEL STUDIOS ORIGINAL" in small spaced caps, over a moody ensemble or key-art image.
- 1 end-card prompt.

=== OUTPUT ORDER ===
1. Character Lock Sheet + reference prompts
2. Location Lock Sheet
3. Shot list, scene by scene, beat by beat
4. Title card + end card
5. Totals: number of beats, estimated runtime (beats × clip length)

=== FINAL CHECK BEFORE YOU FINISH ===
- Every line of the script appears in a SCRIPT field. Nothing skipped.
- Every IMAGE PROMPT is standalone, includes full character and location blocks, and ends with the style anchor.
- No beat exceeds [CLIP LENGTH] seconds of dialogue.
- No visual element contradicts the lock sheets.

If the output is too long, stop at the end of a complete scene and write: "Type CONTINUE for Scene [N]." Do not summarize to save space.

=== SCRIPT ===
[PASTE FULL SCRIPT HERE]
```

## Workflow tips

1. **Generate character reference images first.** Use them as image references in every shot (Midjourney `--cref`, Flux/Nano Banana reference image, Kling "Elements") — this is what keeps faces consistent across a 60-minute film.
2. **Batch by scene, not by beat.** Same location + same wardrobe in one session = fewer continuity errors.
3. **Lip-sync:** generate the voice line first (ElevenLabs or similar), then run the clip through your video tool's lip-sync feature, or a dedicated lip-sync tool.
4. **Feature-length scripts:** run the prompt with `SCENES TO PROCESS: Scenes 1–8`, then 9–16, and so on. Keep the Lock Sheets from the first run and paste them back in at the top of each later run.
5. **Assembly:** edit clips in order of BEAT numbers, lay the voice track, add score under every [music] tag, and drop the logo-card beats where the CTA lines sit.
