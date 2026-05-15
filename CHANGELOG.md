# Changelog

## v5.4 — Canon Download Cleanup

- Removed **Open All Download Links**.
- Removed the collapsible **Canon Google Doc URLs** section.
- Kept:
  - **Download All Canon Docs**
  - **Show Individual Downloads**
- Updated canon setup wording.
- Updated the **How to Play** steps to match the simplified canon document flow.
- Confirmed JavaScript syntax check passes.

## v5.3 — Multi Canon Download

- Added **Download All Canon Docs**.
- Added sequential multi-download attempts for all five canon documents.
- Kept individual download links as a fallback.
- Added note explaining browser multiple-download permission behavior.
- Confirmed JavaScript syntax check passes.

## v5.2 — Reliable Canon Downloads

- Replaced unreliable automatic multi-download behavior with one download button per document.
- Added **Show Canon Download Links**.
- Added download links using Google Docs `.docx` export URLs.
- Added fallback behavior for browsers that block automatic downloads.
- Confirmed JavaScript syntax check passes.

## v5.1 — VEINFIRE Handoff Cleanup

- Removed BG3 wording from the header.
- Removed irrelevant `Character Creation · 200 CR / 150 VR` text.
- Review page no longer shows the warning box.
- Dossier spacing normalized.
- Type and Discipline/Proficiency integrated into the **Selections** table.
- Major pages and top navigation centered more cleanly.
- Removed **Embedded Summary Mode**.
- GM packet now assumes Google Doc URL access first.
- Added **Download Canon Docs** button.
- GM packet instructs the AI:
  - try to access/read the Google Doc URLs first
  - confirm access to each document
  - ask the player to download and upload docs manually if access fails
  - never pretend it accessed docs it cannot read
- Confirmed JavaScript syntax check passes.

## v5.0 — Canon Source Setup

- Added **Canon Source Setup** section to GM Handoff.
- Added three canon modes:
  - Uploaded Docs Mode
  - Google Doc URL Mode
  - Embedded Summary Mode
- Added canon Google Doc URLs:
  - VEINFIRE: Sensory Descriptions v5
  - VEINFIRE: Worldbuilding v5
  - VEINFIRE: Complete Timeline v5
  - VEINFIRE: Terminology v5
  - VEINFIRE: Writer Personal Note v5
- GM packet instructs AI to confirm document access before starting.

## v4.9.1 — Structured GM Updates Fix

- Fixed JavaScript syntax issue caused by Markdown code fences inside the GM packet template.
- GM packet still includes structured GM update instructions.
- Confirmed JavaScript syntax check passes.

## v4.9 — Structured GM Updates

- Added required **GM_UPDATE_JSON** structure to GM packet.
- Added import-compatible fields:
  - resources
  - inventoryAdd
  - inventoryRemove
  - permanentGrowthAdd
  - conditionalGrowthAdd
  - temporaryEffectsAdd
  - scarsConsequencesAdd
  - trainingProjectsAdd
  - storyRewardsAdd
  - playerFacingLedgerAdd
  - milestones
  - tier
  - unspentGrowth
  - npcAdd
  - campaignNotesAdd
  - chronicleAdd
- Instructed GM not to include hidden clocks, secret motives, undiscovered lies, or offscreen spoilers in player-facing JSON.

## v4.8 — Locked Handoff & Import Tracker

- GM packet hidden by default.
- Player must select AI model before building packet.
- GM packet is read-only by default.
- Added guarded **Edit Packet** mode with confirmation prompt.
- Progress Tracker starts blank.
- Progress data only appears after import.
- Manual Tracker Editor disabled until progress data is imported.
- Added file import for progress data.

## v4.7 — Handoff & Progress Tracker

- Cleaned GM Handoff page.
- Added AI model buttons:
  - ChatGPT
  - Gemini
  - Grok
  - Claude
- Added separate **Progress Tracker** tab.
- Moved Campaign State, Advanced Trackers, NPC Cast, and Chronicle out of GM Handoff.
- Added Import GM Update.
- Added Manual Tracker Editor.
- Added Export Progress JSON.
- Added Download Progress Save.

## v4.6 — Resolution Flow

- Added correct play sequence to GM packet:
  - describe scene
  - player acts
  - GM decides if check is needed
  - resolve action/check
  - narrate visible outcome
  - privately update hidden consequences
  - ask what the player does next
- Added Player-Facing Ledger.
- Added Hidden GM Ledger.
- Clarified what should and should not be shown to the player.

## v4.5 — Advancement System

- Added Tier system.
- Added Milestones.
- Added Unspent Growth tracker.
- Added Permanent Growth tracker.
- Added Conditional Growth tracker.
- Added Temporary Effects tracker.
- Added Scars / Consequences tracker.
- Added Training Projects tracker.
- Added Story Rewards tracker.
- Added recommended Health formula:
  - `Max Health = 10 + Body × 3 + Tier × 2`
- Added advancement rules to GM packet.

