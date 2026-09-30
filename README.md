StudioCut Pro
A browser-based 16:9 video studio: multi-clip timeline, image/video/text overlays, chroma key, music, sound effects, voiceover and export. No build step, just open `index.html`.
Structure
```
index.html            page markup
css/styles.css        custom styles (sliders, scrollbars, mobile layout)
js/
  tailwind-config.js  Tailwind theme (colors, fonts)
  state.js            global state and canvas pipeline
  canvas.js           canvas sizing and pointer coordinates
  clips.js            media loading and multi-clip sequence engine
  layers.js           overlay layers and inspector sync
  chroma-key.js       background removal for image/video overlays
  text-layers.js      text overlay styling
  render.js           frame renderer, animations, filters
  interaction.js      drag / scale / rotate on the canvas
  timeline.js         timeline UI, lanes, playhead
  editing.js          split, trim, delete
  transport.js        playback controls
  export.js           video export
  audio.js            music, SFX, voiceover
```
Scripts are plain (non-module) files loaded in order from `index.html`, so keep that order if you add files.
Run
Open `index.html` in a browser, or serve the folder (`npx serve` / GitHub Pages). Microphone access (voiceover) requires `https` or `localhost`.
