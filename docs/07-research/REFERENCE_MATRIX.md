# Reference Matrix

**Status:** Active

This document tracks what Rookvale studies from external games and, equally importantly, what it does **not** copy from them.

| Design area | Reference candidates | What to study | Current Rookvale direction |
| --- | --- | --- | --- |
| Overworld -> turn-based encounter structure | Hero of Aethric, Broken Ranks | Exploration rhythm, encounter transition, world-content density, how multiplayer presence survives the transition into battle | Hero of Aethric is the primary structural reference; no GPS. Broken Ranks is a secondary MMO reference |
| Multiplayer exploration | Hero of Aethric, Broken Ranks, Loomian Legacy, WAKFU | Seeing other players, party formation, drop-in/out friction, social presence without overcrowding | Multiplayer is foundational, not a post-launch bolt-on |
| Party turn-based combat | Broken Ranks, For The King II, DOFUS/WAKFU, WAVEN | Simultaneous vs sequential turns, action economy, waiting time, class interaction, party coordination | Still open; multiplayer pacing is the first combat-design problem to solve |
| Combat activity / anti-passivity | Sea of Stars, Broken Ranks, Octopath-style break systems | Timed actions, interruption, telegraphing, resource windows, keeping non-active players engaged | Use selectively; avoid turning every action into a reflex minigame |
| Tactical positioning | DOFUS, WAKFU, WAVEN, Divinity: Original Sin 2 | Whether movement/position creates meaningful choices, readability, encounter layout | Research before deciding whether Rookvale uses a grid, lanes, rows, free positioning, or no positional layer |
| Class identity and party roles | Broken Ranks, DOFUS/WAKFU, traditional party RPGs | Tank/healer/damage/control/support identity, class interdependence, solo viability | Rookvale should support meaningful multiplayer roles without making solo play nonfunctional |
| Class advancement | Hero of Aethric, DOFUS/WAKFU, MMORPG job systems | Branch clarity, specialization depth, unlock pacing, respec rules, avoiding bloated class counts | Branching advancement confirmed in principle; exact tree is open |
| Party finding | Broken Ranks and modern MMOs | Activity filters, class/role filtering, level/power requirements, reducing party-formation friction | Treat party finder as core MMO UX, not late polish |
| Boss encounters | DOFUS/WAKFU, Broken Ranks, For The King II, selected JRPGs | Telegraphing, phases, role value, coordination checks, failure recovery | Open |
| World / content variety | Hero of Aethric, DOFUS Touch, WAKFU, selected open-world RPGs | Regional identity, density of enemies/NPCs/dungeons/events, reasons to revisit old areas | Large handcrafted world with distinct spaces and broad content variety |
| Cross-platform tactical UI | WAVEN, DOFUS Touch, Broken Ranks mobile | Touch targets, HUD density, action selection, readable status info on small screens | Web-first implementation must stay within a Roblox/mobile-portable UI vocabulary |
| Roblox battle / exploration UX | Loomian Legacy and other suitable current Roblox RPGs | Controller/touch/mouse parity, menu scale, battle readability, Roblox player expectations | Research current Roblox games before final UI implementation |
| Pixel world presentation | Hero of Aethric plus selected high-quality pixel RPGs | Sprite scale, silhouette readability, environment density, animation economy, visual cohesion | No fixed cute/dark style yet; quality and readability take priority |
| Inventory / equipment UX | Modern mobile/PC RPGs selected per task | Information hierarchy, comparison speed, tooltips, touch usability | Open |
| Social / party UX | Broken Ranks and modern MMOs | Invite flow, reconnect behavior, party leader authority, readiness, matchmaking | Open |
| Deep system interaction | Divinity: Original Sin 2 | Action-point economy, environmental combinations, party skill interactions | Depth reference only; do not inherit its slower encounter pacing by default |
| Formation systems | Atlantica Online | Front/back placement, role protection, party composition as strategy | Secondary research candidate if Rookvale adopts positional party combat |

## First-pass findings

### Hero of Aethric
- Closest baseline for Rookvale's exploration premise: handcrafted pixel-art world, turn-based encounters, class progression, solo or party dungeon play.
- Useful primarily for **world-to-battle structure**, not as a complete template for combat, progression, UX, or content.
- Rookvale explicitly does not use GPS.

### Broken Ranks
- Particularly relevant because it combines an open MMORPG world with turn-based combat and explicit party roles.
- Combat uses simultaneous planning with a short decision window, proving one way to reduce multiplayer turn waiting.
- Its class-role dependence and party-finder design are useful references.
- Rookvale should study the pacing benefit without automatically adopting a hard timer, which may create pressure and accessibility problems.

### DOFUS / WAKFU
- Long-running evidence that class-heavy, tactical, turn-based MMORPG combat can support a persistent online world.
- Strong references for class identity, positioning, encounter mechanics and party synergy.
- Their grid-heavy tactical model is a candidate, not a decision; Rookvale may need faster and simpler combat for web/mobile/Roblox parity.

### WAVEN
- Highly relevant to cross-platform presentation: tactical turn-based multiplayer designed for PC and mobile.
- Useful for compact battlefields, clear action UI, deck/loadout readability and short-session combat presentation.
- Rookvale does not currently intend to become a deckbuilder; study the UX and combat economy rather than copying the deck structure.

### For The King II
- Useful for four-player cooperative turn-based party play and readable role combinations.
- More useful for co-op encounter structure than for MMO overworld design.

### Sea of Stars
- Useful as a reference for keeping turn-based actions tactile through timed input and interruption/lock mechanics.
- Rookvale should avoid mandatory reflex checks on every action, especially because multiplayer, latency and mobile controls matter.

### Divinity: Original Sin 2
- Strong reference for action-point choices, skill combinations and environmental/systemic interaction.
- Not a pacing target: its encounter complexity and duration would be dangerous to inherit wholesale in a persistent multiplayer game.

### Loomian Legacy
- Useful mainly as a Roblox-native reference for exploration-to-battle transition and cross-device menu presentation.
- Creature collection is not a planned Rookvale core pillar, so its progression structure is not a primary reference.

### Atlantica Online
- Secondary reference for formation-based turn combat and front/back role protection.
- Worth deeper study only if Rookvale chooses a positional formation layer.

## Research rule

References are collected per system. A strong implementation may inspire a principle or mechanic, but the final design must fit Rookvale's own world, combat, multiplayer, pixel-art presentation, and cross-platform constraints.

For major systems, follow `RESEARCH_POLICY.md` before locking a design.
