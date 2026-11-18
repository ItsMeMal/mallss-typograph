# Mallss Typograph

**Audio-led motion design. Expressive typography. Intentional editing.**

A focused Claude Code skill library for creating **PMV videos, lyric-style edits, kinetic typography, and audio-driven motion graphics**. It combines one end-to-end creative production workflow with a practical text-animation technique library.

The principle is simple: **let the audio shape the edit, let the meaning shape the visuals, and let typography become part of the composition.**

---

## The two skills

<table>
  <tr>
    <td width="50%">
      <h3>01 · Audio-Driven PMV Studio</h3>
      <code>audio-driven-pmv-typography-skill</code>
      <p>The creative director and production workflow. It analyzes the soundtrack, develops the visual concept, plans the timeline, chooses scene treatments, and guides the video through rendering and quality control.</p>
      <ul>
        <li>Music, voice, rhythm, dynamics, pauses, and vocal phrasing</li>
        <li>Audio cue sheets, scene timelines, and storyboards</li>
        <li>Typography-only, photo-led, mixed-media, abstract, and footage-led scenes</li>
        <li>Audio synchronization and final-output verification</li>
      </ul>
      <a href=".claude/skills/audio-driven-pmv-typography-skill/SKILL.md">Read the skill →</a>
    </td>
    <td width="50%">
      <h3>02 · Kinetic Typography</h3>
      <code>kinetic-typography</code>
      <p>The text-animation technique library. It turns a designed type composition into motion with practical patterns for web and video workflows.</p>
      <ul>
        <li>Line, word, and character splitting and stagger</li>
        <li>Mask, blur, clip-path, and directional reveals</li>
        <li>CSS, GSAP SplitText, Framer Motion, and Remotion</li>
        <li>Variable-font animation, SVG stroke draw-on, and text-on-path</li>
      </ul>
      <a href=".claude/skills/kinetic-typography/SKILL.md">Read the skill →</a>
    </td>
  </tr>
</table>

## How they work together

These are **two complementary skills, not two copies of the same workflow**.

| Stage | Skill | Responsibility |
|---|---|---|
| 1. Listen & interpret | Audio-Driven PMV | Analyze the actual audio and identify meaningful cues |
| 2. Direct & plan | Audio-Driven PMV | Define the concept, visual modes, scene timeline, and storyboard |
| 3. Design text motion | Kinetic Typography | Choose and implement suitable typography-animation techniques |
| 4. Produce & refine | Both | Keep motion aligned with the creative plan, preview, inspect, and revise |
| 5. Verify delivery | Audio-Driven PMV | Check synchronization, readability, continuity, and exported media |

**Important:** Kinetic typography is a technique library—not a visual template. A video does not need to animate every word or use text-only scenes throughout. The PMV workflow can deliberately combine typography, photography, footage, collage, illustration, and abstract motion when the content calls for it.

## What this library is for

- **PMV and lyric-style videos** — interpret vocals and music as a visual sequence.
- **Kinetic typography** — animate headlines, words, phrases, and titles with controlled hierarchy.
- **Audio-driven motion graphics** — connect movement, transitions, and visual emphasis to real audio events.
- **Short-form edits** — develop scene pacing and visual progression for vertical content.
- **Mixed-media storytelling** — combine animated text with photos, footage, graphic elements, and compositing.

## Get started

### Option A — Clone the repository

```bash
git clone https://github.com/ItsMeMal/mallss-typograph.git
cd mallss-typograph
```

Open the repository in Claude Code. The project-level skills are stored in `.claude/skills/`.

### Option B — Add the skills to an existing project

Copy these two directories into the target project's `.claude/skills/` directory:

```text
.claude/skills/
├── audio-driven-pmv-typography-skill/
│   ├── SKILL.md
│   ├── README.md
│   └── references/
└── kinetic-typography/
    ├── SKILL.md
    ├── README.md
    └── references/
```

### Example prompts

**Plan a complete PMV:**

> Use audio-driven-pmv-typography-skill. Analyze the supplied audio first, then develop an original visual concept, audio cue sheet, scene timeline, and storyboard. Choose the right mix of typography, imagery, and motion for each section. Do not render until the plan is ready.

**Build a kinetic title:**

> Use kinetic-typography to create a bold, editorial headline reveal. Choose the split level and reveal technique based on the copy. Include an accessible text label and a deterministic preview so the animation can be inspected.

**Use both together:**

> Load both audio-driven-pmv-typography-skill and kinetic-typography. Create an audio-synchronized PMV. Let the PMV skill direct the concept, pacing, and scene treatments; use the kinetic skill for the text-animation techniques. Keep the visual language coherent and avoid repeating one effect across every scene.

## Production principles

- **Audio first:** use the supplied soundtrack as the timing authority. Automated beat detection is a guide, not a substitute for listening.
- **Meaning before effects:** text and imagery should reinforce the words, mood, or narrative.
- **Scene-level freedom:** choose typography-only, photo-led, mixed-media, abstract, or footage-led treatments where they make sense.
- **A coherent motion language:** use a deliberate set of techniques instead of stacking random effects.
- **Readability matters:** preserve exact copy, clean typography, safe margins, and enough screen time to read.
- **Preview before final:** inspect real frames and playback, then verify the exported file. Never claim a render was completed or checked unless it actually was.

## Verification scripts

Small helpers are included in `scripts/` to support a repeatable preview-and-check workflow.

| Script | Purpose |
|---|---|
| `seek-shot.sh` | Capture deterministic moments from a standalone HTML animation using its `?t=N` seek harness |
| `contact-sheet.sh` | Combine captured frames into a single review image |
| `probe-mp4.sh` | Inspect an MP4 and optionally assert its resolution and frame rate |

See [scripts/README.md](scripts/README.md) for commands and requirements. The scripts use tools such as FFmpeg/FFprobe and Playwright; check the requirements before running them.

## Repository map

```text
.claude/
└── skills/
    ├── audio-driven-pmv-typography-skill/
    │   ├── SKILL.md
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

CLAUDE.md
THIRD_PARTY_NOTICES.md
README.md
```

## Sources & licensing

- **Kinetic Typography** is adapted from [iart-ai/kinetic-typography-skills](https://github.com/iart-ai/kinetic-typography-skills). Its MIT license notice is preserved in [licenses/iart-ai-MIT-LICENSE.txt](licenses/iart-ai-MIT-LICENSE.txt).
- **Audio-Driven PMV Typography** is the custom skill supplied for this repository owner. The original archive did not include a separate license file; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
- Reference implementations and techniques remain subject to their respective upstream licenses and dependencies.

---

<p align="center">
  <strong>Mallss Typograph</strong><br>
  <sub>Listen closely. Design deliberately. Animate with purpose.</sub>
</p>
