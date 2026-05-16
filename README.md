# VEINFIRE RPG Engine

A standalone browser-based setup engine for **VEINFIRE / Eldoria** RPG sessions.

Current build: **v5.9 — NPC Agency, Combat & Relationship v4**

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

The player can either:

1. create their own character, or
2. choose a preset character, then either proceed directly or edit the preset first.

After the campaign is generated, the player builds the GM packet, copies it, and pastes it into their chosen AI chat.

## Campaign Tracker

The **Campaign Tracker** is a standalone tool under **Tools**.

It is not required to create a character or start a campaign.

The tracker can import structured GM updates and display:

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

## v5.9 NPC / Combat / Tracker Update

This build improves live-session behavior and tracker compatibility.

NPC relationships now use a **-10 to +10** scale:

```text
-10 Nemesis
 -9 Hated
 -8 Vengeful
 -7 Dangerous Enemy
 -6 Active Enemy
 -5 Hostile
 -4 Resentful
 -3 Distrustful
 -2 Wary
 -1 Uneasy
  0 Neutral
 +1 Familiar
 +2 Cordial
 +3 Warm
 +4 Friendly
 +5 Trusting
 +6 Loyal
 +7 Devoted
 +8 Deep Bond
 +9 Unshakable Bond
+10 Life-Bound
```

The GM packet now includes stronger rules for:

- shorter, playable AI responses
- player intent versus outcome control
- NPC agency
- NPC resistance
- social conflict
- combat positioning
- injuries
- relationship memory
- consequence tracking

The tracker now supports:

```text
veinfire-progress-v4
```

This schema supports NPC relationship updates, combat state, current conflict, injuries, relationship ledgers, and expanded NPC memory.

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
