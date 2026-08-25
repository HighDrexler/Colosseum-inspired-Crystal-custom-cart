# Colosseum-inspired Crystal custom cart

This repository hosts the Gen1Recomp custom-cart configuration for the Colosseum-inspired Crystal setup.

## Download

Download `colosseum_inspired_overhaul.g1rcart` from this repository and import it through Gen1Recomp's custom-cart importer.

## Current portability status

The configuration file is uploaded exactly as exported, including its complete load order, enabled/disabled state, and mod options.

At the moment, however, the cart is **not yet portable to a clean Gen1Recomp install** because every mod entry is still pinned as `source = "local"`. In Gen1Recomp, local pins refer to mods already installed on the machine that created the cart; they do not download missing mods for another user.

For a true one-click import, each mod must be converted to a published `github` or `gamebanana` pin with the exact public version and archive hash expected by Gen1Recomp.

Two exact builds referenced by this cart are not currently available as matching public releases:

- `STADIUM2_OVERWORLD_MODELS` is pinned to `0.2.88`; the public `randyadr/Gen2-3D-Sprites` releases currently expose `0.2.81` as the newest matching release found during setup.
- `colosseum_ui_overhaul` is pinned to `2.0.2`; the public `HighDrexler/Colosseum-Inspired-UI-Overhaul-V.1.0.0` releases currently expose `2.0.0` as the newest matching release found during setup.

The Colosseum Battle Environments cart entry also needs to be normalized from `1.2` to semantic version `1.2.0` when it is converted to a GitHub pin; the public release is tagged `1.2.0`.

Do not advertise this cart as a clean-install/full-package import until all local pins have been replaced by fetchable published pins. Downgrading the cart to older public builds would change the intended configuration and is intentionally not being done here.
