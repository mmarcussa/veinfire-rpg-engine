# Changelog

## v6.1 — Safety, Tracker Schema, Preset, Background & Review Cleanup

- Added confirmation before actions that discard unfinished character creation work.
- `Create My Own` now asks before wiping unfinished character creation.
- Preset edit/proceed actions now ask before replacing unfinished character work.
- `createCharacter()` now returns success/failure and supports silent success mode.
- Preset proceed flow now stops if character validation fails.
- Restored missing preset guards for edit/proceed flows.
- Persisted selected AI model in save state.
- Restored selected AI model button highlight after reload/render.
- Removed dead `beginWelcome()` code.
- Relationship examples now match the `-10` to `+10` scale.
- Relationship labels are derived automatically from numeric value.
- Removed old `-3/+3` relationship helper code.
- Added explicit preset trope mapping for all preset characters.
- Fixed Torun Red-Horn displaying his personal name instead of `Field Medic` in the preset dropdown.
- Simplified preset trope labeling to avoid fragile personal-name regex guessing.
- Fixed Background display so it no longer shows Origin content.
- Hardened Campaign Tracker progression lists against missing ledger fields.
- Updated `applyProgressData()` with light schema prefix validation.
- Fixed `activePressure` rendering.
- Added `injuriesAdd` to the GM update schema.
- Simplified `inventoryAdd` and `skillAdd` examples to string arrays.
- Prevented `memoryAdd` from polluting NPC objects.
- Wrapped GM update import in try/catch with an error toast.
- Fixed the GM update textarea so example JSON is placeholder text only, not pre-filled real content.
- Fixed Download All Canon so Markdown canon files download with `.md` filenames instead of incorrect `.docx` filenames.
- Escaped Campaign Log rendering to prevent raw HTML injection from stored log entries.
- Added a 500-entry cap to campaign logs to prevent long-term save bloat.
- Removed duplicate `randomButton()` declaration.
- Aligned `freshState().progression` with `defaultProgression()`.
- Escaped preset dropdown option values.
- Removed unreachable legacy button wiring for missing `randomBtn`, `presetBtn`, and `resetBtn`.
- Renamed the inner canon download loop function from `next()` to `triggerNext()` for clarity.

## v6.0 — Class Gear System / Critical Fixes

- Removed the separate Starting Gear selection step from Character Creation.
- Moved starting inventory into Class gear packages.
- Each class now provides both starting skills and class-specific gear.
- Final starting inventory now comes from Class Gear + Personal Object.
- Updated Class section to show Skills and Gear in a cleaner layout.
- Updated Character Dossier labels:
  - `Class Gear & Personal Object` → `Inventory`
  - `Starting Skills` → `Skills`
- Added clickable skill icons.
- Skill name and description now appear only after clicking a skill icon.
- Clicking the same skill icon again closes the skill detail.
- Reworked Class Gear into a left-side gear list with a right-side description panel.
- Gear descriptions open on click and close when clicking the same gear item again.
- Removed icons from Flaw, Goal, and Secret options.
- Added Resume Character Creation option when unfinished character data exists.
- Added Back to Begin button from Character Creation to the setup choice page.
- Moved Generate Campaign button to the right side of the Generate Campaign page.
- Added Beta Prototype badge to the header.
- Added All Rights Reserved footer notice.
- Moved section notes into closable blue help popups opened by `?` buttons.
- Reduced the section help `?` button size.
- Rebuilt Character Creation navigation as a dedicated global fixed action bar.
- Widened the global Character Creation floating action bar.
- Fixed startup so the engine always opens on the Welcome page while preserving saved data.
- Fixed `load()` so it reads from `localStorage` instead of deleting the save key on page load.
- Updated `npcRelationship` import to accept both array and object formats.
- Aligned the GM packet relationship schema with the readable array format.
- Corrected relationship scale wording to `-10 to +10`.
- Copy confirmation uses the selected AI model instead of hardcoding ChatGPT.
- Added a dedicated `name` validation mode so short names like Kai, Eli, or Sam are accepted.
- Removed `renderAll()` backstory mutation.
- Removed duplicate `class="toast"` attribute.
- Consolidated random dice button helper logic.

## v5.9 — NPC Agency, Combat & Relationship v4

- Added GM behavior rules to reduce wall-of-text replies.
- Added response pacing rules:
  - 2–5 short paragraphs by default
  - maximum 3 sentences per paragraph
  - 2–4 options maximum when options are useful
  - end with “What do you do?” or a clear playable prompt
