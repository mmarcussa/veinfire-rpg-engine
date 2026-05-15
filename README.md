# VEINFIRE RPG Engine

A standalone browser-based character creation, campaign generation, GM handoff, and progress tracking tool for **VEINFIRE / Eldoria**.

Current build: **v5.6 — Forced GitHub Canon**

## What this tool does

The VEINFIRE RPG Engine helps players:

- create a character through a structured character creation path
- validate character details against VEINFIRE canon rules
- choose race, gender, type, discipline/proficiency, class, origin, background, gear, faction tie, flaw, goal, secret, appearance, backstory, and personal object
- load preset test characters
- generate a procedural campaign setup
- prepare a GM handoff packet for AI-assisted play
- download canon documents for the GM session
- track campaign progress through imported GM updates
- maintain inventory, resources, advancement, NPCs, chronicle, and consequence ledgers

## How to use

1. Open `index.html` in a browser.
2. Go to **Character Creation**.
3. Create a character manually or use **Load Test Preset**.
4. Complete all required fields.
5. Go to **Campaign Setup**.
6. Choose a campaign archetype.
7. Click **Generate Campaign**.
8. Go to **GM Handoff**.
9. Select the AI model you want to use.
10. Use **Download All Canon Docs** or individual canon file downloads if your AI cannot access the GitHub-hosted Markdown canon links.
11. Click **Build GM Packet**.
12. Click **Copy Packet**.
13. Paste the packet into your AI chat session.
14. Start playing.

## Canon document flow

The GM packet gives the AI direct links to the GitHub-hosted VEINFIRE Markdown canon files.

If the AI cannot access the GitHub-hosted Markdown canon links, the player should:

1. Click **Download All Canon Docs** inside the HTML.
2. Upload the downloaded files manually to the AI chat.
3. Paste the GM packet.
4. Tell the AI to start the session.

## Progress Tracker

The **Progress Tracker** tab starts blank.

To use it:

1. Export or request a structured `GM_UPDATE_JSON` block from the AI GM.
2. Paste the JSON into **Import GM Update**.
3. Click **Import GM Update**.
4. The tracker will update resources, inventory, progression, NPCs, chronicle entries, and ledgers.

Manual tracker editing is disabled until progress data has been imported.

## Files

Recommended GitHub structure:

```text
index.html
README.md
CHANGELOG.md
```

Only `index.html` is required for GitHub Pages or Netlify hosting, but `README.md` and `CHANGELOG.md` are strongly recommended.

## Hosting

This is a standalone static HTML project. It does not require a backend.

It can be hosted on:

- GitHub Pages
- Netlify
- Vercel
- itch.io
- any static web host

## Important notes

- The HTML does not directly call ChatGPT, Gemini, Grok, Claude, or any other AI.
- The live campaign happens in the AI chat after the GM packet is copied.
- The HTML is the character/campaign/control panel.
- The AI chat is the GM/Narrator.
- Browser download behavior may block multiple automatic downloads. If that happens, use the individual canon download buttons.
