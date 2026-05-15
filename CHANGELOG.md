# Changelog

## v5.8 — Campaign, Name & Appearance Patch

- Evened out Campaign Generator spacing.
- Simplified the Campaign Generator intro copy for easier reading.
- Restored the Appearance dice randomizer at the top of the Appearance step.
- Reworked the Name step into a more meaningful character-naming moment.
- Added race and homeland naming guidance to the Name step.
- Enlarged and emphasized the character name input area.

## v5.8 — Final UI Readability Patch

- Simplified Campaign Generator layout into readable prose instead of technical info panels.
- Removed Character Dossier from Campaign Generator because character creation is already complete.
- Simplified GM Handoff visible How to Play steps to only player-needed actions.
- Kept canon-link enforcement inside the GM packet instead of exposing it in player-facing instructions.
- Fixed long Gear pill wrapping in Review and Dossier.
- Reworked Gear display into wrapping chips with cleaner max widths and tooltip support.
- Improved campaign archetype descriptions to focus on world texture, pressure, danger, and atmosphere.

## v5.8 — Tracker Schema & Randomizer Polish

- Added Faction Tie dice randomization with matching custom stat suggestions.
- Randomize dice for Origin, Background, and Faction Tie now appears only when Custom is selected.
- Moved custom randomize dice beside the custom text box with improved spacing.
- Expanded randomization datasets for custom Origin, Background, Faction Tie, Backstory, and Appearance.
- Aligned setup choice card descriptions and buttons more consistently.
- Removed the preset preview helper sentence.
- Restyled preset preview tooltips to match the gold stat-tooltip style and help cursor.
- Review now uses a floating Back / Create Character action bar.
- Campaign Generator descriptions now focus on world texture, scenery, atmosphere, faction pressure, danger shape, and opening feel.
- Expanded campaign generation combinations with opening place, sensory hook, rumor, complication, scarcity, and first meaningful choice.
- Updated GM packet campaign information to include the richer generated atmosphere.
- Updated GM_UPDATE_JSON to schemaVersion veinfire-progress-v2.
- Tracker import now supports campaignState, skillAdd/skillRemove, gear aliases, factionReputation, npcUpdate, and trackerNoteAdd.
- Campaign Tracker rendering no longer requires a completed character and better supports standalone imports.
- Progress JSON export now includes schemaVersion and campaignState.

## v5.8 — UI Flow Polish Patch

- Aligned the setup choice buttons so Create My Own and Choose Preset sit at the same visual level.
- Added more right-side padding to dropdowns so the arrow no longer sits against the border.
- Removed the generic preset preview sentence.
- Added hover tooltips for preset Race, Type, Class, and Origin cards.
- Review now hides the middle panel entirely with a smooth layout transition and expands the dossier.
- Added a Create Character action to the review dossier area.
- Floating Back / Next controls are fixed at the bottom of the screen during Creation Path.
- Removed description detail from Gender.
- Added dice randomizer buttons for Custom Origin, Custom Background, Backstory, and Appearance.
- Added randomization datasets for guided origin, background, backstory, and appearance prompts.
- Dice buttons jiggle when clicked.
- Required guided text boxes now use an asterisk marker.
- Improved Creation Path completion check marks.

## v5.8 — Welcome Flow & Tracker Polish

- Added a first-load Welcome page explaining what the VEINFIRE RPG Engine is and what players should expect.
- Added a setup choice page asking whether players want to create their own character or use a preset.
- Moved preset selection out of the Creation Path.
- Added a preset preview page with dossier and brief character details.
- Preset users can now proceed directly to campaign generation or edit the preset through the full Creation Path.
- Removed the header description because the Welcome page now handles engine explanation.
- Campaign Tracker is now fully standalone and no longer requires a completed character.
- Improved Campaign Tracker spacing and standalone helper text.
- Review step now expands the character dossier and visually collapses the middle review area.
- Campaign Generator archetype descriptions are laid out with factions, threat seeds, generated fields, and player control notes.
- Success toast alerts now default to green; preset alerts remain blue.
- Updated GM Handoff wording to rely on GitHub-hosted Markdown canon links.

## v5.8 — Creation Flow Polish

- Updated preset characters for the new guided Appearance flow.
- Moved presets to the top of the left panel and renamed Load Test Preset to Load Preset.
- Moved Name to the final creation step before Review and added race/homeland naming guidance.
- Reworked Appearance to use backstory-style guided fields with required-star labels.
- Made description/instruction panels visually distinct from player input boxes.
- Removed the Validate button entirely; completion is communicated through Creation Path check marks.
- Fixed Creation Path check marks, including Type discipline/proficiency and guided text sections.
- Added sticky floating Back/Next controls.
- Changed preset-loaded alerts to blue/info styling.

## v5.7 — Guided Navigation & Creation Fixes

- Removed the visible process-note sentence under the main navigation.
- Rewrote the engine description to explain the tool in VEINFIRE/player-facing terms.
- Character Creation path entries can now be clicked freely for previewing sections.
- Next/progression remains gated by required fields.
- Appearance is now split into multiple guided fields instead of one large text box.
- Removed section-level Validate button from character creation.
- Validation remains available at the final Review step.
- Accept and reject alerts now use distinct visual colors.

## v5.7 — Guided Navigation

- Reworked top navigation into the main session flow: Create Character → Generate Campaign → GM Handoff.
- Moved Campaign Tracker under Tools ▾ so it no longer appears as a required process step.
- Added a short process note explaining that the tracker is optional.
- Locked Generate Campaign until a character exists.
- Locked GM Handoff until a campaign exists.
- Updated page labels to use clearer player-facing wording.

## v5.6 — Forced GitHub Canon

- Removed the visible Canon Source Setup download panel from GM Handoff.
- Removed canon download/open buttons from the handoff flow.
- GM packet now directly instructs the AI GM to read the GitHub-hosted Markdown canon links before starting.
- If an AI platform cannot access the Markdown links, it must stop and ask for manual upload or pasted canon text.
- Updated How to Play steps to match the forced GitHub canon-link workflow.

## v5.5 — Markdown Canon Docs

- Updated canon links from `.docx` files to GitHub-hosted `.md` files.
- GM packet now points AI sessions to Markdown canon files for easier link-reading.
- Updated canon download/open labels and handoff wording to reference Markdown canon files.
- Kept manual upload/paste fallback if the AI platform cannot access GitHub-hosted Markdown links.

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
