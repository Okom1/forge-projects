# Ranked Evo Design Document

A variant of Halo Infinite's competitive modes with experimental settings led by the Halo pro Luciid TW.

Ranked Evo aims to refresh the competitive Halo Infinite settings by listening to feedback from the community about what changes could be done to the existing ranked modes and maps to make them better.

Some experimentation is warranted to test the limits of what can work. Potential changes include BR75 starts, a loadout weapon selector, and slightly modified weapons via scripting.

## Game Mode

- Ranked settings
- Ranked base modes with Forge scripting on top
  - 3-Flag CTF
  - 5-Flag CTF
  - King of The Hill
  - Oddball
  - Slayer
  - Strongholds

## Maps

- Custom variants of Ranked maps with additional skill jumps and adjusted sandbox items
  - Maps: https://www.unggoy.xyz/browse?gamertag=Luciid%20TW&searchTerm=Evo&assetKind=Map

## Audience

- Competitive players who are up to try out new settings

## Gameplay loop

### Starting weapons menu

- A radial menu shows up for all players during the intro cameras that allows players to choose their starting weapon for the rest of the match
  - Options for Bandit Evo and BR75
  - Only two of each starting weapon are available. If players pick two BR75s, the remaining two players can only pick Bandit Evos
- Radial menu forcefully closes on Gameplay Start
- If players didn't pick a starting weapon, they will be assigned a weapon by random from the available remaining options

### Standard ranked gameplay

- The gameplay is standard ranked gameplay with no adjustments
