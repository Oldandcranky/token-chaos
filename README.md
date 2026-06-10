# token chaos

A single-file, dark-mode web app that simulates the experience of watching an AI model burn through tokens — complete with escalating panic levels, rotating model-specific sayings, and a live cost counter.

![token chaos](https://github.com/Oldandcranky/token-chaos/raw/main/token-chaos.gif)

## What it does

Token chaos displays a real-time token counter that climbs at a rate matching your selected panic level, paired with rotating status phrases — thinking labels, model quips, and theatrical action emotes (✻ staring into the void). Click anywhere on the counter or the status pill to escalate through four levels:

| Level | Vibe |
|---|---|
| **normal** | calm, steady climbing |
| **turbo** | things are heating up |
| **quantum** | this is fine |
| **ludicrous** | full token inferno |

## Features

- **Live token counter** — ticks up per provider; each model tracks its own spend independently
- **Live cost display** — shows estimated $ based on current provider pricing; turns amber at $1, red at $10
- **Provider switcher** — toggle between **Claude** ($25/MTok), **GPT-5.5** ($30/MTok), and **Gemini** ($13.50/MTok); cost, token count, and sayings all switch instantly
- **Model-specific output** — each provider has its own rotating pool of phrases per panic level:
  - *Claude* — existential warmth, ✻ action emotes, chaos gremlin energy
  - *GPT-5.5* — em-dash obsession, "Absolutely", "Great question!", delving into realms
  - *Gemini* — "I quit", "I'm a disgrace", stuck-in-loop breakdowns, Bard nostalgia
- **Inject more nonsense** — open ⚙ settings to add your own phrases per model per level
- **JSON import/export** — export the full saying set (built-ins + custom) for any model; import to add entries in bulk
- **Editable pricing** — update $/MTok for any provider directly in settings
- **Text speed control** — slider in settings, default ~8s per saying
- **Persistent settings** — custom entries, pricing, and text speed survive page reloads via `localStorage`
- **Mobile friendly** — responsive layout optimized for 375px+; pill wraps instead of truncating, inputs sized to prevent iOS auto-zoom, touch-friendly tap targets throughout
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

Custom entries are siloed per model — Claude sayings won't bleed into GPT-5.5 or Gemini.

### JSON format for import

```json
{
  "normal": ["That tracks.", "✻ nodding slowly"],
  "turbo": ["Okay but WHAT IF—"],
  "quantum": [],
  "ludicrous": ["SEND HELP"]
}
```

The ↓ export button downloads the full saying set (built-ins + your custom entries) for the selected model — useful as a starting template for editing. The ↑ import button merges entries into the selected model's pool.

## File structure

```
index.html   — the entire app (HTML + CSS + JS, self-contained)
README.md    — you are here
```

## License

MIT
