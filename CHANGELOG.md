# Changelog

## v6.1 — Safety, Relationship Cleanup & Model Persistence

- Added explicit preset trope mapping for all preset characters.
- Simplified preset dropdown labeling so it no longer relies on personal-name regex guessing.
- Fixed Torun Red-Horn displaying his personal name instead of `Field Medic` in the preset dropdown.
- Removed fragile Watcher/Bell regex classification from preset trope labeling.
- Cleaned preset trope labeling so dropdown names no longer depend on removed `label` fields.
- Cleaned duplicated selected-model assignment in `load()`.
- `createCharacter()` now returns success/failure and supports silent success mode.
- Preset proceed flow now stops if character validation fails.
- Restored missing preset guards for edit/proceed flows.
- Removed old orphaned relationship helper functions from the previous `-3/+3` scale.
- Removed advisory `label` field from `npcRelationship` GM packet examples because labels are derived from relationship value.
- Replaced unused clear-state helper with shared reset helper used by create-own and preset flows.
- Added confirmation guard before actions that discard unfinished character creation work.
- `Create My Own` now asks before wiping an unfinished character.
- Preset edit/proceed actions now also ask before replacing unfinished character work.
- Relationship examples now match the `-10` to `+10` scale.
- Importer no longer lets an explicit stale relationship label override the derived label.
- Removed old `-3/+3` relationship helper code that could become a future trap.
- Persisted selected AI model in save state.
- Restored selected AI model button highlight after reload/render.
- Removed dead `beginWelcome()` code.

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
- Added response pacing rules.
- Added Player Input Authority Rule.
- Added Intent → Method → Resistance → Outcome action resolution.
- Added Yes/And, Yes/But, No/But, No/And outcome framing.
- Added NPC resistance rules so NPCs do not instantly comply.
- Expanded NPC relationship scale from `-3/+3` to `-10/+10`.
- Added relationship labels from Nemesis to Life-Bound.
- Added relationship clamping and relationship bar UI support.
- Added gradual relationship-shift rules to the GM packet.
- Strengthened NPC agency rules.
- Clearly separated relationship from resistance.
- Added social conflict rules.
- Added combat behavior rules.
- Added injury tracking support.
- Updated GM_UPDATE_JSON to schemaVersion `veinfire-progress-v4`.
- Progress save export uses `veinfire-progress-save-v4`.

## v5.8 — Welcome Flow, Creation Polish & Tracker Foundation

- Added Welcome page as the first player-facing screen.
- Added “How do you want to begin?” setup choice flow.
- Moved preset selection out of the Creation Path.
- Added preset preview with character dossier.
- Added options to proceed directly from preset or edit preset details first.
- Improved Character Creation navigation.
- Removed per-section Validate buttons.
- Added guided Appearance section with multiple boxes.
- Added dice randomizers and expanded randomization datasets.
- Improved Campaign Generator readability.
- Improved Campaign Tracker standalone behavior.

## v5.7 — Guided Navigation

- Reworked top navigation into the main flow.
- Moved Campaign Tracker under Tools.
- Clarified tracker as standalone tool.
- Improved alert color handling.

## v5.6 — Forced GitHub Canon

- Removed visible Canon Source Setup from GM Handoff.
- Updated GM packet to assume GitHub canon access by default.
- Added manual fallback if AI cannot access links.

## v5.5 and earlier

- Updated canon links to GitHub-hosted Markdown files.
- Added public repo/hosting materials.
- Added GM Handoff improvements.
- Added progress tracker foundations.
- Added campaign setup, presets, and character creation foundations.
