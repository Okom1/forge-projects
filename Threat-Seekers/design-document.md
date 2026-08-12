# Threat Seekers Design Document

A Halo Infinite Slayer game mode where being revealed by a Threat Seeker equipment damages you.

## Game Mode

- Slayer:Arena
  - Normal Slayer scoring and time rules
  - Not strictly for slayer, could be adapted to other modes
- Forge Mode; scripted logic
- 4–24 Players
- Single-round, but code support for multi-round

## Maps

- Any map intended for core multiplayer PvP
- Preferrably maps with high verticality

## Audience

- Casual players
- Minigame enjoyers

## Gameplay loop

- Players spawn in completely invisible while holding a Bomb that leaves behind a blue trace when moving.
- Players are equipped with an unlimited-charge Threat Seeker equipment that they must use to seek out the enemy players by revealing them in the equipment's radius.
- If an enemy is revealed, they begin taking damage, but not enough to kill them from just one reveal. Players must take damage from two subsequent reveals in order to die.
- The goal is to not get revealed by the enemies while revealing them in order to kill them and win the game.