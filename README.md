# Starsounds: Binaural Beat Designer

A single-page web app for designing layered binaural beats. Each of five tones sits on a field where left and right sets the beat (0.5–30 Hz) and up and down sets the carrier tone (50–500 Hz). The left ear hears the carrier and the right ear hears the carrier plus the beat.

Use headphones.

## Features

- Five tones, each with a volume slider whose glowing orb is also its mute button. Louder tones look nearer and brighter.
- Reference layer: click a tone to show its octaves (8), fifths (5) and thirds (3), with points where each line meets the curve.
- Curve slider (Mirror, Even, Consonant): sets how beats scale with pitch. On the Consonant curve, both ears hear the same chord, perfectly in tune.
- Point locks (pitch and beat follow the parent) and line locks (pitch follows, beat stays). Locked tones whose point leaves the field wait at the edge, muted.
- White, pink and brown noise channels, each visualized as its own kind of starfield.
- Tone and Noise master levels (click a label to mute its section).
- Presets: 14 chords in three groups (Consonant, Colorful, Dissonant and loose).
- Settings are saved in the browser (localStorage).

## Running it

Everything is in one self-contained `index.html` file with no build step. Open it in a browser, or serve the folder:

```
python3 -m http.server
```

Then visit http://localhost:8000.

It also works as a GitHub Pages site. In the repository settings, go to **Pages**, choose to deploy from the `main` branch root, and the app will be served at `https://<your-username>.github.io/<repo-name>/`.

## Folder layout

| Path | What it is |
|---|---|
| `index.html` | The current app: logo with Presets and Play in a top bar on desktop, a fixed bottom bar on mobile, Curve-style master sliders |
| `experiments/point-lock-test.html` | Scratch copy of the point-lock and curve work |
| `versions/` | Earlier snapshots: before and after the cosmic restyle, before curves, and before the final layout |
| `assets/starsounds_logo.svg` | Logo |

## Notes

The fonts load from Google Fonts. Without a connection, the app falls back to system fonts and works the same.
