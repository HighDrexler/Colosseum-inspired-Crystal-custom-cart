# Colosseum Inspired Crystal Custom Cart

This repository hosts the latest Gen1Recomp custom-cart configuration for the **Colosseum Inspired Overhaul V2** Crystal setup.

## Important: what a `.g1rcart` can contain

Gen1Recomp custom carts are manifests, not mod archives. The cart format stores the base game, exact mod versions, load order, enabled state, and exported options, but it does **not** embed the mod code itself.

That means the closest supported equivalent to a truly prepackaged modded cartridge is a cart whose mods are pinned to exact public releases. The launcher can then resolve/download those exact builds instead of relying on whatever versions the user already has installed.

## Latest V2 cart

Download either of these identical current packages and import it through Gen1Recomp's custom-cart importer:

- `colosseum_inspired_overhaul.g1rcart` — primary/current cart
- `colosseum_inspired_overhaul_v2.g1rcart` — explicitly named V2 copy

The previous fully remote V1 configuration is preserved as `colosseum_inspired_overhaul_legacy_1.0.1.g1rcart`.

## V2 stack

The sealed V2 cart preserves this exact load order and option state from the supplied package:

1. `BATTLE_ART_VOXEL_GEN2` `2.0.1`
2. `COLOSSEUM_BATTLE_ENVIRONMENTS` `1.6.1`
3. `colosseum_ui_overhaul` `2.2.1`
4. `exp_share` `0.1.7`

### Automatically resolvable pins

These three mods are pinned to exact public GitHub release archives and SHA-256 hashes:

- Colosseum Battle Environments `1.6.1` — `HighDrexler/Colosseum-Battle-Environments-1.0-BETA`
- Colosseum Inspired UI Overhaul `2.2.1` — `HighDrexler/Colosseum-Inspired-UI-Overhaul-V.1.0.0`
- Exp Share `0.1.7` — `ShaneMcGovernIE/exp_share`

### One remaining manual prerequisite

`BATTLE_ART_VOXEL_GEN2` `2.0.1` is preserved exactly as the supplied V2 cart requested, including its exported options, but that exact version currently has no public resolver-compatible release source that can be safely pinned without substituting a different build.

For a clean install, install/import the exact `BATTLE_ART_VOXEL_GEN2` `2.0.1` mod first, then import the V2 `.g1rcart`. Once that build is published at a stable GitHub or GameBanana release URL, this cart can be converted to a fully remote four-mod configuration with no manual mod prerequisite.

## Crystal / ROM assets

The cart targets Pokémon Crystal and does not distribute copyrighted ROM data. The user still needs a legally dumped compatible Pokémon Crystal ROM for Gen1Recomp. Colosseum Battle Environments may also request the user's legally dumped Pokémon Colosseum ISO/CISO for the assets it extracts at runtime.

## Why the launcher may say mods are not included

That message is expected for the cart format itself: `.g1rcart` files do not physically carry mod folders or archives. What matters is whether each manifest entry has a resolvable published source. The V2 cart now has remote sources for every mod that can currently be resolved without changing the supplied build, leaving only Battle Art `2.0.1` as a manual prerequisite.
