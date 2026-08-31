# Colosseum Inspired Crystal Custom Cart

This repository hosts the latest Gen1Recomp custom-cart configuration for the **Colosseum Inspired Overhaul V2** Crystal setup.

## Current download

The current release is **Colosseum Inspired Overhaul V2 cart 1.0.0**.

Canonical release asset:

`colosseum_inspired_overhaul_v2-1.0.0.g1rcart`

The same current configuration is also kept at repository root as:

- `colosseum_inspired_overhaul.g1rcart`
- `colosseum_inspired_overhaul_v2.g1rcart`

The previous V1 configuration is preserved separately as `colosseum_inspired_overhaul_legacy_1.0.1.g1rcart`.

## Fully launcher-installable V2 stack

The sealed V2 cart preserves the supplied load order and option state while pinning all four mods to exact public GitHub release archives:

1. `BATTLE_ART_VOXEL_GEN2` `2.0.1` — `absol89/Gen2Recomped-DramaticShapes`
2. `COLOSSEUM_BATTLE_ENVIRONMENTS` `1.6.1` — `HighDrexler/Colosseum-Battle-Environments-1.0-BETA`
3. `colosseum_ui_overhaul` `2.2.1` — `HighDrexler/Colosseum-Inspired-UI-Overhaul-V.1.0.0`
4. `exp_share` `0.1.7` — `ShaneMcGovernIE/exp_share`

Each pin records its repository, exact version, and SHA-256. Gen1Recomp's **Install Cart Mods** flow can therefore fetch the exact requested release for every mod and reject an archive whose SHA-256 does not match the cart.

Battle Art `2.0.1` is pinned to `BATTLE_ART_VOXEL_GEN2-2.0.1.zip` with SHA-256:

`fe3292fb4f8f29e105f397e353d3c32611c23af2123a4146632c524ea9fdc0d8`

There is no longer a manual Battle Art prerequisite in V2.

## Recommended clean-install flow

1. Set up/import a compatible Pokémon Crystal ROM in Gen1Recomp.
2. Download and import `colosseum_inspired_overhaul_v2-1.0.0.g1rcart`.
3. Select the Colosseum Inspired Overhaul V2 cart on the Crystal launcher page.
4. Use **Install Cart Mods**. Gen1Recomp should fetch and verify Battle Art `2.0.1`, CBE `1.6.1`, Colosseum UI `2.2.1`, and Exp Share `0.1.7`.
5. Launch the cart. Colosseum Battle Environments may request the user's legally dumped Pokémon Colosseum ISO/CISO for its runtime-extracted assets.

## What a `.g1rcart` contains

A Gen1Recomp custom cart is a manifest rather than a container for mod code. It stores the base game, exact mod versions, load order, option state, source repositories, and hashes. The launcher then downloads the pinned release archives through **Install Cart Mods**.

This V2 cart is therefore now the supported equivalent of a prepackaged four-mod configuration: the user imports one `.g1rcart`, installs its pinned mods through the launcher, and launches the configured Crystal setup.

## ROM assets

This repository and cart do not distribute copyrighted game ROMs. The user needs a legally dumped compatible Pokémon Crystal ROM, and Colosseum Battle Environments may require the user's legally dumped Pokémon Colosseum ISO/CISO.
