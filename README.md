### Mortal Realms MUD (MrMUD v1.4)

Current active server:  game.mortalrealms.com:4321

Welcome to the official repository preserving the source code, game assets, and documentation for the Mortal Realms MUD engine (MrMUD v1.4), originally released in 1993. This repository serves as a historical archive and a development hub for compiling, running, and maintaining this deeply customized text-based multiplayer engine. 

### Overview

Mortal Realms is a highly modified text-based multiplayer virtual world built upon the classic Merc codebase lineage. Designed for high performance and deep mechanical complexity, MrMUD v1.4 introduced advanced room mechanics, comprehensive quest systems, and highly specialized networking protocols optimized for the terminal connections of its era. 

### Key Structural Features

* Heavily Customized Merc Architecture: Optimized memory structures and specialized data models built for long-term server stability.
* Custom Scripting & Area Formats: Native support for sophisticated mob behaviors, room triggers, and programmatic quest progression.
* High-Performance Engine Core: Engineered to manage low-latency networking, concurrent socket handling, and high-frequency combat loops efficiently.
* Terminal Protocol Support: Built-in handling for rich text coloring, terminal emulation strings, and specialized binary formatting designed for custom clients like MrTerm.

### Repository Contents

The root of this repository contains the fundamental building blocks of the game engine: 

* mrmudsrc14.tar.gz - The complete, historical game engine archive containing the full C source code files, makefiles, system configurations, and baseline area definitions.
* MORTAL REALMS.rtf - Extensive documentation, historical background, design philosophy, and administrative overviews detailing the operational history of Mortal Realms.
* LICENSE - The open-source GNU General Public License v3.0, ensuring this historical codebase remains free and open for community preservation.

### Getting Started

To explore or deploy a local instance of the server, you must first extract the primary codebase components. 

### 1. Extraction

Extract the core source directory using standard terminal utilities:
tar -xzvf mrmudsrc14.tar.gz 

### 2. Prerequisites

Building the legacy C codebase requires standard development environments. For modern environments, ensure you have the following installed: 

* GCC (GNU Compiler Collection) or Clang compiler
* GNU Make utilities
* Legacy 32-bit development libraries (if running on a 64-bit architecture, as older mudlibs rely heavily on 32-bit pointer assumptions)

### 3. Compilation

Navigate to the source directory extracted from the tarball (typically named src) and execute the build automation file:
cd src
make 

### Historical Configuration Note

For developers attempting to mirror the authentic 1990s client experience, the engine includes distinct string parsing blocks engineered to interact directly with the MrTerm custom client interface. Ensure terminal echo and local buffer configurations match standard ANSI telnet sequences if you encounter formatting anomalies on modern clients. 

### License


## Client Preservation (MrTerm v1.3)

This repository proudly archives **MrTerm13.zip**, the authentic Windows 95 terminal client custom-tailored for Mortal Realms. 

* **Compatibility:** While the original source disks are lost, this compiled Win32 executable remains fully functional on modern operating systems, including Windows 11, when launched using Windows Compatibility Mode.
* **Protocol Legacy:** It showcases the specialized, low-bandwidth text compression routines and custom binary headers engineered to eliminate gameplay lag over dial-up networking links.

Compatibility settings:  Run as Windows Vista, Run as administrator, Other settings left unchecked.

This project is licensed under the GNU General Public License v3.0. See the LICENSE file for full details regarding distribution, modification, and open-source compliance rules.
