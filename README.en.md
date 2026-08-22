<div align="center">

# XXD Panel 016

### Compress what truly happens in a photograph into one anchor and one field of motion

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-c4573a?style=flat-square)](#four-outputs-not-four-templates)
[![Raster Output](https://img.shields.io/badge/Output-PNG-2f6f62?style=flat-square)](#boundaries-and-trust)

<a href="README.md">简体中文</a> · <strong>English</strong> · <a href="README.ja.md">日本語</a>

</div>

> ONE SUBJECT · ONE MOTION · A LARGE FIELD OF AIR

XXD Panel 016 is an image-generation skill for Codex and compatible agents. It does not place a photograph under a fixed filter. It reads the subject, posture, direction, light, distance, and unfinished relationship, then compresses that evidence into a restrained, tactile Riso or screen-printed composition.

The photograph supplies the facts. 016 decides which motion deserves to remain.

## Why it exists

Generic style transfer often makes unrelated photographs look like the same decorative poster. A real subject becomes a stock sun, wave, ring, or geometric icon; the palette stops belonging to the source; the title could be reused on any image.

016 works in the opposite direction. It locks one small but recognisable visual anchor, then derives exactly one motion logic from posture, light, or spatial relation. The result may be minimal, but it must retain evidence that could only have come from this photograph.

```text
source photo → lock visual facts → read relation and subtext → choose one motion → generate print → compose and inspect
```

## The 016 visual contract

- **One anchor:** a small recognisable core, with no competing second subject.
- **One motion:** falling, rising, flowing, radiating, or ripple/echo—never a stack of effects.
- **Active void:** normally 60%–78% open paper, so stillness and movement can coexist.
- **Source-derived colour:** one dominant source colour, warm paper, and optional black; 2–3 colours in total.
- **Physical print character:** halftone, fibre, dry ink, grain, and slight misregistration act as structure rather than decoration.
- **Type as space:** title and microcopy follow motion, axes, and void instead of sitting inside an advertising box.

## Four outputs, not four templates

If no mode is specified, the skill asks first. Dimensions may be supplied in the same reply; exact pixels take priority.

| Mode | Default canvas | Deliverable |
| --- | ---: | --- |
| `top-bottom` | 3:4 | original photo above, 016 print below, exact 50/50 split |
| `left-right` | 3:2 | original photo left, 016 print right, exact 50/50 split |
| `design-only` | 3:4 | one full transformed print with no visible source photo |
| `wallpaper-pack` | four device sizes | separate phone, iPad, desktop, and watch PNGs |

Photography in paired modes remains truthful, with only restrained grading and necessary environmental extension. In design-only and wallpaper modes, the photograph remains evidence but does not appear in the finished image.

### Wallpaper packs: independent or linked

Defaults are phone `1440×3200`, iPad `2048×2732`, desktop `3840×2160`, and watch `1024×1024`. Each may be overridden independently.

- **Linked pack (recommended):** generate and approve the iPad anchor first; every other device receives the original photo plus that same anchor and is recomposed for its own canvas.
- **Independent set:** every device receives only the original photograph and may explore more freely.

Both options return four separate files. A linked pack is not one master image cropped four ways, and it never chains references from iPad to phone to desktop to watch.

## Copy should make the photograph click

Copy is on by default in every mode and disappears only on an explicit text-free request.

Automatic copy reads literal fact, relational tension, and grounded subtext. It then uses precise naming, contrast, understatement, double meaning, or a slight reversal to produce an extremely short title. The title must pass the unrelated-image swap test: if it works just as well on another photograph, it must be rewritten.

Finished user wording remains verbatim. A direction or editable draft is refined only after preserving audience, communication goal, mandatory words, tone, and implied meaning.

Language follows the intended audience rather than the language used to issue the command:

```text
target market or audience > requested output language > direction language > request language
```

A Chinese request for a Japanese edition produces natural Japanese; a Korean-audience request uses natural Korean; a UK edition uses British English. The skill never guesses nationality from a face or scene and never uses pseudo-foreign text for atmosphere.

## Exact geometry belongs to code; art direction belongs to image generation

The image model creates the print. `scripts/compose_panel.py` only plans canvases, performs exact 50/50 raster composition, finalises dimensions, and audits results. It does not fake artwork with programmatic drawing.

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom
python3 scripts/compose_panel.py --plan --layout left-right --size 2560x1440
python3 scripts/compose_panel.py --audit result.png --layout design-only --size 2048x2048
```

Exact top-bottom canvases require an even total height; exact left-right canvases require an even total width. The skill never silently changes a requested pixel size.

## Get started

```bash
git clone https://github.com/nevertoday/xxd-panel-016.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-016" ~/.codex/skills/xxd-panel-016
```

Claude Code users can link the same folder to `~/.claude/skills/xxd-panel-016`. Restart the agent session after installation.

```text
$xxd-panel-016
Turn this photograph into a 2560×1440 left-right composition. Use Japanese copy.
```

You may also invoke the skill with only a photograph. It will ask for the output mode in a numbered multiline menu, then ask whether a wallpaper pack should be linked or independent when necessary.

Full specifications:

- [Skill workflow](SKILL.md)
- [Chinese full prompt](references/xxd-panel-016-prompt.zh-CN.md)
- [English full prompt](references/xxd-panel-016-prompt.en.md)

## Boundaries and trust

- Each source photo stays inside its own task and never borrows subjects, old outputs, or bundled examples.
- Every invocation opens a fresh task directory; a previous result cannot be declared the current job.
- Deliverables are PNG bitmaps, never SVG, HTML, Canvas, or programmatic-vector substitutes.
- The configured bitmap bridge emits sanitised status only and does not print providers, endpoints, headers, credentials, prompts, or server response bodies.
- Ordinary modes return one image; `wallpaper-pack` returns exactly four separate images, never a contact sheet.

Local composition needs Python 3 and Pillow. The safe bitmap bridge uses Python 3.11+ `tomllib`. Image generation still requires a host agent with built-in raster generation or an already configured compatible raster route.

## How 016 differs from 019

016 shares its mode, sizing, copy, localisation, wallpaper, and review workflow with [XXD Panel 019](https://github.com/nevertoday/xxd-panel-019), but not its visual knowledge.

| 016 | 019 |
| --- | --- |
| tiny anchor plus one motion field | recognisable subject plus geometric hierarchy |
| 2–3 colour Riso or screen print | 3–5 colour retro-modernist flat illustration |
| vast void and physical grain | positive/negative shape, scale contrast, hard colour planes |

## Repository

```text
xxd-panel-016/
├── SKILL.md
├── README.md / README.en.md / README.ja.md
├── agents/openai.yaml
├── scripts/
│   ├── compose_panel.py
│   └── configured_imagegen.py
└── references/
    ├── xxd-panel-016-prompt.zh-CN.md
    ├── xxd-panel-016-prompt.en.md
    └── 016-source.md
```

## Acknowledgements

The multilingual navigation and README information architecture draw inspiration from [Gathered Scenes Zine](https://github.com/Zeejay0/gathered-scenes-zine-skill), [Photo Abstract Editorial](https://github.com/ZzzLc0405/photo-abstract-editorial), and [Awesome GPT Image 2](https://github.com/freestylefly/awesome-gpt-image-2). The 016 visual system, modes, and execution rules remain independent.

<div align="center">

**Let motion come from the photograph, not the template.**

</div>
