# Machine Expansion Fixes

Unofficial corrective add-on for Machines & Robot Expansion Continued 3.2.3, upstream commit `e9d54b14a1f22730f17709efb23b37d83361c2a6`, targeting Stellaris 4.5.*. Load after MRE, before the balance and tradition mods. Neither authored gameplay package nor Gigastructures is required.

## Installation

Subscribe to [Machines & Robot Expansion Continued](https://steamcommunity.com/sharedfiles/filedetails/?id=3163759042), enable both mods in the same playset, and place Machine Expansion Fixes after the original. This package is an add-on, not a standalone replacement. Use one copy of the fixes package in a playset; do not also enable a locally patched full-source fork containing the same fixes.

The [public source fork](https://github.com/JustARegularAndTypicalPerson/stellaris-machine-robot-expansion) contains the corresponding full-source corrections and a copy of this add-on under `Fork/MachineExpansionFixes`. The release package contains fixes only. Auto-Machine Balance and Auto-Machine Traditions are separate projects and are not included.

Initial public version: **0.1.1**. The changes were reviewed against source; they have not been verified in a running game. A clean error log or compatibility with every other mod is not claimed. Save compatibility has not been established.

## Included fixes

- Clearing an insight blocker awards its missing core-insight situation progress.
- Completing a district calls the district insight event instead of the building insight event.
- Resolving the ruined World-Machine anomaly fires the existing discovery insight award.
- Core storage uses special maximum handling with a zero numeric base. The existing Origin modifier supplies the ten-core base once; existing storage modifiers contribute to the same cap used by production checks and cached values. Generic resource warehouses no longer create a separate core-storage maximum.

The first three corrections were extracted from the existing local MRE edits. New district storage, production economics, and fabricator limits belong to Auto-Machine Balance.

## Additional source-audit corrections

The [2026-10-23 audit](Audit20261023.md) records the fixes and remaining candidates in detail. Applied corrections cover shield upkeep constants, obsolete rare-tech weights, Bio-Mech growth arithmetic/display/eligibility, Encrypted Protocol recycling rewards, World-Machine district/army/planet counters, trait-filtered population helpers, a ringworld division-by-zero guard, repeated Auto-Factory research offers, and countdown completion. The dormant AI Splitting handler's ruler scope is corrected; its disabled feature hooks stay disabled.

The audit indexed 551 script files and 411 events, then traced candidates through callers and current vanilla sources. No game launch or automated tests were run; event-queue interruption cases remain separate investigation items.

## Maintenance and attribution

Same-path files replace MRE files once. The large event file includes unchanged upstream events surrounding a small award correction. Rebase these copies when updating MRE; do not put balance changes in them. `Sources.json` records source hashes and revision; `SourcePatch.diff` shows exact corrections.

Original mod code remains credited to XVCV, Openly Retro, Legit Rikk, and the other MRE contributors. The upstream repository and its existing notices remain the authority for inherited content. The independent fork does not grant a new license over inherited code or assets.

This add-on was prepared with AI assistance. It is independent of the upstream maintainers and is not an official upstream release. The local base checkout remains unchanged; the public fork applies the same corrections directly to its source.
