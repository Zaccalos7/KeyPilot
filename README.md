<img width="677" height="369" alt="keypilot" src="https://github.com/user-attachments/assets/17b71bc9-203e-46c3-b2d1-26cea97d1e0c" />


# Keypilot

Inline code completion for VSCode, powered by Gemini (or any OpenAI-compatible API).

## Install

1. Open this folder in VSCode → press **F5** → "Extension Development Host" opens with the extension loaded.
2. Or package it: `npm i -g @vscode/vsce && vsce package`, then install the generated `.vsix`.

## Setup

### Option 1: Gemini API key (free tier available)

1. Go to [Google AI Studio](https://aistudio.google.com/apikey) and create an API key.
2. In VSCode: **Keypilot: Set API Key** command, paste your key.

### Option 2: Groq API key (free)

1. Go to [Groq Console](https://console.groq.com/keys) and create an API key.
2. Set the key as above.
3. Change model to `llama-3.3-70b-versatile` (or `llama-3.1-8b-instant` for faster responses).
4. Set endpoint to `https://api.groq.com/openai/v1/chat/completions`.

### Option 3: Any OpenAI-compatible API

Set your API key, model name, and endpoint in settings — it works with any provider that exposes `/chat/completions`.

## Settings

| Setting | Default | Description |
|---|---|---|
| `keypilot.apiKey` | `""` | Your API key |
| `keypilot.model` | `gemini-3.1-flash-lite` | Model name |
| `keypilot.endpoint` | `https://generativelanguage.googleapis.com/v1beta/openai/chat/completions` | Chat completions URL |
| `keypilot.enabled` | `true` | Toggle suggestions on/off |
| `keypilot.maxContextChars` | `3000` | Max chars of context before cursor |

## Usage

Type code — ghost-text suggestions appear inline. Press **Tab** to accept.

## Commands

- **Keypilot: Test Completion** — quick test to check if it works
- **Keypilot: Set API Key** — set or change your API key
- **Keypilot: Reset Token Counter** — reset usage stats
- **Keypilot: Open Stats** — open stats view in sidebar

## Notes

- Sends code context to the API. Check your provider's data terms before use on private repos.
- No build step required — single `extension.js` file.
- Stats view available in the Keypilot sidebar panel.

## Support the team

<a href="https://buymeacoffee.com/zaccalos" target="_blank">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" height="40">
</a>
