# Changelog

Warzone Royale changelog.

### 0.1.1

- Initial build
- Loot crate distribution script
- Every Tick player respawn unblocking
- 0.1.0 is a profane term in Halo Infinite

### 0.1.2

- Adjusted box placement filter to catch some more equipment dispensers
- Implemented cut-down version of sandbox-warzone
- Implemented weapon spawning at position via M247 HMG Turret on-level spawned from the mode
- Adjusted preliminary mode settings

### 0.1.4

- Fixed issues with weapon spawning at position
- Implemented personalized player weapon skin retaining for base weapons
- 0.1.3 is a profane term in Halo Infinite

### 0.2.0

- Added random distribution of four tiers of loot boxes
  - Tier 1: 40%
  - Tier 2: 30%
  - Tier 3: 20%
  - Tier 1: 10%
- Added loot box proximity detection and loot box opening from proximity

### 0.3.0

- Implemented Custom Equipment A spawn at position

### 0.4.0

- Fixed issues with revive orbs and equipment creation due to player death
- Implemented fists weapon for all players on spawn

### 0.4.1

- Added tier-based FX and audio for looting boxes
- Excluded spawn points from filteredObjects deletion

### 0.4.2

- Fixed issues with weaponSpawners getting destroyed or deleted and thus not spawning weapons

### 0.5.0

- Build with weapon spawning debugs off

### 0.6.0

- Fixed issue where objects originating at 0,0,- would fall on the weapon spawner turrets at 0,0,-9460 after around 7 seconds from Gameplay Start and destroy them, causing not being able to spawn weapons via them (LMAO)
- Changed the base mode to Arena:Slayer so spawn volumes with the "Minigame Include" label that block spawns from any other teams than Eagle or Cobra would get ignored
  - Also fixes the concern for excluding the Assault and Headhunter objects which also use the "Minigame Include" label

### 0.6.1

- Added vehile removal every second

### 0.7.0

- Added loot box drops based on tier of box

### 0.8.0

- Added extra armor feature

### 0.8.1

- Fixed issue with Custom Equipment A staying in the starting player's inventory at Gameplay Start

### 0.8.2

- Added points display per player and did initial loot box points grant balancing

### 0.8.3

- Code cleanup
- Fixed equipment despawn loop being 1 second

### 0.8.4

- Implemented Custom Equipment gathering without the need for player death—requires some equipment placement on the level to work
- Fixed weapon despawn time from loot box dropped weapons not being 20 s for base weapons (cloned weapons)

### 0.9.0

- Changed loot boxes to be interactable power sockets
- Adjuster loot pool to only have base and legendary weapons so players don't get confused by the weapon icon of the Warzone sandbox weapons

### 0.10.0

- Changed base mode to Firefight:Custom due to a better UI and no excess misleading UI communication

### 0.10.1

- Adjusted vehicle deletion script to only fire once On Gameplay Start instead of every second since the Firefight:Custom mode automatically stops vehicle spawner respawns
- Fixed armor not resetting to 0 on death which caused an invulnerability issue

### 0.11.0

- Implemented initial radial menu with options to purchase Ability Boosts, Weapon upgrades and Equipment
- Made kills give points to all team members
- Added a temporary static respawn time of 8 s
- Adjusted point grant amounts from loot boxes

### 0.11.1

- Forced rotation of loot boxes to be 0,45,(variable) so they always face up
- Removed Pursuit Hydra from Tier 3 loot box cause it can be upgraded to a tier 7+ variant
- Removed weapon variants with custom projectiles from weapon upgrade options that would require on-level objects to function
- Fixed temporary respawn time only affecting the first life
- Fixed issues with fists weapon replacement when spawning with a weapon from the death screen

### 0.12.0

- Made loot boxes open via player proximity

### 0.12.1

- Made Ability Boosts reduce player points upon purchase
- Made players initially spawn next to the first player on their team
- Fixed weapon grants past value 84 being offset by +1 in Forge due to fists weapon type being empty
- [11] Armor cost: 2 → 3

### 0.12.2

- Implemented better system to remove vehicles every second, including mounted turrets
- Changed base mode to Arena:Slayer

### 0.12.3

- Changed vehicle deletion from every second to every 0.10 seconds

### 0.13.0

- Changed Custom Equipment A gathering to be dropped from an Eagle team bot who dies at the start of each round

### 0.14.0

- Added buddy spawning functionality

### 0.14.1

- Added team spectating radial and functionality

### 0.15.0

- Added equipment dropping functionality
- Made your previously held equipment automatically drop when buying a new equipment
- Made all spawn points on level be Neutral team and Spawn Order 0
- Added deletion of loose weapons during box distribution
- Added more danger factors to overcome for buddy spawning to work: Proximity to enemies who have line of sight, and buddy firing their weapon
- Fixed issues spawning at 0,0,0 at the start of the match and dying immediately
- Improved spawn queue so it retries to spawn you if the first spawn attempt didn't work. This can happen if more than one player is trying to spawn on a buddy at the same time
- Added creation of new Spawn Order 0, Neutral team spawn points at the locations of every existing spawn point to ensure players on all teams can spawn on the map; some creators may have assigned some spawns to specific teams

### 0.15.1

- Added game ending logic and communication when only one team remaining
- Improved communication and radial displays when your team gets eliminated

### 0.15.2

- Added gathering of the most evenly spaced spawn points which are used to teleport players at those positions at the start of the match. The amount of positions is determined by the amount of teams present 3 seconds into the round

### 0.15.3

- Added a bot pickup ambition on nearby weapons spawned from loot boxes so bots would pick up weapons more
- Made picking up Fusion Coils while holding only Fists not remove the Fists

### 0.15.4

- Adjusted bot weapon pickup ambition radius from 30 to 50
- Updated modules to Sandbox 1.10.0 and Radial 1.6.0
- Fixed issue with dummy bots not spawning in at the beginning of the game, leading to dummy equipment and armor equipment not being gathered
- Made players unharmable before gameplay begins to prevent them from dying from level-based causes like auto turrets during the intro sequence 

### 0.16.0

- Added varying respawn time per team that increases by one second if a teammate dies and decreases by one second if an enemy is killed. Minimum respawn time is always 5 seconds.

### 0.16.1

- Added Power Seed distribution in the box distribution logic that act as the main way of gathering points. Picking up a Power Seed grants points to the player.
- Made players lose half of their points upon death, and drop said points as Power Seeds on their death location
- Added ability to bypass Buddy Spawn danger checks by healing the player with a Repair Field
- Modified player LoS danger detection logic to also trigger for players who are detected by a Threat Sensor or Threat Seeker
- Modified player LoS danger detection logic to cut if the player is inside a Shroud Screen
- Adjusted equipment pickup prevention time after dropping equipment from 0.50 → 1.00 as the dropped equipment was being picked up too easily
- Added periodic loot drops that last for 60 seconds. The loot drops drop the highest tier items
