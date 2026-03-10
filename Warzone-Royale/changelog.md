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
