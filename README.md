# YoutubeShorts

Animated cartoon Shorts rendered in code: three.js inside Remotion (2D cartoon characters in a 3D toon world),
ElevenLabs narration, Whisper word timings for captions.

- `.claude/skills/cartoon-3d-short/` — the cartoon short skill (from mromidev/claude-animated-shorts, MIT), without its reference images.
- `src/videos/bridge/` — the skill's template short, the starting point for every new short.
- `shorts/<name>/SCRIPT.md` — facts, sources and script per short.
- `scripts/stills.mjs` — render test frames: `node scripts/stills.mjs <CompId> out/x_ 100,700 0.5`.

## Rendering without a GPU
Use Chromium's software GL: `--gl=swangle --browser-executable=/opt/pw-browsers/chromium`.
The post-processing composer is driven by hand in `Bridge.tsx`, because the `@react-three/postprocessing`
wrapper produced blank frames under Remotion with the installed versions.
