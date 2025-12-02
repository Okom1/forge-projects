# Spyfall Design Document

Spyfall is a social deduction game where the "Agents" know the end "Location", except the "Spy". The Spy has to figure out the location before the others figure out who the Spy is by asking probing questions from the others. The Agents also have to ask questions about the location even though they know it in order to try and figure out who doesn't know enough relevant information about the location, thus being the Spy.

## Game Mode

- FFA Slayer
  - All players on same FFA Affiliation Team so they don't feel inclined to try and kill each other
  - Must be FFA so specific players can win instead of a team of players
- Forge Mode; scripted logic
- 4–24 Players
- Multi-Round
  - Short rounds so different people can be the Spy and the gameplay stays interesting
- Player with the most points at the end of 5 rounds wins
  - Points awarded and deducted based on positive or negative decisions towards the goal
- If time runs out, the Agents win that round and are awarded points. Spy doesn't lose any points

## Maps

- Custom-built to suit the mode
- [ONI](https://duckduckgo.com/?q=halo%20oni%20building&iar=images&t=h_) theme
- Mostly rooms to walk around in with no gameplay intent
- Emphasis on being able to bump into players to ask questions
- Include a meeting room that can either be closed off via scripting, or is a separate room altogether
- Include an elimination room where players can see others get eliminated

## Audience

- Halo Machinima creators
- Friend groups with comms

## Gameplay loop

### Players spawn in a single room and are assigned roles by random
- Agents are revealed the current round's location with UI messaging
- The Spy is not shown the location; they are instead let know that they are the Spy
### Players begin asking questions
- Done via 3rd party voice chat, as FFA mode can't have in-game voice chat
- Everyone asks questions about the location
- Agents try to probe specific details about the location to figure out who doesn't know it, and who may be lying
- Spy tries to figure out the location by fishing information from others while not revealing that they don't know the location by answering with confidence
- Example questions:
  - "What kind of shoes would you wear here?"
  - "What time of day is busiest at this place?"
  - "What's the worst thing that could happen here?"
### (optional) Agents call a collective emergency meeting
- Initiated by activating a switch in the meeting room
  - Opens a radial menu with one of the options being to call a meeting. That same option turns to a button to agree to the meeting if a meeting request is ongoing.
  - Majority vote: requires 3/4 of all players to press the switch for the meeting to begin. Nav marker attached to the switch communicates how many Agents agree.
  - The Spy is also one of the people who needs to agree, as otherwise you could tell who the Spy is if they can't contribute to the agree count
    - If enough agree, all players are teleported to a central, closed meeting room
    - If not enough agree, game continues as normal
- Objective for the Agents is to vote for the player who they think is the Spy
  - Mark a player to cast a vote; nav marker appears above said player with a counter on how many players voted for them
- 120 seconds time to cast a vote; round timer changes to reflect the time remaining
  - If time runs out, the player with the most votes on them gets eliminated. If more than one player has the same amount of votes, choice will be random.
  - If all votes are cast, a short pause happens where nobody can change their votes anymore and the player with the most votes on them gets eliminated
    - If the Spy, Agents win the round and gain points; Spy loses no points
    - If an Agent, Spy wins the round and gains points; Agents who voted for the wrong Spy lose points
### (optional) Spy guesses the location
- Initiated by Spy activating a switch in the meeting room (same switch as the meeting switch)
  - Opens a radial menu with one of the options being to guess the location (only available for the Spy)
    - Opens a radial menu with 8 location options
    - If correct location chosen, Spy wins the round and gains points; all Agents are eliminated
    - If incorrect location, Spy loses the round and loses points; Spy is eliminated