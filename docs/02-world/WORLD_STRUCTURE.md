# World Structure

**Status:** Core world model and initial macro-world shape locked; final Region names, exact borders, cultures, detailed geography, and route topology remain Draft

## Confirmed direction

Rookvale uses a **handcrafted multi-Region open world** with strong regional identity, dense exploration, meaningful settlements, physically located dungeons, and fixed authored danger rather than universal player-level scaling.

Detailed exploration, map-revelation, Fast Travel, dungeon-discovery, revisit, and density rules are defined in [`../01-gameplay/WORLD_STRUCTURE_EXPLORATION.md`](../01-gameplay/WORLD_STRUCTURE_EXPLORATION.md).

The long-term initial Lv80 macro-world target is defined in [`WORLD_MACRO_REGIONS.md`](WORLD_MACRO_REGIONS.md).

Narrative delivery, naming, historical layering, and environmental-storytelling rules are defined in [`WORLD_NARRATIVE_AND_NAMING.md`](WORLD_NARRATIVE_AND_NAMING.md).

## Canonical hierarchy

```text
World
└ Region
   └ Area
      ├ Settlement
      ├ Wilderness
      ├ Landmark
      ├ Dungeon
      ├ Boss Lair
      ├ Secret
      └ Event Site
```

Regions are large authored spaces made from several connected Areas. Region boundaries may use deliberate loading/transition points where useful for performance, art direction, multiplayer scope, or future Roblox/mobile portability.

Rookvale prioritizes **density and place identity over raw map size**.

## Initial macro-world planning target

The first complete long-form world is currently planned around:

- 8 principal surface Regions on one main landmass;
- one dispersed sea/island macro-region (working label `Outer Isles`);
- one connected underground macro-region (working label `Deepways`).

Only `Rookvale` is currently an established in-world Region name. Other macro labels remain production descriptors until culture-specific naming systems are researched and designed.

This planning target does not mean all Regions are built before the first playable release.

## Region and Tier relationship

Regions do not map one-to-one to Character Tiers.

Each Region has a broad recommended progression range, and ranges may overlap. A single Region can contain:

- ordinary routes appropriate to its main progression band;
- stronger side paths;
- dangerous pockets intended for later return;
- sealed or hidden locations unlocked later;
- bosses/dungeons well above surrounding threat.

This allows the player to discover dangerous content early, remember it, grow, and return later.

## Fixed authored danger

Ordinary world enemies do **not** universally scale to the player's Character Level/Tier.

This preserves:

- visible growth when returning to earlier Regions;
- genuinely dangerous higher-level areas;
- meaningful early sequence exploration;
- world threat communicated by actual enemy stats/mechanics rather than hidden level-difference rules.

Old Regions stay relevant through later quests, newly opened routes, bosses, class content, materials, events, and hidden areas rather than through blanket rescaling.

## Access philosophy

Rookvale mixes three access patterns.

### Open dangerous access

Some high-threat places are physically reachable early. Their danger is the warning.

### Diegetic gates

Whenever reasonable, the world itself explains access restrictions through things such as:

- bridges/ferries/routes;
- seals and keys;
- environmental hazards;
- faction or NPC permission;
- curses/barriers;
- blockades;
- water-level or terrain changes.

### True progression gates

Hard Character Tier/personal-progression gates are reserved for content where sequence breaking would damage progression integrity, reward structure, or encounter assumptions.

## Settlements

Settlements should be useful and memorable rather than copies of one universal service template.

Large hubs may provide most essential services. Smaller settlements should reflect local economy, culture, professions, nearby monsters, factions, class ties, and quest activity.

Regional flavor must not make basic progression services unreasonably inconvenient.

Settlement placement must make geographic/economic sense. Fishing communities need useful water; mining settlements need extraction and transport routes; forts must control something worth controlling; market towns need roads, river access, hinterlands, or other actual reasons to exist.

## Exploration principles

Rookvale does not reveal a Region as a complete checklist of undiscovered icons when the player arrives.

The intended flow is:

```text
known roads / broad geography / known settlements
-> explore
-> discover places, routes, dungeons, landmarks, secrets, NPC sites
-> record discovered information on the map/journal
```

NPC rumors, maps, books, visual clues, faction reports, and similar information can point toward approximate areas without always giving exact coordinates.

Exploration can grant Character XP and unlock routes, Fast Travel, recipes, blueprints, materials, equipment opportunities, lore, quests, class clues, and other meaningful rewards.

A core world-design invariant is:

> **Leaving the obvious road should regularly produce meaningful feedback.**

That feedback may be treasure, an NPC, scenery, lore, a shortcut, a hidden route, a dangerous encounter, a resource site, a quest/event, or a mystery meant for later return.

## Narrative geography

World layout also communicates history.

Roads, borders, settlements, ruins, industries, abandoned structures, reused buildings, enemy occupation, and changed travel routes should provide evidence about how the world developed.

Rookvale avoids depending on a single exposition NPC or long mandatory lore sequence to explain these relationships. The player can learn deeper history by combining environmental evidence with partial accounts from multiple NPCs and sources.

## Fast Travel

Fast Travel is intentionally convenient **after discovery**.

Likely travel anchors include towns, major camps, shrines/waystones or setting-specific equivalents, and selected repeat-play dungeon entrances.

The network should reduce repetitive travel without making authored movement through the world irrelevant.

## Dungeons

Most ordinary dungeons have physical entrances in the world and must be discovered initially through exploration.

After discovery, repeat-play convenience may allow Fast Travel or similar quick return.

Dungeon/site scale varies substantially:

- Micro Sites;
- Small Dungeons;
- Major Dungeons;
- Expeditions;
- Raids;
- Deep/Challenge formats.

Not every cave or ruin is a long commitment.

Failure/retry rules are defined separately in [`../01-gameplay/DEATH_FAILURE_RETREAT.md`](../01-gameplay/DEATH_FAILURE_RETREAT.md).

## Starting-area requirements

The opening Region is `Rookvale`.

It should demonstrate the game's identity quickly through:

- a memorable starting settlement;
- low-risk nearby exploration;
- several genuinely different enemy behaviors;
- at least one reason to party up;
- a dungeon or equivalent focused activity;
- visible signs of places that are too dangerous or inaccessible for now;
- optional discoveries that keep the opening route from feeling scripted;
- at least one later-return mystery or gate;
- visible evidence that the Region used to be busier or function differently;
- several NPCs whose partial observations together communicate local history without one lore lecture.

## Platform implications

The multi-Region structure supports web-first development and later Roblox/mobile portability by keeping asset, simulation, multiplayer, and loading scopes bounded.

Technical partitioning supports the world design; it does not replace authored geography or regional fiction.

## Open questions

- final Region names and naming families;
- detailed cultures and factions;
- exact biome/climate distribution;
- final Region-to-Region topology;
- exact recommended Tier ranges;
- detailed Rookvale map and settlement layout;
- exact sea/island/underground routes;
- Fast Travel fiction and final density;
- map fog/revelation presentation;
- exploration journal presentation;
- traversal mechanics;
- settlement service/economy distribution;
- dungeon density per Region;
- world-event placement/persistence;
- day/night and weather systems;
- detailed political/religious history.
