# Historical Preservation: Strategy Plus Magazine Feature (April 1995)

This document preserves the gameplay mechanics, architectural insights, and server statistics of the **Mortal Realms MUD (MrMUD v1.4)** as documented in its major print media feature. 

The following data has been transcribed and reconstructed from **Computer Games Strategy Plus (Issue No. 53, April 1995)** in a review written by J. Grant Bell entitled *"MORTAL REALMS: Over the Net"*.

---

## 📋 Review Overview & Legacy Nodes
In the mid-1990s, Mortal Realms stood out in the MUD community for its operational stability, large-scale custom world, and custom split-screen terminal interface.

* **Publication Date:** April 1995
* **Historical Host Node:** `hydrogen.ee.utulsa.edu 4321`
* **Historical IP Mapping:** `129.244.42.48 4321`
* **Scale of the World:** 15,000+ custom-built rooms distributed across 5 major distinct continents.

---

## 🎲 Character Creation & Stat-Rolling Engine
The review details the specific math behind the Mortal Realms character generator. Unlike stock codebases, character generation leveraged a hidden compilation matrix to evaluate rolls.

### The Composite Score Scale
Every newly generated character received a composite valuation score calculated across the core six attributes (**Strength, Dexterity, Constitution, Intelligence, Wisdom, Charisma**):
* **13.0:** The baseline average for a standard automated character roll.
* **14.4:** The minimum competitive composite recommended by veteran players before keeping a character.
* **14.6:** An elite tier roll, typically requiring approximately 15 minutes of continuous fast-rolling to pop up.
* **14.8+:** Classified as an exceptional "real find" with idealized maximum baseline stats.

### Core Stat Influences
* **Wisdom:** Dictated the exact number of practice/skill advances a player received upon gaining a new level.
* **Intelligence:** Formed the mechanical ceiling for how high a player could train specific spell masteries and martial skills.
* **Constitution:** Explicitly determined the maximum hit point depth gained per level marker.

---

## 🔀 Multi-Class System & Progression Meta
Mortal Realms featured a highly integrated multiclass system that departed drastically from traditional rigid Merc class limits.

* **The Conversion Threshold:** Characters could choose to pivot or convert into entirely different primary professions at milestone intervals (such as reaching 10th level).
* **The Strategic Meta:** A popular strategic route included starting a character as a **Ranger** to secure universal weapon usage and heavy armor allowances early on, then converting into a specialized casting or stealth role (like **Assassin** or **Illusionist**) at later levels.
* **The Single-Class Reward:** To balance multi-class flexibility, the absolute highest-tier spells and maximum skill limits were structurally locked to purist characters who stayed dedicated to a single profession through level 20 and beyond.

---

## 🗣️ The Language & Communication Grid
To build immersion and partition high-level communication, the engine featured a localized linguistic translation barrier.

* **The Gibberish Filter:** If characters did not share an identical known language, all adjacent or global text strings sent over the network parsed as randomized gibberish syllables.
* **The `speak` Protocol:** Players used the `speak <language>` command to explicitly toggle between known regional dialects (e.g., *Dwarf, Gnome, Orc*).
* **Linguistic Acquisition:** Characters could gradually master new dialects naturally by gaining levels, or artificially bypass communication barriers by tracking down and buying rare language potions from specialized local magic vendors.

---

## 🖥️ Screen Layout & Client-Server Telemetry
The magazine featured direct terminal screens demonstrating the visual interface powered by the server's VT102 screen-splitting engine and the **MrTerm** client.

### Visual Layout Map
```text
+-----------------------------------------------------------------------------+

| Salamander the Assassin                        Sp:Dwarf FX:none Lev: 1      |
|-----------------------------------------------------------------------------|
| [Main scrolling output text window: room descriptions, combat rounds,      |
|  and language strings show here...]                                         |
|                                                                             |
|                                                                             |
|-----------------------------------------------------------------------------|
| H: 22/22  Mn:100 Mv:103  Ex:0         Gd:0          Exit: NESW      3:13pm  |
|-----------------------------------------------------------------------------|
| Alt-Z for Help | VT102   |  57600-N81 FDX |                 | Online 00:23  |
+-----------------------------------------------------------------------------+
```

### Element Breakdown
1. **Header Display String (Row 1):** Tracks current character name, title handle, active language/species flag (`Sp:Dwarf`), current status ailments/spell buffs (`FX:none`), and level marker (`Lev: 1`).
2. **Dynamic Middle Info Bar (Row 22):** Provides continuous tracking of Vitals (`H:` Health, `Mn:` Mana, `Mv:` Movement), raw Experience (`Ex:`), Gold reserves (`Gd:`), visible room exits (`Exit:`), and real-time server time tracking.
3. **Terminal Configuration Footing (Row 24):** Details the active client emulation flags (`VT102`), serial transmission properties matching high-speed dial-up parameters (`57600-N81 FDX`), and session length tracking (`Online`).
