# AI Hub

A polished, dependency-free AI chat workspace designed for GitHub Pages.

## Deploy

1. Open `app.js` and replace the three clearly marked `PUT_*_KEY_HERE` values with restricted, low-quota provider keys.
2. Upload these files to a GitHub repository.
3. Enable **GitHub Pages** in the repository settings.
4. Open the published URL.

There is no install, build command, backend, database, or user API-key screen. Conversations are stored only in the visitor's browser using `localStorage`.

> **Security note:** GitHub Pages is static hosting, so keys placed in `app.js` can be discovered by site visitors. Only use burner/restricted keys with small quotas.

## Providers

The owner can add or remove models in the `PROVIDERS` object in `app.js`. AI Hub includes adapters for OpenAI Chat Completions, Google Gemini `generateContent`, and Anthropic Messages APIs. Anthropic browser calls include Anthropic's required direct-browser access header.

## If a chat cannot connect

AI Hub now shows the provider name and actionable checks instead of only the browser's generic `Failed to fetch` error. Verify that the key was pasted exactly, the selected model is enabled for that key, and a browser extension, corporate network, or firewall is not blocking the provider request.
