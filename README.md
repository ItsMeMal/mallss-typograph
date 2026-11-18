# Mallss Typograph

A focused skill collection for **audio-driven PMV production** and **kinetic typography**. Built for deliberate motion design: the soundtrack drives the edit, the meaning drives the visuals, and typography is treated as composition—not just animated subtitles.

## Included skills

### 1. `audio-driven-pmv-typography-skill`

The full PMV / audio-driven production workflow. It helps an agent:
- Analyze music, voice, rhythm, vocal phrasing, dynamics, pauses, and emotional progression.
- Build an audio cue sheet, scene timeline, and storyboard before rendering.
- Choose between typography-only, photo-led, mixed-media, abstract, and footage-led scenes.
- Design a coherent motion language and synchronize visual events to meaningful audio cues.
- Plan, render, preview, inspect, and quality-check the final video.

This is the creative-direction and end-to-end production skill.

### 2. `kinetic-typography`

A practical text-animation skill covering:
- Line, word, and character splitting/staggering.
- Mask, blur, and clip-path reveals.
- GSAP SplitText, Framer Motion, CSS, and Remotion techniques.
- Variable-font weight/width animation, SVG stroke draw-on, and text-on-path.
- Accessibility-safe text splitting and deterministic visual verification.

This is the typography-animation technique library.

## How the two skills work together

Use **audio-driven PMV** to decide *what the video should communicate and when*. Use **kinetic typography** to decide *how a particular text element should move and reveal*.

The kinetic skill is a technique reference, not a fixed visual template. Do not force every scene to use text-only animation. Choose visual modes scene by scene based on audio, words, and concept.

## Repository structure

```text
.claude/
└── skills/
    ├── audio-driven-pmv-typography-skill/
    │   ├── SKILL.md
    │   ├── README.md
    │   └── references/
    └── kinetic-typography/
        ├── SKILL.md
        └── references/
scripts/
├── contact-sheet.sh
├── probe-mp4.sh
├── seek-shot.sh
└── README.md
licenses/
└── iart-ai-MIT-LICENSE.txt
```

## Use with Claude Code

Clone this repository and open it as the project, or copy the two skill folders into your own project's `.claude/skills/` directory.

```bash
git clone https://github.com/ItsMeMal/mallss-typograph.git
```

Then ask Claude Code to use:
- `audio-driven-pmv-typography-skill` for an audio-led PMV, lyric-style, or motion-graphics video.
- `kinetic-typography` when designing or implementing animated text, titles, lyric phrases, or caption treatments.

For a complete audio-driven typography video, explicitly ask it to load **both** skills.

## Verification helpers

The included scripts support the kinetic-typography workflow:
- `scripts/seek-shot.sh` — capture deterministic moments from a standalone HTML animation.
- `scripts/contact-sheet.sh` — combine still frames for quick visual review.
- `scripts/probe-mp4.sh` — inspect and optionally assert an exported MP4's resolution, frame rate, and codec.

See [scripts/README.md](scripts/README.md) for usage and requirements.

## Attribution and licensing

- `kinetic-typography` and its supplied helper scripts are adapted from [iart-ai/kinetic-typography-skills](https://github.com/iart-ai/kinetic-typography-skills), under the MIT License. The original notice is preserved in [licenses/iart-ai-MIT-LICENSE.txt](licenses/iart-ai-MIT-LICENSE.txt).
- `audio-driven-pmv-typography-skill` is the custom skill created for the repository owner and supplied in the original archive. No separate license file was included with that archive; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

