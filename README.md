# Tiny Chat Client

A tiny, dependency-free AI chat client that works with any OpenAI-compatible API.

Single HTML file. No build step. No backend. Open it and chat.

## Features

- Works with any OpenAI-compatible endpoint (`/v1/chat/completions`)
- Streaming responses
- Multiple saved endpoints (switch between providers)
- Model picker with free-text model input
- Temperature / max tokens controls
- Chat history kept in `localStorage` (never leaves your browser)
- Export / import conversations as JSON
- Dark theme

## Quick start

1. Download `index.html`
2. Open it in a browser (double-click, or serve with `python -m http.server`)
3. Click the gear icon, enter:
   - **Base URL** — e.g. `https://api.openai.com/v1`
   - **API key** — your key
   - **Model** — e.g. `gpt-4o-mini`
4. Start chatting

## Using your own relay

If you run an OpenAI-compatible relay (one-api / new-api / LiteLLM), point the
Base URL at it:

```
http://localhost:3000/v1
```

All requests are sent from your browser directly to the endpoint you configure.
The key is stored only in `localStorage`.

## Browser notes

The upstream must allow CORS from the origin you open this file from
(`file://` or `http://localhost`). If it does not, put a small proxy in front.

## License

MIT
