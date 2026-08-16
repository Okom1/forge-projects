# Changelog

Threat Seekers changelog.

### 0.1.1

- Initial build
- Players are always invisible, and have unlimited Threat Seekers
- Players leave behind a trace when moving due to the Bomb they're holding that can't be dropped
- Players can damage other players by revealing them

### 0.2.0

- Made Bomb not drop on the ground when a player dies
- Added a custom cooldown to using the Threat Seeker, as players were able to use it too fast and keep enemies constantly revealed
- Enabled third person
- Enabled lifepools for teams; 4 respawns, after which players must be revived

### 0.3.0

- Adjusted custom equipment cooldown from 8 → 7 s
- Added danger nav markers to players who don't move enough for more than 4 seconds to prevent camping
- Changed mode variant to Arena:Elimination

### 0.4.0

- Changed equipment Threat Seeker → Threat Sensor cause it was too difficult to dodge Threat Seekers, and their effect lingered on for too long
- Changed starting weapon from Generic Bomb → Sandwich as the Threat Sensor has a glow on the ground already, so don't need the trail from the Bomb
- Adjusted nav marker join-in-progress assignment logic
- Increased damage from reveal per 0.10 seconds from 4 → 8
- Added a docked nav marker warning to players who are revealed by a Threat Sensor
- Reduced custom equipment cooldown from 7 → 5 s

### 0.4.1

- Brought back the Generic Bomb for the trail, as the light that the Threat Sensor emits on the ground was only very noticeable on a test platform, but not on other maps.
- Adjusted mode settings to return it back to a normal Slayer with respawns.
