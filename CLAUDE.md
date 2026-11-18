# Mallss Typograph — Agent Instructions

This repository contains two complementary typography/video-production skills. Load the source skill files when a task matches them; do not replace their workflows with generic assumptions.

## Skill routing

### Audio-led PMV / lyric-style / music-driven video
Read:
- `.claude/skills/audio-driven-pmv-typography-skill/SKILL.md`
- Its relevant files under `.claude/skills/audio-driven-pmv-typography-skill/references/`

Use this as the primary creative-direction and end-to-end production workflow. The actual supplied audio determines pacing, phrase timing, rhythm, dynamics, and emotional progression.

### Animated type / title / lyric text implementation
Read:
- `.claude/skills/kinetic-typography/SKILL.md`
- `.claude/skills/kinetic-typography/references/reveal-recipes.md`

Use this as a technique library for choosing and implementing text animation. Do not apply every technique or turn the entire video into the same reveal effect.

## When both apply

1. Use the audio-driven PMV skill first to analyze the soundtrack, establish the concept, choose scene-level visual modes, and create the authoritative timeline/storyboard.
2. Use the kinetic-typography skill for the specific text treatments that serve that plan.
3. Preserve the PMV skill's scene-level flexibility: typography-only, photo-led, mixed-media, abstract, and footage-led scenes may coexist.
4. Choose the rendering stack only after inspecting the project's existing framework and locally available tools. Do not assume Remotion, After Effects, Alight Motion, FFmpeg, or any paid service is available.
5. Render a preview, inspect real frames and playback, correct defects, and verify the actual export before calling it final.

## Quality bar

- No generic slideshow or random beat-flashing.
- Do not animate every word or beat by default.
- Keep text accurate, readable, accessible, and synchronized to the real audio.
- Keep source media intact and preserve asset attribution.
- Never claim to have rendered, inspected, or verified output that was not actually produced and checked.
- Do not edit unrelated repository files.
