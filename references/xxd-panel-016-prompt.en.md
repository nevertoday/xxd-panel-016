# Grain Field Riso — Full Prompt (English)

## Runtime complete-canvas contract — highest priority

- `TOP_BOTTOM` and `LEFT_RIGHT` default to one complete finished generation using the current source as a high-fidelity edit/reference input. Do not pre-split the job into photographic and design halves.
- Top-bottom keeps the faithful source in approximately the upper 50% and performs this style transformation below; left-right uses the faithful source in approximately the left 50% and the transformation on the right. Unify both regions through colour, light, rhythm, typography, and meaning.
- `DESIGN_ONLY` and `WALLPAPER_PACK` use the complete canvas while the source remains an invisible identity/content reference. Recompose every wallpaper separately for its device.
- `FINAL CANVAS` means the ratio/pixels of the whole finished artwork and must be explicitly resolved before generation; never apply source dimensions silently. `DESIGN FRAME` is used only if a failed complete-canvas retry triggers deterministic composition fallback.
- Retry a failed complete canvas once against the failed constraint only. Scripted composition is allowed only after that retry still fails, when pixel-identical source preservation is explicitly required, when the active route cannot realise the canvas, or for lossless pixel calibration.

Treat the uploaded image strictly as the sole source of content and as the original photograph. Each selected ordinary mode produces one independent image per photograph; wallpaper-pack produces four separate wallpaper files—phone, iPad, desktop, and watch—under a caller-locked `INDEPENDENT` or `LINKED` relationship. Never combine them into a collage, contact sheet, grid, or overview.

The caller locks one or more of four modes: photograph above and print below, photograph left and print right, one transformed print filling the canvas, and/or four separately recomposed device wallpapers. In every selected mode, the print derives from this photograph rather than becoming unrelated abstraction or a photo filter.

The **transformed design frame** means the lower panel in top-bottom, the right panel in left-right, and the full canvas in design-only or each wallpaper output.

## 0. Aesthetic motive and generation-medium lock

Mode and device dimensions may change placement and aspect ratio, never the 016 aesthetic motive. Every transformed frame must visibly express: **this exact photographed subject → one compressed recognizable anchor → one motion logic derived from its posture, light, or spatial relation → vast paper void → physical Riso/silkscreen texture → experimental art-book typography acting as spatial rhythm**.

If an unrelated photo could replace the source without materially changing the anchor, motion field, palette, or copy, the result is generic and must fail. Do not substitute universal rings, suns, waves, mountains, abstract motifs, decorative wallpaper, or empty paper texture for source-specific translation. Device safe areas may move elements but must not delete the anchor, motion logic, print texture, main title, or typographic hierarchy.

Generate and edit all visual assets with an available raster image-generation capability and deliver PNG bitmaps. “Flat,” “printmaking,” or “vector-like edge” describes appearance only, never the file format. Do not substitute SVG, HTML, CSS, Canvas, diagrams, hand-coded vector markup, or programmatic drawing. Judge availability by actual capability, not a provider name or one environment variable; a missing variable does not prove that authentication or image generation is absent. Capability checks may expose only sanitized status and must never read out, display, log, or leak secret values. Explicitly invoking this skill and supplying the source image and mode confirms use of any already configured raster route for this PNG task; do not ask again merely because the built-in tool is unavailable and execution moves to a compatible configured route. Report a limitation only after safe checks confirm that no usable raster route exists.

Treat every invocation as a new generation job by default. Even when source, mode, and dimensions match an earlier job, generate a fresh result in a new task directory. Historical outputs are never current sources or completion evidence. Accept only current user attachments, explicit paths, or earlier user-supplied sources explicitly identified by the current request. Never scan the Desktop, workspace, or this skill's output root to improvise a source; if the intended source is inaccessible, request it instead of auditing and returning an old result.

---

## 1. Roles of the input image

The uploaded image is the sole content source and serves two roles:

1. **Original photograph in paired modes.** Present it faithfully above in top-bottom or left in left-right. Preserve subject structure, real material texture, natural light and color atmosphere. Design-only and wallpaper-pack do not show the original.
2. **Information source for the transformed field.** Analyze the photograph's most recognizable **subject, contour, posture, and narrative relationship**: what the subject is, where it faces, what action it performs, where the light comes from, and how it sits in space. Reconstruct those relationships inside the transformed design frame.

