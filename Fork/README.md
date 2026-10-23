# Independent fixes distribution

This directory contains the separately installable Machine Expansion Fixes add-on and its release documentation. The repository's root `common/` and `events/` files already contain the same fixes directly.

- Add-on users load `MachineExpansionFixes/` after the original Machines & Robot Expansion Continued 3.2.3.
- Full-source fork users enable their checkout directly and do not also enable this add-on.
- `MachineExpansionFixes/SourcePatch.diff` is the cumulative patch against upstream commit `e9d54b14a1f22730f17709efb23b37d83361c2a6`.
- `MachineExpansionFixes/Sources.json` records upstream and patched file hashes.
- `ReleaseNotes.md` records installation and validation limits.

The authored balance redesign and tradition add-on are separate projects and are not included in this release. Original MRE credits and notices remain in effect for inherited work. The independent corrections were prepared with AI assistance.
