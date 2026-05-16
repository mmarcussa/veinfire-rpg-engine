# VEINFIRE RPG Engine

**Current build:** v6.1 — Review Cleanup Patch  
**Status:** Beta prototype

VEINFIRE RPG Engine is a standalone browser-based setup tool for running heavy VEINFIRE / Eldoria RPG sessions with an external AI GM.

The engine helps players:

- create a canon-aware character
- choose or edit preset characters
- generate a campaign premise
- build a structured GM handoff packet
- use a standalone Campaign Tracker for GM update JSON imports

The live roleplay session happens in the chosen AI chat after the GM packet is copied.

## How to use

1. Open the hosted page.
2. Start from the Welcome screen.
3. Choose whether to create your own character, resume character creation, or use a preset.
4. Generate a campaign.
5. Build the GM packet.
6. Copy the GM packet into your chosen AI chat.
7. Use the Campaign Tracker if your GM provides tracker update JSON.

## Hosting

This is a standalone static HTML project. It does not require a backend.

It can be hosted on:

- GitHub Pages
- Netlify
- Vercel
- itch.io
- any static web host

For GitHub Pages, the main file must be named:

```text
index.html
```

## Recommended repository structure

```text
index.html
README.md
CHANGELOG.md
NOTICE.md
```

## Canon documents

The GM packet is designed around GitHub-hosted Markdown canon documents. If an AI model cannot access GitHub links, it should ask the player or session host to paste or upload the needed canon text manually.

## Important notes

- The HTML does not directly call ChatGPT, Gemini, Grok, Claude, or any other AI.
- The browser page is the character / campaign / tracker engine.
- The AI chat is the live GM / Narrator.
- Campaign Tracker imports should use valid JSON only.
- The project is still a beta prototype, so testers should report bugs, confusing UI, and broken tracker updates.

## Ownership and fan creations

VEINFIRE, Eldoria, related lore, canon material, names, worldbuilding, characters, factions, and setting concepts are owned by the creator.

Players and fans may create personal, non-commercial fan works such as fanart, OCs, session notes, and private play materials, as long as they do not claim ownership of the canon IP or present fan material as official canon.

See `NOTICE.md` for more detail.
