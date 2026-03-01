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
