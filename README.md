# Vortex Video Converter

A browser-based tool that turns regular videos into animated **Vortex Part pixel screens** and exports a ready-to-use Vortex `.lua` script.

**Local processing · No upload required · Smart compression · 16.7M colors**

## Quick start

1. Download or clone this repository.
2. Open `index.html` in Chrome, Edge, or another modern Chromium-based browser.
3. Drop in a video.
4. Choose **Auto Vortex** for the easiest setup.
5. Click **Convert video to Vortex**.
6. Preview the result.
7. Download the generated `.lua` script and use it in Vortex.

## What it includes

- Video-to-Part pixel conversion
- Auto Vortex quality selection
- Fast, Recommended, Better, High, Ultra, and Custom presets
- 16.7M-color processing
- Edge-preserving scaling
- Temporal anti-flicker
- Motion smoothing
- Scene/detail detection
- Smart frame compression
- Duplicate-frame merging
- Live Vortex performance meter
- Estimated conversion time
- Built-in pixel preview and playback
- Optional physical screen frame
- Editable Vortex export settings
- Obfuscated generated Vortex runtime code
- Branded ending on every export: **Made with Vortex Video Converter**

## Quality presets

| Preset | Best for | Vortex load |
| --- | --- | --- |
| Auto Vortex | Most users | Automatically balanced |
| Fast | Testing and weaker systems | Low |
| Recommended | Everyday conversions | Medium |
| Better | More visual detail | Medium–High |
| High | Short, detailed clips | High |
| Ultra | Maximum detail | **Very laggy — short clips only** |
| Custom | Manual control | Depends on settings |

## Performance tips

Vortex has to update many colored Parts every frame. Higher resolution and higher FPS increase the workload quickly.

If a converted video is too heavy, try lowering the quality preset, lowering FPS, reducing the Part resolution, or shortening the clip. The converter shows a live load estimate before you start.

## Privacy

The selected video is processed locally in your browser. The converter does not upload the video to a server.

## Browser compatibility

Chrome and Edge are recommended. Other modern browsers may work, but supported video formats depend on the browser's built-in codecs.

## Export format

The generated Vortex script contains a readable **SETTINGS** section followed by compressed/obfuscated playback data and runtime code. This keeps the important setup values easy to edit while making the generated payload more compact and less readable.

## End credit

Every generated video ends with:

> **Made with Vortex Video Converter**

The credit is rendered as actual pixel frames so it appears on the same Vortex Part display.

## Repository files

- `index.html` — complete converter website and app
- `README.md` — project guide
- `CHANGELOG.md` — release history

## Troubleshooting

**The conversion is taking a long time**  
Use Fast or Recommended, reduce FPS, or reduce the Part resolution.

**The result is laggy in Vortex**  
Lower the preset until the performance meter reports a safer load.

**A video will not open**  
Try converting the source file to a browser-friendly MP4/WebM format first. Browser codec support varies.

**The exported Lua is large**  
Long videos, high FPS, and high Part resolution naturally create more frame data. Smart compression and duplicate-frame merging help reduce it.

## Credits

Created for the Vortex community.

Repository: https://github.com/Madster522/VortexVideoConverter
