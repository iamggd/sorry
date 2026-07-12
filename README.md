# Sorry Card

A simple single-file HTML apology card with an interactive envelope animation that reveals a message.

## Project Structure

- `/home/runner/work/sorry/sorry/index.html` — Complete app (HTML, CSS, and JavaScript).

## Usage

1. Open `/home/runner/work/sorry/sorry/index.html` in any modern browser.
2. Click/tap the envelope to reveal the letter.

## Customization Guide

### 1) Change the visible text

Edit these elements in `index.html`:

- Prompt text (`tap to open`)
- Quote text (`"A good apology is like a good bridge..."`)
- Main apology text (`I'm sorry 🙏`)
- Footer text (`let's be okay again?`)

### 2) Change colors and theme

Update CSS variables in the `:root` section:

- `--bg1`, `--bg2` for page gradient
- `--ink`, `--ink-soft` for text
- `--accent`, `--accent2` for highlights
- `--paper`, `--paper-shade` for envelope/letter surface

### 3) Tune animation timing

Adjust transition timing values in:

- `.env-flap` transition
- `.letter-wrap` transition
- JavaScript `setTimeout(..., 450)` to control reveal timing after flap open

### 4) Customize fonts

Google Fonts are loaded in the `<head>`. Replace the font link and update:

- `font-family: 'Nunito', sans-serif;` (body text)
- `font-family: 'Baloo 2', sans-serif;` (display text)

## Behavior Notes

- Click handling is attached to `#envelope`.
- On click, class `open` is added to animate the flap.
- After delay, `#envelopeWrap` gets `hidden` and `#letterWrap` gets `visible`.
- Reduced-motion users are respected via `@media (prefers-reduced-motion: reduce)`.

## Browser Compatibility

Works in current versions of Chrome, Edge, Firefox, and Safari with modern CSS support.
