# token chaos

A single-file, dark-mode web app that simulates the experience of watching an AI model burn through tokens — complete with escalating urgency levels, rotating "claudeisms," and a live token counter.

![token chaos screenshot](https://github.com/Oldandcranky/token-chaos/raw/main/screenshot.png)

## What it does

Token chaos displays a real-time token counter that climbs at a rate matching your selected panic level, paired with rotating status phrases — thinking labels, model quips ("I cannot and will not"), and theatrical action emotes (✻ staring into the void). Click anywhere on the counter or the status pill to escalate through four levels:

| Level | Vibe |
|---|---|
| **normal** | calm, steady climbing |
| **turbo** | things are heating up |
| **quantum** | this is fine |
| **ludicrous** | full token inferno |

## Features

- **Live token counter** — ticks up continuously, styled by level (green → yellow → orange → red fire animation)
- **Elapsed time** — shows how long you've been watching the chaos unfold
- **Claudeisms** — a curated pool of AI-flavored phrases, quotes, and action emotes that rotate at each level
- **Custom claudeisms** — open settings (⚙) to add your own phrases targeted at any level; stored in `localStorage`
- **No dependencies** — single HTML file, one CDN import (Tabler Icons for the gear icon), works offline

## Usage

Open `index.html` directly in any modern browser — no build step, no server required.

Or visit the live version on GitHub Pages (if enabled):
```
https://oldandcranky.github.io/token-chaos/
```

## Customizing phrases

Click the **⚙** gear icon to open the settings modal. Add one phrase per line:

- Plain text → rendered as a quoted remark
- `✻ action text` → rendered as an italicized action emote

Select the target panic level before adding so your phrases appear at the right intensity.

Custom entries are saved to `localStorage` and survive page refreshes.

## File structure

```
index.html   — the entire app (HTML + CSS + JS, self-contained)
README.md    — you are here
```

## License

MIT
