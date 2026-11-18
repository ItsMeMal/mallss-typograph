# Production Implementation Notes

Choose tools after inspecting the local environment and user constraints.

## Audio analysis
Possible utilities include `ffprobe` for metadata, FFmpeg for extraction/assembly, and librosa or an equivalent tool for onset/tempo analysis. Validate beat markers by listening. Automated beat detection can be wrong, especially with live music, syncopation, ambient sound, and tempo changes.

## Timeline-first implementation
Represent each scene/cue as structured data (JSON, CSV, or the native editor's markers). Store time in seconds and derive frame positions once the frame rate is fixed. All text, image, transition, and sound cues should reference the same scene timeline.

## Code-driven render
If using Remotion, a browser canvas, or another code-driven renderer:
- use deterministic scene timing;
- preload media and fonts;
- avoid layout shifts during render;
- use frame-based animation values;
- render representative frames and inspect them before full export;
- verify audio muxing and final output metadata.

## Native editor
If using After Effects, Alight Motion, Resolve, Blender, or another editor:
- preserve an editable project;
- organize layers and comps by scene;
- label audio markers and scene transitions;
- avoid flattening the only editable source;
- collect fonts and media dependencies when possible.

## Environment honesty
Do not state that a package, app, plugin, GPU encoder, browser, or image-generation service is available until checked. If a capability is missing, select a workable alternative or explain the exact blocker. Never replace the requested final video with a screenshot or HTML mockup without saying so.