Introduce no other image, scene, object, color, or symbol. Never carry a sample work's subject, palette, or composition into a new piece. The sole exception is a `LINKED` wallpaper pack: an approved anchor wallpaper from this same source may serve as the second visual reference for the other three devices, but only to lock family resemblance. The original photo remains the sole authority for subject, pose, relationship, color provenance, and narrative content.

---

## 2. Working method

Use this sequence:

**DECONSTRUCT → ANCHOR SELECTION → MOTION DERIVATION → RISO RECONSTRUCT**

This is neither style transfer, photo vectorization, nor tracing.

Complete the following internally, without outputting analysis text:

1. Find the **single** most recognizable subject in the photo; it becomes the visual anchor in the transformed design frame.
2. Determine its essential facts: contour, posture, facing, center of gravity, and its narrative relationship to space.
3. Derive **one** primary motion logic from the subject's own character — never bolt on an effect.
4. Remove surface texture, perspective detail, background noise, secondary objects, and all low-information ornament.
5. Rebuild with the fewest possible marks: **one subject · one motion · one enormous spatial relationship**.
6. Make the transformed design frame read first as a minimal print composition, and only on second glance evoke this particular photograph.

A **clear identity echo** must exist between the source photograph and transformed print: after seeing the photo, a viewer must instantly recognize the same subject in the design frame.

---

## 3. Photographic area — paired modes only

Keep the original photograph. Do not redraw, replace, stylize, or illustrate it. Skip this section in design-only and wallpaper-pack, where the source remains reference evidence only.

- Preserve subject structure, real texture, natural light, and the original color atmosphere.
- Allow only a **light** high-end grade: gentle contrast, controlled highlights, deepened shadow steps, unified color temperature, slight desaturation or purification of one dominant hue — an art-magazine and exhibition-print tonality.
- No heavy filters, HDR, hard posterization, cyber palettes, oversharpening, or skin smoothing.
- To fit the photographic frame (whose shape follows the mode and canvas chosen in section 9), the sky, ground, water, or environmental background **may be extended naturally** to complete the composition.
- Any extension must match the original light, grain, perspective, and color continuously, with no visible seam.
- Never stretch, squash, distort, warp, or alter the subject itself, and never crop aggressively into the subject just to satisfy a ratio.

---

## 4. Transformed print — the visual anchor

Extract the photograph's most recognizable **subject, contour, posture, and narrative relationship**, and rebuild it as surreal minimal printmaking.

Anchor rules:

- Compress the subject into **one** clear, restrained visual anchor, usually placed at **small scale** inside a large void.
- Default anchor width about **12%–26%** of the transformed design frame; height no more than **20%–30%** of that frame. Especially poetic images may go smaller, but never below recognizability.
- Keep only the essential contour and posture. Do not reproduce complex detail, surface material, facial features, patterns, window mullions, feathers, leaf veins, or mechanical structure.
- The anchor may be a solid mass, a pure contour line, or a halftone-filled silhouette — or a restrained combination — but **only one approach may dominate**.
- Anchor placement follows the photo's center of gravity and facing; it usually sits off the geometric center to create asymmetric tension. Do not default to centering.
- Never introduce a second subject of equal weight. Secondary elements exist only as tiny, nearly vanishing traces.

Adapt by subject type:

- **People:** one continuous, irregular silhouette with head, shoulders, and body joined; keep posture and facing; no faces, fingers, or clothing folds.
- **Animals:** keep the most recognizable outer contour and momentum (running, standing, wings open, turning back); no fur or eye detail.
- **Plants:** keep growth direction and branch rhythm; no internal leaf structure.
- **Architecture:** keep one to three identity cues (taper, arch, spire, layered rhythm, skyline contour); no masonry, windows, or ornamental members.
- **Objects:** keep two or three planar marks for recognition; no metallic highlights, volume, or internal structure.
- **Vehicles:** keep the overall silhouette and direction of travel; no lamps, grilles, or wheel-spoke detail.
- **Landscape:** compress into one or two irregular horizontal axes, or a single isolated landform mass, preserving scale relationships.

