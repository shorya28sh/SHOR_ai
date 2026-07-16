# SHOR.ai

A chatbot website with three modes: **Chat**, **Image**, and **Video**.

## How to run

No build step, no install — just open `index.html` directly in any browser
(double-click it, or right-click → Open with → Chrome/Firefox/Edge).

⚠️ Do **not** open it inside Claude's inline preview pane — that sandbox blocks
external network requests, so image generation won't load there. A normal
browser tab has no such restriction.

## What each mode does

- **Chat** — real conversation, powered directly by Claude (no API key needed,
  it's built into how this file calls the Anthropic API).
- **Image** — type a description, get a real AI-generated image back
  (free, no-key API: image.pollinations.ai).
- **Video** — takes your prompt and shows the interaction flow. Full AI video
  generation needs a paid video-model API (Runway, Pika, Luma) plugged in —
  good talking point for judges: "here's the UX, here's where generation
  would connect."

## Troubleshooting

- **Image generation fails to load:** usually flaky/firewalled wifi blocking
  `image.pollinations.ai`. Test by pasting this in your browser address bar:
  `https://image.pollinations.ai/prompt/a%20dog` — if that doesn't load, it's
  the network, not the site. Switch to mobile hotspot if needed.
- **Chat doesn't respond:** check your internet connection; the chat call
  goes out to the Anthropic API over HTTPS.

## Rebranding

To rename the bot, search `index.html` for `SHOR` and swap it — it appears in
the page title, header logo, and the bot's reply label.
