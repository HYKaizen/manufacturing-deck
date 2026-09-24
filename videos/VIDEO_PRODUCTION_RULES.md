# VIDEO PRODUCTION RULES — Prowiso / Yellow Belt Series
# Non-negotiable standards for ALL episodes. Do NOT deviate.

## Voice & TTS
- **Model:** `eleven_multilingual_v2`
- **Voice ID:** `eJWQWZhpuvfzqwHiQBK2`
- **Settings (F):** `{"stability": 0.40, "similarity_boost": 0.60, "style": 0.50, "use_speaker_boost": true}`
- **Slowdown:** `atempo=0.88` (12% slower for comfortable pace)
- **Naming:** "I'm Hakan" — NEVER "I'm Hakan Yasar" in speech
- **Slides/visuals:** "Hakan Yasar — HY Kaizen Consulting" is fine on screen

## Speaking Style
- **Üzerine basa basa anlat** — like a teacher emphasizing key points, not rushing
- Natural, conversational — NOT robotic or textbook
- Contractions, rhetorical questions, real-world anecdotes
- "Here's the thing...", "Let me give you an example...", "And this is important..."
- Mix short punchy sentences with longer explanatory ones
- **Sınıf havası:** Ask questions, pause, answer yourself
  - "Let me ask you something... [question] ... Take a moment... The answer is..."
- Repeat/emphasize critical concepts: "And I want to be clear about this..."
- **NEVER rush.** Quality and comprehension > brevity. Episodes can be 10-15+ minutes if the content requires it.

## Episode References
- ✅ **Past references OK:** "As we discussed in Episode 3...", "Remember from the previous episode..."
- ✅ **Forward teasers OK:** "We'll cover this in more detail in a later episode", "İlerleyen bölümlerde daha detaylı ele alacağız"
- ❌ **Future episode NUMBERS forbidden:** NEVER say "In Episode 32 you'll learn..." (viewer hasn't been there yet)

## Slide Design
- **Dimensions:** 2666 × 1500 px (even width for libx264)
- **Colors:** Navy #1B3A5C, Teal #00A3B4, Orange #E8742A, White #FFFFFF
- **Font:** Helvetica (system)
- **Logo:** Square aspect ratio (750×750 source) — NEVER stretch/squash
- **Footer:** "Prowiso | HY Kaizen Consulting | Hakan Yasar"

### Slide Density Rules
- **Slides must be FULL** — no empty/sparse pages
- Every slide should have multiple visual elements: boxes, badges, bullets, color blocks
- **Minimum 10-12 slides per episode**
- Each slide = 30-90 seconds of audio (varies by content density)

### Slide Type Variety (rotate through these, NEVER all same layout)
1. **Intro slide** — dark gradient, episode badge, topic cards with icons
2. **Definition slide** — big teal box with term + definition, context below
3. **Comparison slide** — side-by-side columns (green/red, before/after, vs)
4. **Bullet slide** — with highlight box at top, orange bullet points
5. **Waste/concept card** — letter badge circle + definition + real example box + impact
6. **Question slide** — navy question box + answer cards below
7. **Acronym/overview slide** — items with colored badges, row layout
8. **Recap slide** — 4-5 items with problem + solution summaries
9. **Assignment/exercise slide** — numbered steps, teal action card
10. **Closing slide** — dark gradient, checkmark takeaways, next episode teaser

### Color Coding (consistent across ALL episodes)
- **Definitions/concepts:** Teal box/outline
- **Warnings/problems:** Orange or Red
- **Positive/solutions:** Green
- **Examples:** Light background box with colored border
- **Before:** Red-tinted box | **After:** Green-tinted box
- **Questions:** Navy background box

## Video Assembly
- **NO black gaps between slides** — segments concat directly, no gap.mp4
- **Pipeline:** PIL → PNG slides → ElevenLabs TTS → atempo=0.88 → ffmpeg concat
- **ffmpeg encode:** `libx264 -tune stillimage -c:a aac -b:a 192k -ar 44100 -ac 2 -pix_fmt yuv420p -shortest`
- **Assert:** `len(slides) == len(scripts)` before ANY assembly — 1:1 mapping enforced
- **Output:** `/documents/EP{NN}_{slug}.mp4` + copy to WIP folder
- **Symlink:** to `kaizen-academy/public/videos/`

## Episode Structure (every episode)
1. **Intro slide** (30-40s) — warm welcome, context, what they'll learn
2. **8-10 content slides** (varied layouts, 40-90s each) — teaching with examples
3. **Closing slide** (40-60s) — key takeaways, next episode preview, "I'm Hakan"

## Content Rules
- Source material: Hakan's training PPTX speaker notes (`yb_full_notes.md`)
- Scripts must match slide visual content
- Real-world examples mandatory — factories, hospitals, offices, warehouses
- No generic filler — every sentence must teach something
- **No repetition across episodes** — if covered before, reference the episode
- **Minimum 5 minutes per episode** — no upper limit if quality demands more

## Delivery
- All videos → workspace + WIP folder + platform symlink
- DB: `is_published=1`, `video_path` set
- Quiz questions seeded per module
