# Laser Sight Design Document

A Halo Infinite Slayer game mode where players just have to look at other players or objects to damage them over time. Players can't shoot, melee or throw grenades to ensure the objective stays clear. The Shroud Screen equipment can be used to temporarily disrupt line of sight.

Players are given a special weapon which has a unique reticle and no first person model to alleviate distractions as much as possible, and let players focus on just their aim. The weapon is Harbinger's custom weapon combined with a S7 Flexfire Sniper to produce the unique plus-shaped reticle.

Multiple raycasts are performed every tick for each player to accurately calculate where the player is aiming. A circular nav marker is constantly displayed at the collision point of the most relevant raycast. If the raycast lands on a valid target object, the target becomes locked for a short period unless the player finds another target before the period is over. This is a sort of aim magnetism that makes the gameplay less frustrating. When a target is locked, the nav marker changes to a red lock-on icon, and damage will start to be dealt to the target.

## Game Mode

- Slayer:Arena
  - Normal Slayer scoring and time rules
  - Not strictly for slayer, could be adapted to other modes
- Forge Mode; scripted logic
- 4–24 Players
- Single-round, but code support for multi-round

## Maps

- Any map intended for core multiplayer PvP
- Map must have working Nav Mesh and the first found respawn point must be on Nav Mesh data so the Harbinger AI can be spawned on it temporarily

## Audience

- Casual players
- Minigame enjoyers

## Gameplay loop

- Players spawn in and their weapons are replaced with the custom invisible weapon
- Players can't shoot, throw grenades, or melee
- Players must simply just aim at other players to begin dealing damage to them over time
- Players utilize movement tactics to try and disrupt the enemy's aim from their player model while keeping their own aim on the enemy in order to win fights
