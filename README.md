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
- Automatic portrait-video detection and portrait-friendly Part layouts
- Auto Vortex quality selection
- Fast, Recommended, Better, High, Ultra, and Custom presets
- 30-bit extended-color processing (10 bits per RGB channel)
- Up to 1.07B representable RGB colors in the exported 30-bit color pipeline
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

## Portrait videos

Vertical videos are detected automatically. Auto Vortex and the built-in quality presets rotate their Part dimensions to preserve a portrait layout instead of forcing a landscape-sized screen.

## Extended color

The converter now keeps 10 bits of precision per red, green, and blue channel through its processed output, for up to 1,073,741,824 representable RGB values. Vortex supports normalized `Color3.new(R, G, B)` values from 0 to 1, which the generated player uses for the extended-color output.

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

## Vortex property-change safety

Vortex can reject a task that queues too many property changes in a single engine frame. Generated scripts now build the screen in batches of **500 Parts** and yield between batches. They also include a **30,000 color-change** guard for unusually large custom screens.

The generated Lua keeps these controls in the readable SETTINGS section:

- `BUILD_PARTS_PER_STEP=500`
- `MAX_COLOR_CHANGES_PER_STEP=30000`
- `SAFE_YIELD_SECONDS=0.02`

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
