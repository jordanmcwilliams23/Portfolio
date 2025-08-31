---
title: "Refactor Games"
permalink: /RefactorGames/
layout: single
author_profile: true
---

# Journeyman
*Fantasy MMORPG with Souls-like elements built in Unreal Engine 5.3*
Role: Gameplay Engineer Intern
<iframe src="https://store.steampowered.com/widget/2131360/" frameborder="0" width="646" height="190"></iframe>

##My Work

### Arena
- I significantly enhanced the runtime performance of a cooperative Arena Gamemode, boosting the frame rate from approximately 35 fps to roughly 77 fps, marking an increase of 220%. This enhancement was achieved by minimizing redundant 'Get All Actors of Class' calls, eliminating unnecessary function calls, and optimizing logic executed during Event Tick. Additionally, key sections of C++ code were rewritten for improved efficiency.
- Set-dressed the arena to feature medieval banners, a royalty viewing area, and interactive shopkeeper signs
- Developed a C++ weighted selection algorithm for enemies spawning into the arena for players to fight to add hand-crafted randomization to the player experience
- Utilized Unreal Engine's chaos destruction system to create destructible pillars in the arena that can be interacted with by players and enemies
<iframe src="https://drive.google.com/file/d/1BHpvTbsihrpH7hf3yPegcqHlsi2_29LQ/preview" width="640" height="480" allow="autoplay"></iframe>

### Level Design
- I created a town reminiscent of the 1800s medieval era with a Tim Burton-like aesthetic, named Tombsteel. This town showcases a vast commoners' graveyard at the base level and an elevated, affluent graveyard near a church on a hilltop. My main focus was to ensure that the play areas were expansive enough to support multiplayer gameplay and mechanics, while still preserving the town's somber and gloomy ambiance. Additionally, the town boasts a mausoleum where a deranged necromancer conducted experiments on cadavers, a fittingly designed building that I constructed myself.
<iframe src="https://drive.google.com/file/d/17fh-4tfHqIr7HwzdLHA1cp1qq2Lc4qJ4/preview" width="640" height="480" allow="autoplay"></iframe>
- Built a large-scale PvP map intended for "Capture the Flag" gamemode with two team bases, traversable underground tunnels, and multiple fun engagement points.
<iframe src="https://drive.google.com/file/d/15vBVniBD94NzNrAPzuOg1iu6VE4GDsHs/preview" width="640" height="480" allow="autoplay"></iframe>

### Misc
- I refactored many different systems present in the game which contained suboptimal coding practices and made them work efficiently in a networked multiplayer game, improving framerates ranging from 5% up to 30%.
- Optimized major areas of concern in the game including lighting performance, non-spatialized actors, and more which drastically improved framerate.
- Created a new procedural dungeon system using the asset "Dungeon Architect" with cyclical paths, treasure rooms, random enemy variations, and traps galore!
- Designed a "Demon Knight" cinematic boss encounter with networked events and polished game feel
<iframe src="https://drive.google.com/file/d/1P2KOe9svYXXi5USAQxgq8UKEzlLKiG6D/preview" width="640" height="480" allow="autoplay"></iframe>
- Crafted multiple tools/blueprint utilities to help improve developer's workflows, including a day/night system for lights, a modular rope bridge, an asset thumbnail setter, and a chaos destructible base.
<iframe src="https://drive.google.com/file/d/1uKpsXY4HqY9_xvNmXPWoXl9BHz_INGeI/preview" width="640" height="480" allow="autoplay"></iframe>