# VEINFIRE RPG Engine

**Current build:** v6.2 — Raw Canon Links  
**Status:** Beta prototype

VEINFIRE RPG Engine is a standalone browser-based setup tool for running heavy VEINFIRE / Eldoria RPG sessions with an external AI GM.

The engine helps players create a canon-aware character, choose or edit preset characters, generate a campaign premise, build a structured GM handoff packet, and use a standalone Campaign Tracker for GM update JSON imports.

## v6.2 canon access note

The GM packet now uses **raw GitHub Markdown URLs** for canon documents instead of GitHub Pages Markdown URLs.

This helps AI GM tools open the exact source text directly instead of searching by document title and possibly finding unrelated results.

If the selected AI model still cannot access the raw links, it should ask the player or session host to paste or upload the canon document text manually before canon-sensitive play begins.

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

For GitHub Pages, the main file must be named:

```text
index.html
```

Recommended repository structure:

```text
index.html
README.md
CHANGELOG.md
NOTICE.md
```

## Important notes

- The HTML does not directly call ChatGPT, Gemini, Grok, Claude, or any other AI.
- The browser page is the character / campaign / tracker engine.
- The AI chat is the live GM / Narrator.
- Campaign Tracker imports should use valid JSON only.
- The project is still a beta prototype.


## v6.2 player clarity patch

The GM packet now instructs the AI GM to:

- show a compact live status line at the top of normal play responses
- visibly show stat checks, dice rolls, modifiers, DC/opposition, and success/failure result
- label suggested actions as optional examples, not fixed choices
- remind players they may type any action in their own words
