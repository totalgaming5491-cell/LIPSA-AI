# Lipsa AI 2.0

This project keeps the original Lipsa AI interface and changes its AI connection so the browser calls a server endpoint (`/api/chat`). The provider API key stays on the server, not in the HTML file.

## Included

- `public/index.html` — your Lipsa AI interface, adapted for a normal website.
- `server.js` — a small Node.js server and secure AI proxy.
- `package.json` — project dependencies.
- `.env.example` — configuration template. Do not put real keys in GitHub.

## Important

GitHub Pages only hosts static files. It cannot run `server.js`. To make AI chat work online, deploy this whole project to a host that supports Node.js, then add these environment variables in that host's settings:

- `ANTHROPIC_API_KEY` — your provider API key.
- `ANTHROPIC_MODEL` — a currently supported model ID from your provider.

Ask a parent or trusted adult to help with any provider account, API access, or billing setup. Never post your API key in chat, screenshots, HTML, or a public repository.

## Run locally (computer required)

1. Install Node.js 18 or newer.
2. Copy `.env.example` to `.env`.
3. Fill in the two AI environment variables in `.env`.
4. Run `npm install`.
5. Run `npm start`.
6. Open `http://localhost:3000`.

## Android note

You can edit and upload the project from an Android phone, but running/deploying the Node.js backend requires a Node-compatible hosting service. The HTML alone cannot securely hold an API key.

## Current limitations

- Voice replies use the voices available on the device/browser; the app cannot guarantee a specific female voice.
- Voice input depends on browser support for Speech Recognition.
- Photo understanding is not connected in this first independent version.
- Chat history and basic memory are stored in the browser on that device. They are not encrypted cloud sync.
