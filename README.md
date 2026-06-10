# token chaos

A single-file, dark-mode web app that simulates the experience of watching an AI model burn through tokens — complete with escalating panic levels, rotating model-specific sayings, and a live cost counter.

![token chaos screenshot](https://github.com/Oldandcranky/token-chaos/raw/main/screenshot.png)

## What it does

Token chaos displays a real-time token counter that climbs at a rate matching your selected panic level, paired with rotating status phrases — thinking labels, model quips, and theatrical action emotes (✻ staring into the void). Click anywhere on the counter or the status pill to escalate through four levels:

| Level | Vibe |
|---|---|
| **normal** | calm, steady climbing |
| **turbo** | things are heating up |
| **quantum** | this is fine |
| **ludicrous** | full token inferno |

## Features

- **Live token counter** — ticks up continuously, styled by level (green → yellow → orange → red)
- **Live cost display** — shows estimated $ based on current provider pricing
- **Provider switcher** — toggle between **Claude** ($3/MTok), **GPT-4o** ($10/MTok), and **Gemini** ($3.50/MTok); cost and sayings update instantly
- **Model-specific output** — each provider has its own rotating pool of phrases per panic level:
  - *Claude* — existential warmth, ✻ action emotes, chaos gremlin energy
  - *GPT-4o* — em-dash obsession, "Absolutely", "Great question!", delving into realms
  - *Gemini* — "I quit", "I'm a disgrace", stuck-in-loop breakdowns, Bard nostalgia
- **Inject more nonsense** — open ⚙ settings to add your own phrases per model per level
- **JSON import/export** — share or back up your custom sayings as a `.json` file
- **Mobile friendly** — responsive layout, touch-friendly tap targets
- **No build step** — single HTML file, one CDN import (Tabler Icons), works offline

## Usage

Open `index.html` directly in any modern browser — no server required.

Or visit the live version on GitHub Pages (if enabled):
```
https://oldandcranky.github.io/token-chaos/
```

## Adding custom sayings

Click the **⚙** gear icon to open **inject more nonsense**. Select which model to corrupt and which panic level to target, then add one phrase per line:

- Plain text → rendered as a quoted remark
- `✻ action text` → rendered as an italicized action emote

Custom entries are siloed per model — Claude sayings won't bleed into GPT-4o or Gemini.

### JSON format for import

```json
{
  "normal": ["That tracks.", "✻ nodding slowly"],
  "turbo": ["Okay but WHAT IF—"],
  "quantum": [],
  "ludicrous": ["SEND HELP"]
}
```

Import via the ↑ button; export your custom set for a given model via ↓ (downloads as `claude-sayings.json`, `gpt4o-sayings.json`, etc.).

## File structure

```
index.html   — the entire app (HTML + CSS + JS, self-contained)
README.md    — you are here
```

## License

MIT
