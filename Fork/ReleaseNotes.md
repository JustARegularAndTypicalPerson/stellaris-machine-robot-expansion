# Machine Expansion Fixes 0.1.1

Initial public release of the unofficial fixes add-on for Machines & Robot Expansion Continued 3.2.3 and Stellaris 4.5.*.

## Installation

1. Install [Machines & Robot Expansion Continued](https://steamcommunity.com/sharedfiles/filedetails/?id=3163759042).
2. Extract the release archive. Put `MachineExpansionFixes/` and `MachineExpansionFixes.mod` inside `Documents/Paradox Interactive/Stellaris/mod/`.
3. Enable the original mod and Machine Expansion Fixes in one launcher playset, with the fixes after the original.

The archive is an add-on, not a replacement for the full original. Do not also enable the full-source fork containing the same corrections. Steam subscribers can use the Workshop package instead of this manual archive.

## Changes

- Restored three World-Machine insight award paths and corrected Auto-Core storage accounting.
- Updated shield upkeep constants and obsolete rare-tech weight references.
- Corrected Bio-Mech multiplier arithmetic, stale growth displays, and duplicated event conditions.
- Corrected Encrypted Protocol recycling rewards.
- Corrected World-Machine district/army/planet counts and trait-filtered population helpers.
- Guarded ringworld resizing against zero eligible segments.
- Prevented repeated completed Auto-Factory research offers and premature fractional countdown completion.
- Corrected the dormant AI Splitting ruler scope without enabling its disabled hooks.

The package contains 15 source-file replacements. `SourcePatch.diff`, `Sources.json`, and `Audit20261023.md` provide the exact changes, source hashes, and detailed evidence. Formatting was refined to match the surrounding upstream scripts without adding gameplay changes.

## Validation and scope

Source-reviewed; no automated tests or game session were run for this release. In-game behavior and save compatibility remain unverified. The audit lists unresolved event-queue and interruption cases.

Auto-Machine Balance and Auto-Machine Traditions remain separate and unpublished. No balance redesign is included.

This is an independent AI-assisted patch. Inherited code remains credited to the original MRE contributors, and no new license is granted over their work.
