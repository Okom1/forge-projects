# Rocket Jumpers Design Document

Rocket Jumpers is a Halo Infinite Slayer game mode where players are equipped with a custom rocket launcher and a sniper. The rocket is mainly used as a means to propel yourself or enemies in the air via a "rocket jump" by shooting under their feet. The secondary weapon is used for kills.

The rocket launcher is the ["A Go At" Fuel Rod SPNKr from TSG Warzone](https://github.com/The-Scripters-Guild/Warzone/blob/main/docs/items/weapon-configs.md#41-a-go-at) which shoots a Rockethog rocket projectile in addition to applying a custom velocity to any players close to the rocket explosion to create a large knockback effect which allows the rocket jump.

The mode follows normal Slayer rules. The secondary weapon can be changed, but it defaults to the S7 Sniper. The melee damage is increased to allow for one-hit melee kills which rewards players who get close to enemies via rocket jump movement. Explosion resistance is increased so players don't die to the rocket jumps as quickly as normally.

## Game Mode

- Slayer:Arena
  - Normal Slayer scoring and time rules
  - Not strictly for slayer, could be adapted to other modes
- Forge Mode; scripted logic
- 4–24 Players
- Single-round, but code support for multi-round

## Maps

- Any Forge canvas-based map intended for core multiplayer PvP. Dev maps unsupported due to custom object placement loaded from the mode that utilize the 0,0,-8500 coordinate, which behaves differently on dev-made maps compared to Forge canvas maps.

## Audience

- Casual players
- Minigame enjoyers

## Gameplay loop

- Players spawn in and are given the rocket launcher and a sniper
- Players aim to kill the enemy team and reach the score limit before the enemy team
- Players are encouraged to use the rocket launcher to perform rocket jumps which give the players a positional advantage
- Players can have fun with the rocket jumps and also attempt to hit cool sniper shots while in the air
