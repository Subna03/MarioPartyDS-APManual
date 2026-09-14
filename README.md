# MarioPartyDS-APManual
Manual implementation for Mario Party DS, for Archipelago Randomizer. Two goals to choose from: beat Bowser in Story Mode, or sweep all 5 boards in Party Mode.
---------------------------------------------------------------------------------------------------------
Mario Party DS is an acclaimed 2007 party game for the Nintendo DS that follows Mario and his friends after Bowser shrinks them down to toy size. Up to four players compete on five themed boards to collect coins and stars, playing through over 70 minigames that utilize the console's touchscreen and microphone. It stands out for its single-player story mode and a local multiplayer option that lets four people play together using just a single game cartridge via Download Play.

# How to play
(Of course you need Manual from Archipelago, and a copy of Mario Party DS.)
Pick a **Goal** in your YAML before generating:
**Story Mode** progress through the 5 boards in a fixed order, defeat the bosses along the way, and beat Bowser at the end
**Party Mode** (unlock and win all 5 boards in any order, no bosses required.

At the start of the game, depending on your options, you'll have restrictions:
- **You won't have any board unlocked** unless you set a starting board in Party Mode. Boards unlock via items from the multiworld.
- **You won't be able to fight any boss minigame** until you receive its unlock item (if Boss Minigame Lock is on).
- **You won't have access to the Minigame Mode sub-modes** (Step It Up, Battle Cup, Score Scuffle, Rocket Rascals, Boss Bash) until you receive their items (if enabled).
- **You won't have access to the Puzzle Mode sub-modes** until you receive their items (if enabled).
- **You'll only have one character unlocked** the rest come in through the multiworld.
- **You won't be able to use board items/hexes** (Dice Blocks, Hexes, etc.) until you receive their unlock item back (if enabled).
- **The CPU will start on Easy** and ramp up in difficulty as you receive CPU Level Up traps (if enabled).

Free Play minigames (~74 of them) are **always available from the very start**, regardless of goal or options — these are your bread and butter for early checks.

# Checks
- **Board Wins**: winning 1st place on each of the 5 boards.
- **Boss Minigames**: Feed and Seed, Hammer Chime, Hexoskeleton, Book Bash, and Bowser's Block Party. Playable and checkable in both goal modes.
- **Minigames**: all Free Play minigames, including the twelve 1 vs 3 minigames, configurable in YAML to require winning on both teams separately, or just once regardless of team.
- **Minigame Mode Wins**: Step It Up, Battle Cup, Score Scuffle, Rocket Rascals, Boss Bash (togglable in YAML).
- **Puzzle Mode Goals**: reach a target level or score (your choice, set per-game via YAML sliders) in each of the 6 Puzzle minigames (togglable in YAML).
- **Party Item Pickups**: optionally, picking up each board item/hex for the first time also counts as a check (togglable in YAML).

# Items
- **Board Unlocks** (5): one per board. In Story Mode these stack cumulatively in order. In Party Mode each board only needs its own item.
- **Boss Unlocks** (5): one per boss minigame. In Story Mode, a boss also requires that its matching board be reachable  so bosses naturally unlock in story order.
- **Character Unlocks** (8, minus your starting pick): filler items, purely cosmetic choice of who to play as.
- **Items/Hexes Unlocks** (16): unlock use of each board item/hex (togglable, if off, you can use them freely from the start).
- **Minigame Mode Unlocks** (6): one per sub-mode + Amusement Passes, the general gate for all of them. Both the individual items and the general gate can be independently toggled on/off in YAML.
- **Puzzle Mode Unlocks** (7): same structure as above, with Sky Crystals as the general gate.
- **CPU Level Up** (trap, 0-3 copies depending on your starting CPU difficulty): raises CPU difficulty one level each time you receive it.
- **Filler Dice**: standard filler.

# Goal
Choose one in your YAML:
- **Story Mode**: receive all 5 Board Unlocks and all 5 Boss Unlocks, then beat Bowser's Block Party.
- **Party Mode**: receive all 5 Board Unlocks and win 1st place on all 5 boards, in any order.

Note: like the rest of Manual, the GOAL becoming "available" in your tracker means you *have what you need* to finish — it doesn't verify you've actually played through everything in order. Same honor system as any other Manual restriction.
------------------------------------------------------------------------------------------------------------------------------------------
# Notes / Misc.
- Puzzle Mode goals can be set by Level or by Score (your choice, one setting applies to all 6 games), with individual sliders per minigame either way.
- Boss Minigame Lock, the two Minigame/Puzzle sub-mode toggles (individual items + general gate), and the 1 vs 3 split are all independently configurable — mix and match freely.
- Free Play minigames are never gated by any option they're your guaranteed early checks no matter how you configure everything else.
-------------------------------------------------------------------------------------------------------------------------------------------