- Added Player Input Authority Rule:
  - player controls intent/action
  - GM controls outcome, NPC reaction, hidden truth, resistance, and consequences
- Added Intent → Method → Resistance → Outcome action resolution.
- Added Yes/And, Yes/But, No/But, No/And outcome framing.
- Added NPC resistance rules so NPCs do not instantly comply.
- Expanded NPC relationship scale from `-3/+3` to `-10/+10`.
- Added relationship labels from Nemesis to Life-Bound.
- Added relationship clamping and relationship bar UI support.
- Added gradual relationship-shift rules to the GM packet.
- Strengthened NPC agency rules:
  - wants
  - fears
  - boundaries
  - leverage
  - memory
  - stress response
  - voice
- Clearly separated relationship from resistance.
- Added social conflict rules so persuasion, intimidation, seduction, deception, and interrogation do not become mind control.
- Added combat behavior rules covering:
  - position
  - range
  - cover
  - terrain
  - morale
  - noise
  - legal heat
  - bystanders
  - escape routes
  - injuries
  - consequences
- Added injury tracking support.
- Updated GM_UPDATE_JSON to schemaVersion `veinfire-progress-v4` during development.
- Tracker import supports:
  - currentConflict
  - combatState
  - injuriesAdd
  - relationshipLedgerAdd
  - expanded npcUpdate
  - memoryAdd
  - `npcRelationship` using `-10` to `+10`
- Progress save export uses `veinfire-progress-save-v4`.

## v5.8 — Welcome Flow, Creation Polish & Tracker Foundation

- Added Welcome page as the first player-facing screen.
- Added “How do you want to begin?” setup choice flow.
- Moved preset selection out of the Creation Path.
- Added preset preview with character dossier.
- Added options to proceed directly from preset or edit preset details first.
- Improved Character Creation navigation.
- Removed per-section Validate buttons.
- Moved validation/status into Creation Path completion checks.
- Added required `*` indicators instead of explicit REQUIRED labels.
- Added guided Appearance section with multiple boxes.
- Added dice randomizers for:
  - Custom Origin
  - Custom Background
  - Custom Faction Tie
  - Backstory
  - Appearance
- Expanded randomization datasets.
- Added tooltips for preset preview sections.
- Improved Review page behavior.
- Improved Campaign Generator readability.
- Expanded campaign generation combinations:
  - opening place
  - sensory hook
  - local rumor
  - opening complication
  - scarcity pressure
  - first meaningful choice
- Improved Campaign Tracker standalone behavior.
- Updated tracker import/export foundations.
- Added `veinfire-progress-v2` and later tracker compatibility work during the v5.8 cycle.

## v5.7 — Guided Navigation

- Reworked top navigation into the main flow:
  - Create Character
  - Generate Campaign
  - GM Handoff
- Moved Campaign Tracker under Tools.
- Clarified that Campaign Tracker is a standalone tool, not part of the main play-start process.
- Removed confusing main-session-flow explanatory text.
- Improved player-facing engine description.
- Allowed players to click around Creation Path sections more freely.
- Removed Validate buttons from each Character Creation section.
- Added Creation Path checkmark/status logic.
- Improved alert color handling:
  - success = green
  - preset/info = blue
  - rejection/error = red

## v5.6 — Forced GitHub Canon

- Removed visible Canon Source Setup from GM Handoff.
- Updated GM packet to assume GitHub canon access by default.
- GM packet instructs the AI GM to read GitHub-hosted Markdown canon links before starting.
- Added fallback instruction: if the AI model cannot access the links, it must ask the player/session host to provide the canon text manually.
- Removed unnecessary player-facing Google Docs download instructions after canon moved to GitHub.
- Removed outdated canon-link panels from the GM Handoff UI.

## v5.5 — Markdown Canon Docs

- Updated canon document workflow from `.docx` to GitHub-hosted `.md` files.
- Updated GM packet wording to reference Markdown canon files.
- Confirmed Markdown is easier for AI chat access than `.docx`.
- Updated canon references to v5.5 after repo upload.
- Maintained manual upload/paste fallback if the AI platform cannot access GitHub links.
- Canon files expected in repo:
  - `VEINFIRE_ Complete Timeline v5.5.md`
  - `VEINFIRE_ GM Note v5.5.md`
  - `VEINFIRE_ Sensory Descriptions v5.5.md`
  - `VEINFIRE_ Terminology v5.5.md`
  - `VEINFIRE_Worldbuilding v5.5.md`

