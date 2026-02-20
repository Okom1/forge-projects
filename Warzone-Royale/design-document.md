# Warzone Royale Design Document

Warzone Royale is a battle royale mode where players fight in teams to scavenge loot and aim to be the last squad standing.

Players start with no weapons, and need to find their loadout from loot boxes scattered around the map. Loot boces also contain "Armor" in the form of Custom Equipment, which can be stacked and activated to give the player a higher temporary damage resistance, until depleted.

After finding weapons, players can ugrade their equipped weapon using a radial menu with points also gathered from loot boxes, or enemy eliminations. Points can also be spent on Ability Boosts, which enhance specific abilities of the player such as upgraded sprinting, or faster reload speed.

When players die, they can be revived or will automatically respawn after an increasing respawn time as long as one of their teammates are still alive. Eventually, a zone will start shrinking to a random location on the map to force the remaining players into engagements that will determine who is the last team standing, and wins the game.

## Game Mode

- Minigame or Elimination
  - Must support revive orbs
  - Must support teams
- Forge Mode; scripted logic
- 4–24 Players
  - Players can split into how many teams they want
- Single-round, but code support for multi-round
- Last team with players alive wins
- No time limit

## Maps

- Should work on any map with respawn points
  - On-level weapons, equipment and grenades need to be deleted via scripting, while still allowing custom items to be spawned, so can't use mode setting to turn them off.

## Audience

- Everyone, but inclined for players who enjoy Battle Royale modes

## Gameplay loop

### Pre-game

- Players set up in teams in the pre-game lobby
- Teams can be of any size and distribution

### Spawning 

- Players spawn on the map evenly distributed on the available spawn points near their teammates
  - Players start with fists and 3 armor applied
- Players can respawn as long as one of their teammates is still alive
  - Players respawn near their teammates with just a Mk50 Sidekick and 3 armor applied
- Default respawn time of 10 s
  - Every teammate death increases the respawn time of all teammates by 1 s
  - Every kill on enemies decreases the respawn time of all teammates by 1 s
- If all members of a team are dead simoultaneously, the team is eliminated

### Armor

- Armor is a damage resistance trait that depletes when you are damaged
- Players start with 3 armor
- Armor pickups can be found in loot boxes in the form of custom equipment
- Armor is displayed to the player via a docked nav marker offset to the left of the screen; still always visible on the UI, even when at 0 armor
  - Amount of armor is communicated via a progress bar around the nav marker as well as the message "Armor: x"
- Armor is displayed to other players via the VIP and Overshield VFX around the player model
  - VIP (blue ring) = 1–3 armor
  - Overshield = 4–5 armor
- Armor can be applied by activating the custom equipment
  - Up to 10 custom equipment can be held at a time
  - The maximum amount of armor is 5
  - Trying to activate more than 5 armor will not apply the armor, and will not consume the custom equipment

### Looting items

- Players start with just fists and have to scavenge weapons from loot boxes around the map
- Loot boxes are placed near spawn points and the original locations of weapon pads, grenade dispensers and equipment spawners
- Going near a loot box automatically opens the loot box and spawns two weapons, a grenade, one or more armor pickups and grants points based on the rarity of the box
  - One of the weapons is always a lower-tier loadout weapon intended for ammo refills, and the other is a main weapon
  - Multiple tiers of loot box rarities with low-tier ones being more common than high-tier ones. The closer you get to the center of the map, the higher tier boxes there are. Some high-tier boxes will also be scattered with the low-tier ones.
- An event plays 1-2 times per match somewhere on the map that spawns the highest-tier loot which is not obtainable from anywhere else.
  - Weapons like Snipers, Turrets, Ravagers, Carbines, and Hydras

### Points

- Points are used as currency to purchase upgrades to your loadout and passive abilities
- Points are gathered by finding them in loot boxes, by killing players, or by engaging in events that happen on the map
  - Points from kills are granted to all teammates
  - Completing events grants a large amount of points to the completing team
- Points can be used to purchase upgrades in a radial menu

### Radial menu

- A radial menu can be opened at any time by pressing the Custom Input (default: 1 or Dpad Right)
- The radial menu contains menus for Ability Boosts, Weapon Upgrade, (undecided), and Spawning
- Ability Boosts act as passive upgrades to certain abilities like increased movement speed, or reload speed
  - Cost is relatively low
- Weapon Upgrades allow the player to upgrade their equipped weapon to a higher tier variant
  - Cost is proportional to how good the higher tier variant is

### Spectating

- If all players from a team die, they will be eliminated, after which they will turn into spectators
- Spectators have their respawns disabled, and can spectate third-person gameplay of alive players on the same team as them
- In order to spectate players from other teams, a separate radial menu will be available for spectators which allows changing their team to one of the remaining teams
  - Eliminated teams will be unselectable
