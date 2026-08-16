# Changelog

Translocators changelog.

### 0.1.1

- Initial build
- Players have an unlimited use of the Quantum Translocator equipment
- Players can destroy enemy teleporter objects with a Gravity Hammer swing
- Players can destroy their own teleporter with the custom input
- Nav markers are attached to all teleporters that display the owner and how long the teleporter is still alive

### 0.2.0

- Added an alert nav marker for when an enemy is on your translocator
- Added a separate nav marker for friendly translocators
- Adjusted nav marker assignment logic per player index to not account for new join-in-progress players as a debug measure for nav marker issues
- Changed the way the translocator teleport is destroed from it being deleted to damaging by 10,000 health, so the destruction causes a native animation instead of just disappearing
- Adjusted sound of manually destroying your own translocator via custom input
