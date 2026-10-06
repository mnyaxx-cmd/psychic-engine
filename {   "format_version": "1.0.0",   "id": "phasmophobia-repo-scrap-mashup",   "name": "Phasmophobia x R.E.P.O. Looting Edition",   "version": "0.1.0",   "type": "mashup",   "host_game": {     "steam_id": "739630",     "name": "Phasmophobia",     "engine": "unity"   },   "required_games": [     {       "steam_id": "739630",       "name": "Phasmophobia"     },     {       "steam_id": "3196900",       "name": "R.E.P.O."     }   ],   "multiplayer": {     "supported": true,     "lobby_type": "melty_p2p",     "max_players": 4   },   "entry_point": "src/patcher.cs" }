# Coding Agent Instructions: Phasmophobia x R.E.P.O. Mashup

You are a coding agent building a cooperative multiplayer game mashup inside Melty. 

## Target and Architecture
* **Host Engine:** Phasmophobia (Unity, 64-bit).
* **Modding Framework:** Use BepInEx or MelonLoader via C# hooks.
* **Secondary Game:** Extract inventory, asset values, and weight balance data from the user's R.E.P.O. installation folder.

## Core Mechanics to Implement

### 1. Scrap & Looting System (R.E.P.O. Logic)
* Scan the active Phasmophobia map scene for interactive furniture and prop objects.
* Assign a weight (kg) and currency value ($) to at least 20 types of house items (clocks, paintings, laptops, etc.).
* Inject a custom inventory system into the Phasmophobia player controller:
  * Maximum carrying capacity: 30 kg.
  * Apply a movement speed penalty linear to the weight carried.

### 2. Paranormal Synergy (Phasmophobia Logic)
* Hook into the Phasmophobia Sanity meter: walking while carrying loot drains player sanity 1.5x faster.
* Items with a high value ($150+) must trigger an EMF Level 2/3 reading when scanned with the EMF Reader.
* Picking up a "Cursed" variant of loot must instantly increase the ghost's aggression level and potentially trigger a hunt.

### 3. Multiplayer Synchronization
* Hook into Phasmophobia's network layer (Photon/Fusion).
* Synchronize the dynamic weight, taken/left status of loot items, and team total value across all 4 players in the lobby.

### 4. Win Condition (Evacuation)
* Modify the Phasmophobia van trigger: players can only leave if they have successfully locked in the ghost type AND secured at least $500 worth of loot in the van's cargo zone.