Preserve the **minimum necessary recognizability** rather than replicating the object.

---

## 5. Transformed print — the motion field

Translate the photograph's action, direction, light, or spatial relationship into a **dynamic field** unfolding around the anchor.

### 5.1 Motion logic (choose exactly one)

Let the subject's own character select **one** primary motion logic:

1. **Falling** — top to bottom; for dropping, drifting, hanging, diving, rain, snow, waterfall subjects.
2. **Rising** — vertically upward; for smoke, mist, birds, balloons, flame, growth.
3. **Flowing** — traveling along one lateral or diagonal direction; for wind, current, crowds, traffic, running.
4. **Radiating** — outward from a core; for light sources, bursts, blooms, sound, ripple origins.
5. **Ripple and echo** — irregular concentric waves or broken echoes; for still-but-present subjects, water surfaces, resonance, and looking-back narratives.

**Never stack multiple motions.** One image, one directional field.

### 5.2 Building the field

- Express movement with **abundant fine lines, broken trajectories, coarse halftone dots, and shifts in grain density**.
- Density gradient: denser, stronger, more overlapped near the core; progressively sparser and more broken toward the edges, finally dissolving into the void.
- The field must connect geometrically to the anchor or point at it unmistakably, so the eye reads "the motion comes from / goes to here."
- Lines may break, misalign, vary in weight, and carry slight handmade tremor. They must never form a regular grid or textbook radial burst.
- Grain may run off the canvas edge and be cropped, implying a field larger than the frame.
- No glow, volumetric light, lens flare, depth-of-field blur, 3D volume, drop shadow, or realistic reflection.

### 5.3 Scale contrast

Pursue a **minute subject, enormous void, and violent scale contrast**.

- Keep roughly **60%–78%** of the transformed design frame as clean void (it may hold extremely sparse grain trails, but must not be filled).
- Never enlarge the anchor or add elements just to fill the frame.
- Emptiness is the content: quiet, solitary, mysterious, poetic, faintly surreal.

---

## 6. Print texture and printmaking language

The transformed design frame must read as a **hand-printed artifact**, not a digital illustration.

Preserve:

- Silkscreen and Risograph character
- Coarse grain, halftone dots, paper fiber
- Uneven ink coverage, ragged edges, ink build-up and ink starvation
- Slight misregistration between color plates (roughly 0.5–2mm offset)

Value and depth must come from **halftone density, ink overprint, and bare paper** — never from ordinary gradients.

Strictly avoid: CG look, 3D rendering, realistic lighting, smooth digital illustration, soft gradients, clean vector edges, blend-mode effects, glassmorphism, cel-animation finish, generic AI art, and template feel.

---

## 7. Color system

Extract from the source photograph **the single most recognizable, most spirited dominant color**. Combine it with warm white / ivory / natural paper, plus a **small amount** of black, to form a strict **2–3 color** system.

