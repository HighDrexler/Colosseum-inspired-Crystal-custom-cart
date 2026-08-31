# Colosseum Inspired Crystal Custom Cart

This repository hosts the latest Gen1Recomp custom-cart configuration for the **Colosseum Inspired Overhaul V2** Crystal setup.

## Important: what a `.g1rcart` can contain

Gen1Recomp custom carts are manifests, not mod archives. The cart format stores the base game, exact mod versions, load order, enabled state, and exported options, but it does **not** embed the mod code itself.

The closest supported equivalent to a prepackaged modded cartridge is therefore a cart whose mod entries point at exact published releases. Gen1Recomp's **Install Cart Mods** flow can download GitHub pins at the version named by the cart, verify their SHA-256 archive hash, and install them.

A mod recorded as `source = "local"` cannot be downloaded by the launcher because the cart only knows that the build existed on the machine that created the cart.

## Current download

The current release is **Colosseum Inspired Overhaul V2 cart 1.0.0**.

Canonical release asset:

`colosseum_inspired_overhaul_v2-1.0.0.g1rcart`

The same current configuration is also kept at repository root as:

- `colosseum_inspired_overhaul.g1rcart`
- `colosseum_inspired_overhaul_v2.g1rcart`

The previous V1 configuration is preserved separately as `colosseum_inspired_overhaul_legacy_1.0.1.g1rcart`.

## V2 stack

The sealed V2 cart preserves this exact load order and option state from the supplied package:

1. `BATTLE_ART_VOXEL_GEN2` `2.0.1`
2. `COLOSSEUM_BATTLE_ENVIRONMENTS` `1.6.1`
3. `colosseum_ui_overhaul` `2.2.1`
4. `exp_share` `0.1.7`

### Launcher-installable pins

These three mods are now pinned to exact public GitHub release archives and SHA-256 hashes:

- Colosseum Battle Environments `1.6.1` — `HighDrexler/Colosseum-Battle-Environments-1.0-BETA`
- Colosseum Inspired UI Overhaul `2.2.1` — `HighDrexler/Colosseum-Inspired-UI-Overhaul-V.1.0.0`
- Exp Share `0.1.7` — `ShaneMcGovernIE/exp_share`

When they are missing or the installed version is different, the cart's **Install Cart Mods** action can fetch the exact requested release and reject an archive whose SHA-256 does not match the cart.

### One remaining manual prerequisite

`BATTLE_ART_VOXEL_GEN2` `2.0.1` is preserved exactly as the supplied V2 cart requested, including its exported options, but that exact version currently has no public resolver-compatible GitHub release/tag that can be pinned without substituting a different build.

For a clean install, install/import the exact `BATTLE_ART_VOXEL_GEN2` `2.0.1` package first. Then import the V2 `.g1rcart` and use **Install Cart Mods** so Gen1Recomp downloads the other three pinned mods automatically.

If Battle Art is not installed first, the launcher can still install the three GitHub pins, but it will report Battle Art as unresolved because a `local` pin has no downloadable source.

## Recommended clean-install flow

1. Set up/import a compatible Pokémon Crystal ROM in Gen1Recomp.
2. Install `BATTLE_ART_VOXEL_GEN2` `2.0.1`.
3. Download and import `colosseum_inspired_overhaul_v2-1.0.0.g1rcart`.
4. Select the Colosseum Inspired Overhaul V2 cart on the Crystal launcher page.
5. Use **Install Cart Mods** to fetch/verify CBE `1.6.1`, Colosseum UI `2.2.1`, and Exp Share `0.1.7`.
6. Launch the cart. Colosseum Battle Environments may request the user's legally dumped Pokémon Colosseum ISO/CISO for its runtime-extracted assets.

## ROM assets

This repository and cart do not distribute copyrighted game ROMs. The user needs a legally dumped compatible Pokémon Crystal ROM, and Colosseum Battle Environments may require the user's legally dumped Pokémon Colosseum ISO/CISO.

## Remaining path to a fully remote four-mod cart

Once the exact `BATTLE_ART_VOXEL_GEN2` `2.0.1` package is published as a stable GitHub release (with a downloadable `.zip` asset), its cart entry can be changed from `local` to `github` with the repository and SHA-256. At that point **all four mods** can be installed from the cart through the launcher's Install Cart Mods flow, with no manual mod prerequisite.
