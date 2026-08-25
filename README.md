# Colosseum-inspired Crystal custom cart

This repository hosts the Gen1Recomp custom-cart configuration for the Colosseum-inspired Crystal setup.

## Download

Download `colosseum_inspired_overhaul.g1rcart` and import it through Gen1Recomp's custom-cart importer.

The cart is fully remotely pinned. On a clean compatible Gen1Recomp install, the launcher can fetch the exact mod archives used by the cart instead of requiring those mods to already exist locally.

Current cart configuration: `1.0.1`.

## Pinned stack

The sealed cart installs and locks the following builds in this load order:

1. Colosseum Battle Environments `1.2.0`
2. Stadium 2 Overworld Models custom fork `0.2.88`
3. Colosseum Inspired UI Overhaul `2.0.3`
4. Exp Share `0.1.7`
5. Wilds of Kanto `2.1.8` — installed/configured but starts OFF
6. PotatoVoxel `1.9.1`

Every GitHub pin includes the exact release version and SHA-256 archive digest expected by Gen1Recomp. The Stadium2 pin uses `HighDrexler/Gen2-3D-Sprites` release `0.2.88`, which is byte-for-byte identical to the custom Stadium build used when this cart was captured.

The exported mod options, enabled/disabled state, and load order are preserved by the cart rather than relying on the user's existing mod configuration. Cart `1.0.1` also preserves the current PotatoVoxel `curve = 2` setting from the latest exported setup.

## ROM assets

The cart does not distribute copyrighted game ROMs. The user still needs a legally dumped compatible Pokémon Crystal base ROM for Gen1Recomp, and Colosseum Battle Environments may request the user's legally dumped Pokémon Colosseum ISO/CISO for its extracted assets.
