# VEINFIRE RPG Engine

A beta prototype standalone browser-based setup engine for **VEINFIRE / Eldoria** RPG sessions.

Current build: **v6.0 — Class Gear System / Critical Fixes**

## What this engine is

The VEINFIRE RPG Engine helps players prepare for a VEINFIRE campaign with an AI GM.

It is used to:

- create a canon-aware VEINFIRE character
- choose or edit preset characters
- generate a campaign opening
- build a structured GM handoff packet
- support AI-led play in ChatGPT, Claude, Gemini, Grok, or another AI chat
- import GM updates into the Campaign Tracker
- track NPCs, relationships, injuries, inventory, consequences, advancement, and campaign state

The engine is not the live GM. The live campaign happens in the AI chat after the GM packet is copied.

## Main player flow

```text
Welcome → Character Setup → Generate Campaign → GM Handoff
```

The player can either create their own character or choose a preset character, then proceed directly or edit the preset first.

## v6.0 Class Gear System

Starting Gear is no longer a separate player-selected step.

Starting inventory now comes from:

```text
Class Gear + Personal Object
```

Class defines the practical tools the character has at the beginning of play. The Personal Object remains separate because it carries emotional, narrative, or personal weight rather than functioning as a normal equipment package.

## Campaign Tracker

The **Campaign Tracker** is a standalone tool under **Tools**.

It can import structured GM updates and display:

- current campaign state
- current conflict
- resources
- inventory
- advancement
- NPC cast
- NPC relationship scores
- NPC resistance states
- injuries
- relationship ledger
- chronicle entries
- visible consequences

The tracker supports:

```text
veinfire-progress-v4
```

## Canon source

The GM packet points the AI GM to the GitHub-hosted VEINFIRE Markdown canon files.

The AI GM is instructed to read the canon files before beginning canon-sensitive play. If the AI platform cannot access the links, it should ask the player or GM/session host to provide the required canon text manually.

## Project files

This repository contains:

- `index.html` — the VEINFIRE RPG Engine
- `README.md` — project overview and usage notes
- `CHANGELOG.md` — version history
- `NOTICE.md` — intellectual property and fan-use notice
- `canon-docs/` — VEINFIRE canon files used by the GM packet

## Intellectual Property and Fan Use

VEINFIRE, Eldoria, and all related lore, characters, terminology, factions, races, campaign material, and worldbuilding are original creative works by Kanniti Singsanan. All rights reserved.

Players and fans may use the VEINFIRE RPG Engine for personal, non-commercial gameplay, character creation, campaign generation, fan OCs, fanart, and session participation. Fan creations are welcome, but they do not grant ownership of VEINFIRE or become official canon unless approved by Kanniti Singsanan.

Do not sell, redistribute official lore documents, copy large portions of the source material, claim VEINFIRE as your own, create commercial derivative works, or use VEINFIRE materials for AI training, datasets, or prompt packs without written permission.

See [`NOTICE.md`](NOTICE.md) for the full intellectual property and fan-use notice.