## v5.4 — Public Repo Cleanup

- Prepared public-facing GitHub materials.
- Added README.
- Added CHANGELOG.
- Added NOTICE/IP and fan-use language.
- Clarified that players and fans may make personal, non-commercial fan creations.
- Clarified that fan creations do not transfer ownership or become canon unless approved.
- Removed old setup/hosting guidance from the public README after it became irrelevant.
- Added repo/project structure guidance during setup phase.

## v5.3 — GitHub / Netlify Hosting Preparation

- Prepared the engine for GitHub Pages hosting.
- Prepared the engine for Netlify hosting.
- Clarified that a custom domain is optional.
- Discussed hosting canon docs in the GitHub repo.
- Moved away from relying on Google Docs as the main canon source.
- Clarified that AI chat cannot reliably fetch and upload documents into a session automatically.
- Added instructions for AI models to use links when possible and ask for manual canon text when not possible.

## v5.2 — Canon Docs Download / Link Workflow

- Added canon document link/download workflow concepts.
- Added multi-download support attempts.
- Removed extra Google Doc collapsible sections after canon workflow changed.
- Simplified How to Play steps around canon document access.
- Removed irrelevant “Canon Google Doc URLs” panels from GM Handoff once the approach changed.

## v5.1 — GM Handoff Simplification

- Simplified GM Handoff so it initially shows only the necessary player-facing controls.
- GM Session Packet remains hidden until the player selects an AI model and clicks Build GM Packet.
- Added AI model choices:
  - ChatGPT
  - Gemini
  - Grok
  - Claude
- Made GM Session Packet locked by default.
- Added edit confirmation behavior for packet editing.
- Moved Campaign State, Advanced Trackers, NPC Cast, Chronicle, and similar material into tracker/tool concepts instead of the primary GM Handoff panel.
- Added Import GM Update / manual tracker editor concepts.

## v5.0 — GM Packet and Tracker Compatibility

- Added GM packet structure for AI-led play sessions.
- Added tracker JSON structure alignment with GM packet expectations.
- Added rules telling the GM to maintain tracker-compatible JSON updates.
- Added support concepts for:
  - Campaign State
  - Advanced Trackers
  - NPC Cast
  - Chronicle
  - Progress Tracker imports
- Clarified what is shown to the player versus what is tracked silently.
- Added consequence/outcome rules for actions.
- Clarified that outcomes should be presented after actions resolve, not before.
- Added player-facing steps for copying the GM packet into a new AI chat.

## v4.9 — Browser Stability / UI Fixes

- Fixed blank-browser-load issue from earlier HTML version.
- Adjusted GM Handoff panel layout.
- Removed irrelevant warning text from Review.
- Fixed Dossier spacing issues.
- Centered menu/panel placement.
- Removed Summary Mode from GM Handoff.
- Simplified canon download/open-link buttons.

## v4.x — Campaign Handoff and Tracker Foundations

- Added campaign archetype generation.
- Added campaign seed support.
- Added GM Handoff packet generation.
- Added early Progress Tracker import/export concepts.
- Added campaign-state display.
- Added NPC cast display.
- Added skill and gear usage descriptions.
- Added advancement and consequence systems.
- Added GM update JSON concept.

## v3.x — Campaign Setup and Presets

- Added random campaign setup.
- Added campaign navigation.
- Added campaign premise generation.
- Added gender, classes, and starting skills.
- Added Whore class support.
- Added preset main characters.
- Added preset loading workflow.
- Added Character Dossier preview concepts.
- Added class/stat/skill package handling.

## v2.x — Character Creation Foundations

- Built BG3-style character creation flow.
- Added lore validation concepts.
- Added uploaded-docs-only canon validator logic.
- Added race/type/class/background/origin/flaw/goal/secret/name structure.
- Added structured backstory and character dossier foundations.
- Added early Review step.
- Added basic visual layout for Creation Path.

## v1.x — Early Prototype

- Created first standalone HTML prototype for VEINFIRE RPG setup.
- Established the engine as a browser-based character/campaign setup tool.
- Began separating engine UI from live AI GM play.
- Established the idea that the AI chat session runs the live campaign after receiving a structured packet.
