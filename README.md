# Vortex Video Converter

Convert regular videos into animated **Vortex Part pixel screens**.

The converter runs locally in your browser and exports a Vortex `.lua` script that recreates the video using colored Parts.

## Features

- Video-to-Part pixel conversion
- Auto Vortex quality settings
- Multiple quality presets
- 16.7M-color processing
- Edge-preserving scaling
- Temporal anti-flicker
- Motion smoothing
- Scene/detail detection
- Smart frame compression
- Live Vortex performance estimate
- Estimated conversion time
- Built-in pixel preview
- Optional physical screen frame
- End card on every export:
  **Made with Vortex Video Converter**

## How to use

1. Open `index.html` in a modern browser.
2. Choose or drag in a video.
3. Pick a quality preset.
4. Click **Convert video to Vortex**.
5. Preview the result.
6. Download the generated `.lua` file.
7. Run/import that script in Vortex.

## Quality presets

- **Auto Vortex** — easiest option and automatically balances quality and performance.
- **Fast** — fewer Parts and lighter performance.
- **Recommended** — good balance of detail and smoothness.
- **Better** — higher visual detail.
- **High** — heavier Vortex workload.
- **Ultra** — **VERY LAGGY** and best kept to short clips.
- **Custom** — manually choose resolution, FPS, and other settings.

## Performance

Higher resolution and FPS create more Part updates and can cause lag.

If a video is too heavy:
- lower the quality preset,
- reduce FPS,
- reduce the Part resolution,
- or use a shorter clip.

The website includes a live performance meter before conversion.

## Privacy

Video processing is performed locally in your browser.

Your selected video is not uploaded by the converter.

## Browser support

Use a current version of Chrome, Edge, or another Chromium-based browser for best results.

Video format support depends on what your browser can decode.

## Credits

Created for the Vortex community.

Every generated video ends with:

> Made with Vortex Video Converter

## Repository

Website entry point: `index.html`
