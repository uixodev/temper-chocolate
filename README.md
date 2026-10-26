# Temper

A landing-page hero for a handmade chocolate maker. The word **TEMPER** sits glossy and solid on an ivory screen, and behaves like real chocolate.

- **Move the cursor** over a letter and its edges go soft, like chocolate on a warm hand.
- **Hold it still** for about a second and the letter melts: the bottom sags, a drop forms, stretches into a thin strand and falls. It lands at the bottom of the screen as a small puddle.
- **Move away** and the letter slowly pulls itself back and sets, with a brief shine passing across it. The puddle stays a while, then fades.
- At the bottom of the screen one slow drop keeps forming and falling: the invitation to scroll.

Technique follows the `test-liquid` experiment: letters are round-pen skeletons drawn as circles on a canvas, and an SVG blur + alpha-threshold filter fuses them into one smooth liquid shape. Thin strands, which are too fine for that filter, are drawn crisp on a separate canvas on top.

## Run

No build step. Open `index.html`, or serve the folder (for example VS Code Live Server).

## Tweak

Everything tunable is in the `SETTINGS` block at the top of the script: hold time, melt and recovery speed, sag, gravity, how long puddles stay, shine duration and the scroll-cue timing. Colours are in the `BG`, `DARK`, `WARMC`, `HI` and `CREAM` constants.

## Notes

- The `<h1>` stays in the page for search engines and screen readers; the canvases are `aria-hidden`.
- `prefers-reduced-motion` gets a still, solid word with no melting.
- On narrow screens the word wraps to TEM / PER. Touch works: press and hold a letter.
- `window.temper` exposes the letters, drops and puddles for inspection.