## v4.4 — Preset Gear Layout Fix

- Removed old placeholder gear:
  - `personal tool`
  - `worn travel kit`
- Added sanitizer so old placeholder items cannot appear in Gear/Inventory.
- Gear now comes only from:
  - Starting Gear
  - Personal Object
- Long gear text wraps properly.
- Preset dropdown uses shorter display labels.

## v4.3 — Gear Cleanup

- Removed discipline-focus items from Gear.
- Added sanitizer so discipline names cannot appear in Gear/Inventory.
- Removed extra Type header in dossier.
- Gear now has unique flavor text and unique use text.
- Personal objects generate context-sensitive descriptions.

## v4.2 — Compact Dossier

- Moved repeated gear/session-use logic into Notes and GM packet.
- Dossier Starting Skills are compact with hover tooltips.
- Dossier Gear is compact with hover tooltips.
- Added separate Type section in dossier.
- Generate Campaign proceeds to GM Handoff and builds packet.

## v4.1 — Skill & Gear Usage

- Starting skills show descriptions in creation sections.
- Race skills show in Race section.
- Class skills show in Class section.
- Gear and Inventory include short descriptions and usage guidance.
- GM packet includes skill and gear descriptions.
- Added support for newly gained skills and gear during play.

## v4.0 — Expanded Campaigns

- Removed page-level Back/Next buttons.
- Navigation only through top tabs.
- Added 10 campaign archetypes:
  - Vein Carnival
  - Blood Ledger
  - Glass Court Masquerade
  - Dead Bell Monastery
  - Red Market Auction
  - Salt Marsh Covenant
  - Frostwake Convoy
  - Ash Pit Rebellion
  - Mirror Clinic
  - Skychain Mutiny
- Added Inventory to tracked state and GM packet.

## v3.9 — Campaign Navigation

- Added top navigation:
  - Character Creation
  - Campaign Setup
  - GM Handoff
- Added navigation flow between creation, campaign setup, and handoff.
- Added GM rules:
  - NPCs can be newly generated during campaign
  - difficulty can change dynamically
  - GM only describes what the player character can perceive or infer

## v3.8 — Preset Main Characters

- Added Load Test Preset selector.
- Added 5 preset main characters:
  - Jereq Quilmik
  - Maeva Thorne
  - Orruk Deepcut
  - Sable Vey
  - Torun Red-Horn
- Removed Whore-specific fade-to-black restriction from GM handoff.

## v3.7 — Whore Class

- Added Whore class.
- Added sexually oriented starting skills.
- Added Whore’s Kit.
- Added whore-based faction ties:
  - Brothel House
  - Courtesan Circle
  - Streetwalkers’ Mutual

## v3.6 — Gender, Classes, Skills

- Added Gender:
  - Male
  - Female
- Added Class step.
- Added class starting skills.
- Added race starting skills.
- GM packet includes gender, class, and starting skills.

## v3.5 — GM Handoff Mode

- Removed fake/scripted live chat focus.
- Added Build GM Packet.
- Added Copy Packet.
- GM packet includes character, campaign, stats, gear, NPCs, opening incident, and GM rules.

## v3.4 — Chat Session

- Added scripted chatbot-like live session.
- Player could type actions into the HTML.
- Engine reacted with simple keyword logic.
- Later replaced by GM Handoff model.

## v3.3 — Random Campaign Setup

- Removed player-selected region.
- Starting region generated randomly every run.
- Added Whore House campaign archetype.
- Removed left Ready panel.

## v3.2 — Structured Backstory Fix

- Fixed Backstory step so structured multi-box backstory layout actually rendered.

## v3.1 — Structured Backstory

- Backstory split into:
  - Origin Point
  - Pressure or Burden
  - Turning Incident
  - Living Tie
  - Reason to Enter the Campaign
  - Optional Other Details

## v3.0 — Guided Backstory

- Added guided required backstory fields.
- Moved repeated guidance out of option descriptions.
- Option descriptions expanded and made more specific.

## v2.9 — Fresh Character Creation

- New iteration starts from a fully blank character creation state.
- No prior selections, campaign, NPCs, or play state carried over.

## v2.8 — Uploaded-Docs Lore Validator

- Added uploaded-docs-only lore validator rule set.
- Validator grounded in v5 document rules embedded from uploaded chat files.

## v2.7 — Lore Validator

- Added placeholder/low-effort text rejection.
- Rejected entries like `test`, `asdf`, `???`, `none`, `todo`.

## v2.6 — Character Creation Fixes

- Removed default custom stats.
- Added review-only Validate button.
- Improved page gating and descriptions.

## v2.5 — Character Creation Polish

- Added custom stat assignment.
- Added dialogue-style Flaw, Goal, Secret.
- Added tooltip validation.
- Added dossier improvements.

## v2.4 and earlier

- Early BG3-inspired character creation prototype.
- Added race/type/discipline/proficiency handling.
- Added compact cards, dossier, gear, lore warnings, and stat tradeoffs.