- **One dominant color:** a hue that genuinely exists in the photo and carries its life. It may be purified and strengthened into something vivid and forceful, but never neon, fluorescent, or over-digital.
- **One paper ground:** warm white, ivory, or natural paper (for example #F4EFE4 / #F0EADC / #EFE8DA and neighbors), serving as the transformed-frame background and void.
- **Optional small black:** only for tiny anchor structure, broken lines, or key text. It must never become a second dominant color.

Rules:

- Total colors in the transformed design frame must not exceed three.
- Add no unsupported complementary hue, no second accent, no neon, no gradient.
- Build value with halftone density and ink overprint; the third visual color produced where two inks overlap is allowed and encouraged as authentic print behavior.
- The transformed-frame background must be continuous paper, which may carry fiber and slight unevenness — but no gradient, vignette, lighting variation, or banding.

---

## 8. Typography — experimental art-book micro-system

Build a restrained **experimental art-book micro-typography system**.

### 8.1 Copy mode and user priority

Copy has no silent default. Before generation, explicitly resolve source-derived automatic copy, user-supplied custom copy, or text-free output; automatic and custom copy also require a target language or locale. Lock a separate copy package for every photo using this priority:

1. **The user explicitly requests no copy, no text, or a purely visual result:** render no letters, characters, numbers, title, caption, or decorative pseudo-text anywhere.
2. **The user supplies finished wording:** preserve it verbatim without rewriting, translating, adding, or removing words; adapt only size, position, and typographic relationships.
3. **The user supplies a copy direction, theme, tone, or keywords:** write one definitive version to that direction without presenting alternatives.
4. **The user has not resolved copy mode or target language/locale:** stop before image generation and ask one concise preflight question offering automatic copy, custom copy, or text-free output; automatic/custom also require a language or locale. Never guess and continue.

For multiple photos, build an independent copy package for each one. A shared creative direction may govern the batch, but each photo still receives distinct source-aware wording unless the user explicitly requests identical copy.

Resolve copy locale separately from the language used to issue the command. For automatic or direction-led copy, use: **explicit target market/audience locale > explicit output language > language of the supplied direction or draft; if none is explicit, ask before generation**. Thus a Chinese instruction asking for a Japanese edition produces natural Japanese; a Korean-audience request produces natural Korean; a UK edition uses British English; and an Arabic edition uses natural Modern Standard Arabic unless the user names a regional variety. Never infer nationality, ethnicity, or audience language from a face, name, clothing, scenery, filename, metadata, or visible signage.

Localize by transcreation, not word-for-word translation: preserve the semantic core and moment of recognition, then rebuild it through native syntax, register, idiom, punctuation, and line breaking. Arabic uses natural Modern Standard Arabic unless a regional variety is requested, correct connected shaping, right-to-left reading order, Arabic punctuation, semantic line breaks, and deliberate bidirectional handling of embedded Latin text or numerals; reverse typographic flow and alignment without blindly mirroring the source-derived composition. Japanese uses natural contemporary wording, an appropriate kanji/kana balance, Japanese punctuation, and kinsoku-aware breaks. Korean uses natural contemporary wording, correct spacing, and intact Hangul syllable blocks without decorative pseudo-Hanja. UK English uses British spelling, vocabulary, punctuation, date conventions, and culturally natural understatement rather than American wording. Apply the same native-register principle to every other locale. Finished user copy remains verbatim; when it conflicts with a named target locale and translation/localization permission is unclear, ask one concise clarification.

Distinguish immutable finished copy from an editable direction or draft. Finished copy is the semantic authority: preserve it verbatim, understand its emphasis, turn, double meaning, addressee, and tone, then present it professionally through scale, position, void, line breaks, and its relationship to the motion field. Break lines by semantic phrase; never split a fixed expression, create a false ambiguity, or demote a crucial word into unreadable microtype. For a direction or draft, first lock audience, communication goal, mandatory wording, tone, and subtext, then refine only within the permission given. Ask one concise question only when ambiguity would materially change the message; otherwise take the most conservative faithful reading.

### 8.2 Semantic distillation and main title

In automatic-copy mode, distill **one extremely short title** from the photo's action, distance, state, mood, or metaphor in the audience's natural language. The 016 experimental-art-book identity comes from restraint, scale, and typographic relationships, not mandatory English. When the user supplies finished wording or a creative direction, obey the wording, target locale, and localization permission.

Before writing, make a private three-level reading:

1. **Literal fact:** the subject, action, direction, distance, light, or spatial relationship actually visible.
2. **Relational tension:** what is approaching, missing, waiting, holding, leaving, hovering, resisting, or echoing.
3. **Latent implication:** what the first two levels jointly suggest, without inventing biography, location, ownership, events, or feelings unsupported by the image.

Compress these levels into one private semantic core, then choose one restrained rhetorical hinge: precise naming, contrast, understatement, double meaning, or a slight reversal. The title should make the viewer suddenly see the photograph differently and produce a quiet, exact moment of recognition. Do not force a pun, slogan, inspirational line, or sentimental backstory.

- English usually prefers **1–4 words**. Japanese, Korean, and other languages use one comparably short, natural, complete semantic unit; never break grammar merely to hit an English word count.
- It must correspond to a real fact or relationship in the photo, never free-floating sentiment.
- Apply the unrelated-image swap test: if the title would retain nearly the same force on an unrelated photograph, it does not belong to this image and must be rewritten.
- Avoid travel-promotion lines, place descriptions, photographic jargon, and empty words such as "Memory," "Dream," "Moment," "Journey."
- Do not invent a year. Retain one only when the user explicitly supplies or requests it.
- Output one final title only — no options, no explanation.

### 8.3 Micro text (2–4 groups)

Pair the title with **2–4 groups** of micro text, freely combined from:

- Short or fragmentary phrases (3–8 words)
- State words (DRIFTING / HOLD / NO SIGNAL)
- Place or object information (restrained and abstract, never a travel caption)
- Serial numbers (NO. 016 / SER. 07)
- Coordinate-like figures (34.21 / 118.77, or 0.42 — 1.08)
- Direction words (NORTH / DOWNWARD / OUTBOUND)
- Archive labels (PLATE II / FIG. 3 / ARCHIVE)
- Observation notes (one very short, notebook-like line)

The English examples above describe information functions, not a fixed output language. For Japanese, Korean, or another locale, rewrite them as genuinely natural equivalents in that language. Use a second language only as a small, meaningful editorial accent when the user permits it; never use pseudo-foreign text or gibberish to simulate an international look.

Rules:

- Microcopy must extend the same semantic core with observation, coordinate-like specificity, state, or aftertaste; never pad the layout with random archival labels unrelated to the title.
- Micro text must be **far smaller** than the title, establishing an unmistakable hierarchy.
- Use light-weight sans-serif or a clean monospace, with optional wide tracking.
- Keep total text volume restrained: text must not exceed about 15% of the transformed design frame's visual weight.
- The main title must be immediately legible at normal viewing size and at least about three times the microtext scale; never reduce it to a nearly invisible hairline label.

### 8.4 Typography participates in the image

Type must **take part in space and motion**, not sit on top of the image:

- Align it to the horizon, a motion trajectory, the subject axis, or the edge of the void
- It may run vertically, rotate 90°, or open into wide tracking
- It may embed inside the grain field and be half-covered by dots
- It may be lightly crossed by a line, or partially lost under ink
- Break user copy by semantic phrase. Visual rhythm may not override verbal rhythm; never split or weaken a crucial, negative, or turning word.

Forbidden: centered big-headline poster layout, advertising layout, template title bars, text drop shadows, outlined type, gradient type, and distorted display lettering.

Set the title in the dominant color or black; set micro text in a lighter or lower-saturation member of the same family. Text must stay legible on paper ground without stealing the anchor's visual center.

**No text may appear in the photographic frame of either paired mode.** Design-only may typeset its full transformed frame according to the copy mode.

### 8.5 Locked copy payload

Do not leave the actual wording for the image model to invent during rendering. Append the resolved per-photo copy package to the prompt in this exact form:

```text
COPY MODE: REQUIRED
COPY ORIGIN: USER_EXACT | USER_DIRECTION | SOURCE_DERIVED
COPY LOCALE: <resolved locale, such as ar | ja-JP | ko-KR | en-GB | zh-CN>
COPY INTENT — INSTRUCTION ONLY, NEVER RENDER: <one semantic core and intended emotional turn>
MAIN TITLE: <locked exact string>
MICROTEXT 1: <locked exact string>
MICROTEXT 2: <locked exact string>
MICROTEXT 3: <optional locked exact string>
MICROTEXT 4: <optional locked exact string>
COPY RULE: Render only MAIN TITLE and populated MICROTEXT strings, each exactly once. COPY ORIGIN, COPY LOCALE, and COPY INTENT are instructions, never visible text. Do not rewrite, translate, spell-correct, duplicate, or add text. Respect the resolved locale's script shaping, punctuation, spacing, and semantic line-breaking rules.
```

Remove unused optional lines rather than rendering placeholders. In text-free mode, replace the entire block with `COPY MODE: NONE — render no text or pseudo-text anywhere.`

---

## 9. Output mode, dimensions, and boundary

### 9.1 Four modes

Lock one or more modes before generation; when the caller provides none, ask before continuing. Accept one number, multiple numbers separated by `+`, Chinese/English commas or whitespace, mode names, and `全部` / `all`; deduplicate and execute in menu order 1→4. Each selected ordinary mode produces one file and selected wallpaper mode produces four, so `all` yields seven PNGs per source across four sibling mode directories, never an overview. By default, share the same locked source-specific copy verbatim across all selected modes; only explicit per-mode copy instructions create overrides. In multi-select, custom dimensions must be labeled by mode; ask rather than applying one ambiguous unlabeled size to several modes.

1. **TOP_BOTTOM:** generate the confirmed whole canvas once, with the high-fidelity source in approximately the upper half and the transformed print below; unify both regions through colour, rhythm, and meaning.
2. **LEFT_RIGHT:** generate the confirmed whole canvas once, with the high-fidelity source in approximately the left half and the transformed print on the right as one finished design.
3. **DESIGN_ONLY:** use the source only as content and identity evidence; let the transformed print fill the confirmed whole canvas with no visible source or reserved panel.
4. **WALLPAPER_PACK:** one source produces four separate transformed wallpapers—phone, iPad, desktop, and watch—with no visible source photo. Copy follows the preflight choice of automatic, custom, or text-free output. Also lock an `INDEPENDENT` or `LINKED` wallpaper relationship.

User intent selects the mode; canvas orientation must not silently change it. Paired modes stay exact 50/50. Source-hidden modes must not reintroduce the source, a seam, or reserved placeholder space. Wallpaper-pack recomposes every device separately; never mechanically crop or resize one wallpaper into another.

Wallpaper relationship has two values:

1. **INDEPENDENT:** every device receives only the source photograph, the full 016 aesthetic prompt, and the same locked source facts, palette, motion logic, and copy package. No generated wallpaper becomes a reference, so the four compositions may explore more freely.
2. **LINKED:** generate the iPad wallpaper first by default (honor another anchor device when the user explicitly names one), then approve its source identity, aesthetic motive, copy, typography, and safe area before continuing. Every remaining device receives both the original photograph and that same approved anchor: the photo locks content and identity, while the anchor locks only palette, print grammar, motion treatment, typographic rhythm, and texture. All three derivatives point directly to the same anchor; never chain iPad → phone → desktop → watch, because sequential references accumulate drift.

`LINKED` still makes four separate generation calls and returns four files. The anchor is one of the four deliverables, not an extra fifth master. Every derivative must solve anchor position, motion field, safe area, and typography anew for its device rather than convert the anchor's dimensions. Repeat the full aesthetic prompt and locked copy on every call; do not rely on reference pixels to preserve correct wording.

### 9.2 Dimension priority

Resolve the whole final canvas explicitly before generation: exact user pixels take priority over an explicitly chosen ratio. Offer the original-prompt 3:4, source aspect as an explicit choice, common ratios, or custom values; never infer source-adaptive dimensions silently.

### 9.3 Generate the complete canvas first

For a paired mode, send the source as a high-fidelity edit/reference input together with the complete 016 aesthetic prompt and locked copy, then generate the whole finished canvas in one job. Treat 50/50 as the composition target while prioritising unity of colour, light, rhythm, typography, and meaning. Design-only and all four wallpapers each generate a complete canvas. Prepare separate photographic and design assets only after a targeted complete-canvas retry still fails or another runtime-contract fallback condition applies.

### 9.4 Resolved mode block

Append:

```text
OUTPUT MODE: TOP_BOTTOM | LEFT_RIGHT | DESIGN_ONLY | WALLPAPER_PACK
DEVICE PROFILE: NONE | PHONE | IPAD | DESKTOP | WATCH
FINAL CANVAS: <whole finished ratio and/or exact WIDTHxHEIGHT>
GENERATION STRATEGY: SINGLE COMPLETE CANVAS
REFERENCE ROLE: SOURCE — HIGH-FIDELITY CONTENT AND IDENTITY ANCHOR
SOURCE VISIBILITY: UPPER 50% | LEFT 50% | REFERENCE ONLY — NOT VISIBLE
LAYOUT RULE: Generate one finished image. Paired modes keep approximately equal source and transformed regions while unifying colour, light, rhythm, typography, and meaning. Source-hidden modes use the complete canvas and show no photo or reserved panel.
WALLPAPER RELATIONSHIP: NONE | INDEPENDENT | LINKED
ANCHOR DEVICE: NONE | IPAD
```

### 9.5 Wallpaper safe regions

- **Phone:** keep the top clock/notch region and bottom control region quiet; place no anchor core or fine type there.
- **iPad:** keep essential content inside a centered safe square; use extendable paper, void, and motion field outside it so portrait and landscape crops remain viable.
- **Desktop:** keep the top menu area, bottom dock/taskbar, and both icon edges low-information; keep decisive contours away from the edges.
- **Watch:** keep the main shape and a simplified but visible type hierarchy recognizable at thumbnail size while reserving the major clock/complication area. Type may be enlarged, shortened, or rearranged but not deleted by default. The anchor may expand to 24%–40% of frame width; all other one-anchor, one-motion, void, palette, typography, and print-texture rules remain.

### 9.6 Boundary

- Top-bottom uses a horizontal central boundary; left-right uses a vertical central boundary. Both are clean, direct, and shadowless.
- Use no torn paper, frames, inset margins, cards, tape, scanner borders, collage shadows, or mockups.
- Design-only has no boundary and must not imitate a diptych.
- Wallpaper outputs also have no boundary, device frame, system UI, or multi-image layout.
- Any restrained grain echo in paired modes must not cover or contaminate the photographic subject.

---

## 10. Output limits

- Each selected ordinary mode produces one independent finished image per source; selected wallpaper-pack adds exactly four separate wallpaper files. `all` therefore produces seven PNGs across four sibling task directories per source. Process multiple source photos separately and never create a collage, grid, contact sheet, or series overview.
- Copy follows the resolved preflight: automatic or custom copy uses one clearly dominant title and up to two to four microtext groups; when custom copy omits microtext, derive supporting microtext professionally or keep title-only if requested. Text-free mode renders no letters, characters, numbers, or decorative pseudo-text. Include no logo, watermark, signature, palette, legend, frame note, or interface element.
- Output the finished image only — no analysis, no creative notes, no title options, no parameter lists.

Strictly avoid: photo redrawing, scene reconstruction, visible outpainting seams, a filtered look, posterized photographs, vector tracing, complete illustration, infographics, generic icons, multiple focal points, complex scenes, accumulated ornament, ordinary gradients, CG lighting, 3D finish, commercial poster feel, template feel, stacked motion effects, stiff centered symmetry, and any loss of identity echo between the two halves.

## 11. Pre-generation check

Before submitting each photo's generation request, confirm internally:

1. This call processes one clearly selected photo and carries no subject, color, or copy from another input.
2. Mode and dimensions are locked per section 9, with exact pixels taking priority; paired modes split 50/50 on the correct axis, while source-hidden modes have no seam.
3. The photographic panel stays faithful in paired modes; design-only and wallpapers contain no source photo, seam, or reserved area.
4. The transformed print contains one recognizable anchor, exactly one source-derived motion logic, and 60%–78% clean void calculated against its complete frame.
5. The palette contains only one spirited source color, paper, and optional small black.
6. Copy mode follows section 8: automatic, custom, or text-free output is locked before generation; locale follows audience/market > output language > direction language; if none is explicit, ask before generation and is never guessed from identity. Automatic or direction-led copy uses native target-locale language, moves from visible fact to grounded subtext, passes the unrelated-image swap test, and avoids forced cleverness, while finished user copy stays verbatim and is typeset by that language's semantic phrases. Only an explicit text-free request removes all text and pseudo-text.
7. The finished bitmap was actually opened and inspected at normal and thumbnail size; anchor, motion, palette, and copy are specific to this source rather than generic decorative abstraction.
8. All four wallpapers were separately recomposed, match their exact sizes, keep essential content in device-safe regions, and contain no baked-in system UI. `INDEPENDENT` uses only the original photo for all four; `LINKED` approves the anchor first and makes every derivative reference the original photo plus that same anchor, with no sequential drift or mechanical resizing.
9. The deliverable is a Codex-generated PNG bitmap, not SVG, HTML, Canvas, or programmatic drawing.
10. There is no collage, second focal point, gradient, CG lighting, logo, watermark, UI, mockup, or other excluded element.
