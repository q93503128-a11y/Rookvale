# World Structure and Exploration

**Status:** Core world-structure philosophy locked; exact continents, region count, region names, biome themes, settlement rosters, dungeon counts, and route topology remain Draft

## Core world model

Rookvale uses a **handcrafted multi-region open world** rather than one enormous flat seamless map built primarily for scale.

The structural hierarchy is:

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

Regions are large authored spaces made from several connected Areas. Movement inside a Region should feel natural and exploratory. Region-to-Region transitions may use deliberate loading/transition boundaries when useful for performance, art direction, simulation scope, or future platform portability.

The design priority is **density and identity rather than map-size competition**.

## Region progression and Character Tier

Regions are not mapped one-to-one to Character Tiers.

Rookvale does not use a simplistic structure such as:

```text
Tier I = grassland
Tier II = desert
Tier III = snow
```

Instead, each Region has a broad recommended progression range, and those ranges may overlap.

A single Region may contain:

- ordinary routes appropriate to its main progression band;
- harder side paths;
- dangerous pockets intended for later return;
- sealed or hidden content unlocked by future progression;
- bosses or dungeons well above the surrounding area's normal threat level.

This allows the player to encounter something clearly too dangerous, remember it, grow stronger, and return later.

## No universal enemy level scaling

Rookvale does **not** automatically scale ordinary world enemies to the player's current Character Level/Tier.

World areas retain authored threat identities.

Consequences:

- returning veterans can feel their accumulated strength;
- dangerous areas can be entered too early and remain genuinely dangerous;
- earlier enemies can later be defeated much more easily;
- the world communicates progression through actual stats/mechanics rather than hidden level-difference modifiers.

Later content may revisit older Regions through new events, quests, hidden routes, bosses, class content, or newly accessible sub-areas without scaling every old enemy upward.

## Access model

Rookvale mixes three kinds of world access.

### 1. Open dangerous access

Some higher-threat areas can be entered early if the player physically reaches them.

The danger itself is the warning.

This supports sequence experimentation, exploration, and memorable retreats.

### 2. Diegetic gates

Many access restrictions should exist through the world rather than through an arbitrary level-number wall.

Examples include:

- repairing a bridge;
- unlocking a ferry or ship route;
- obtaining a seal/key;
- clearing a blockade;
- gaining faction or NPC permission;
- surviving an environmental hazard;
- opening a mountain pass;
- draining or redirecting water;
- removing a curse or magical barrier.

These gates should strengthen setting coherence and create return routes.

### 3. True progression gates

Hard Character Tier / personal-progression requirements are reserved for content where sequence breaking would damage progression integrity, reward structure, or encounter assumptions.

Examples may include:

- pinnacle endgame content;
- some raids;
- highly progression-sensitive dungeons;
- specific story/advancement structures.

## Region composition

Regions do not follow one rigid repeated template.

A typical Region may include some mixture of:

- one major settlement or hub;
- small villages, camps, outposts, or isolated homes;
- roads and alternate routes;
- wilderness sub-biomes;
- major landmarks;
- one or more major dungeons;
- smaller caves, ruins, lairs, tombs, mines, or similar sites;
- field bosses and rare enemies;
- secret areas;
- quest/event locations;
- progression gates and later-return sites.

Different Regions may deliberately break this pattern.

Examples:

- a dense city-region with little wilderness;
- a near-empty cursed wasteland;
- an island chain;
- a huge underground Region;
- a vertical mountain Region;
- a frontier Region built around scattered camps rather than towns.

## Settlement identity

Settlements should not all be copies of the same service list.

Large regional hubs can provide most essential services, but smaller settlements should express local identity through available services, NPCs, economy, quests, and nearby content.

Examples:

- mining town: ore, smithing, heavy equipment, mine expeditions;
- hunting village: tracking, monster parts, Ranger/Hunter connections;
- religious settlement: healing, relics, Acolyte-related content;
- trade city: broader merchants and economic activity;
- frontier camp: basic supplies and route support rather than full urban services.

Essential catch-up services must remain accessible enough that settlement flavor does not become needless inconvenience.

## Exploration-first map revelation

Rookvale does not populate a newly entered Region with a complete checklist of undiscovered icons.

The intended flow is:

```text
known roads / broad geography / known settlements
-> explore
-> discover landmarks, camps, dungeons, secrets, routes, NPC sites
-> discovered information becomes recorded on the map/journal
```

The player should often discover that something exists rather than merely walk toward a pre-disclosed icon.

## Information-led exploration

World information can reveal **clues** without always revealing exact coordinates.

Sources may include:

- NPC rumors;
- tavern talk;
- maps or sketches;
- books/letters;
- environmental signs;
- quest dialogue;
- scout reports;
- visible distant landmarks;
- faction intelligence.

Examples:

- "strange red light northeast of the village";
- a rumor about a monster near an abandoned watchtower;
- an old map showing a ruin but not a precise entrance;
- a class trainer reported somewhere in a mountain settlement.

The map may mark an approximate search region or clue rather than placing an exact objective pin by default.

Players should also be able to place their own map pins/notes if the UI supports it.

## Discovery rewards

Exploration is a legitimate progression activity.

Discoveries can grant Character XP and, depending on significance, may also grant or unlock:

- crafting recipes;
- blueprints;
- rare materials;
- equipment;
- Unique/Relic opportunities;
- class or advancement clues;
- lore and collection entries;
- Fast Travel access;
- shortcuts/routes;
- quests or NPC relationships.

Discovery reward scale should depend on significance. Walking across every trivial map cell does not need to produce reward spam.

## Exploration journal / completion

Rookvale may track Region discoveries through an exploration journal.

Possible categories include:

- major locations;
- discovered dungeons;
- local stories;
- rare creatures;
- major landmarks;
- notable secrets.

Exact presentation remains Draft.

100% Region completion is optional and must not become a universal requirement for Character Tier advancement or ordinary best-in-slot combat progression.

Completion rewards may exist for players who enjoy systematic exploration, but exploration must remain discovery rather than compulsory map-cleaning.

## Fast Travel

Fast Travel is intentionally convenient after exploration has earned it.

Candidate Fast Travel points include:

- towns/cities;
- important camps;
- shrines/waystones/setting-specific travel nodes;
- major discovered dungeon entrances where repeat farming would otherwise create pointless travel repetition.

General rule:

> discover a valid travel point once, then use it later.

The network should be useful but not so dense that walking through the authored world becomes irrelevant.

Rookvale does not adopt a default design where repeated long-distance travel is itself a punitive resource-management system.

## Dungeon discovery and entry

Most ordinary dungeons exist physically in the world.

The default first-time flow is:

```text
explore world
-> discover dungeon entrance
-> enter
-> dungeon/party instance as appropriate
```

The game does not primarily expose undiscovered dungeons as a menu list detached from geography.

After discovery, repeat-play convenience may allow Fast Travel or other quick return to the entrance.

First discovery remains exploration; repetition may prioritize convenience.

## Dungeon scale variety

Not every discovered interior is a long dungeon.

Rookvale supports several scales of authored combat/exploration site.

Working categories:

### Micro Site

Very short cave, ruin, shrine, cellar, nest, hidden room, or similar encounter site.

Typical purpose:

- treasure;
- short fight;
- lore;
- secret;
- rare resource;
- environmental puzzle.

### Small Dungeon

Compact multi-room/site experience with several encounters and potentially a miniboss or focused objective.

### Major Dungeon

A substantial authored location with multiple sections, bespoke mechanics, events, narrative/environmental identity, checkpoints, and major boss content.

### Expedition / Raid / Deep Dungeon / Challenge format

Separate advanced structures using the failure/retry contracts defined in `DEATH_FAILURE_RETREAT.md`.

Exact playtime ranges are not locked; variety and identity matter more than fixed duration labels.

## Returning to old Regions

Older Regions remain relevant without globally scaling their original enemies upward.

Reasons to return may include:

- previously inaccessible sealed areas;
- later quests;
- class advancement content;
- high-threat bosses seen early;
- new NPC incidents;
- special materials;
- newly acquired traversal/access capabilities;
- hidden routes;
- endgame events that intentionally revisit a location;
- collection/exploration goals.

The ordinary early enemies may remain weak, preserving the player's sense of growth, while later content provides new reasons to revisit the Region.

## Exploration density invariant

A major world-design rule is:

> **Leaving the obvious road should regularly produce meaningful feedback.**

Not every side path needs combat loot, but repeated empty detours teach the player to stop exploring.

Possible meaningful outcomes include:

- treasure;
- NPC encounters;
- unusual scenery/landmarks;
- hidden paths;
- shortcuts;
- lore/environmental storytelling;
- rare enemies;
- resources;
- quests/events;
- future-return mysteries;
- dangerous encounters;
- access to other routes.

This does not mean placing a collectible every few seconds. It means authored detours should usually justify curiosity.

## Technical/platform direction

The multi-Region structure also supports Rookvale's web-first implementation and later portability goals.

Benefits include:

- bounded asset/simulation scopes;
- easier loading and streaming;
- stronger regional art/audio identities;
- easier multiplayer instance management;
- less dependence on one massive continuously loaded map;
- cleaner adaptation to Roblox/mobile constraints later.

Technical convenience does not dictate the fiction, but world partitioning should be planned from the start rather than retrofitted after a seamless prototype.

## Design invariants

1. Handcrafted density is valued over raw square-kilometer scale.
2. Regions are authored places, not one-Tier biome stages.
3. Ordinary enemies do not universally scale to the player.
4. Recommended Tier ranges may overlap and dangerous pockets may exist inside safer Regions.
5. High-level areas are often physically reachable early unless a real gate is justified.
6. Diegetic gates are preferred over arbitrary numeric doors.
7. The map reveals discovery rather than presenting the whole Region as an icon checklist.
8. Exploration grants real progression and utility rewards.
9. Fast Travel becomes convenient after discovery.
10. Most dungeons have real world entrances and must initially be found.
11. Dungeon scale varies substantially.
12. Old Regions receive later reasons to revisit without erasing growth through universal scaling.
13. Side-path exploration should regularly reward curiosity.

## Open questions

- world/continent count;
- launch Region count;
- final Region names and cultures;
- biome and climate distribution;
- region-to-region topology;
- exact recommended Tier ranges;
- starting Region and starting settlement;
- sea/island/underground scope;
- exact Fast Travel fiction and density;
- map fog/revelation presentation;
- exact exploration journal UI;
- traversal mechanics, if any;
- settlement service/economy distribution;
- exact dungeon density per Region;
- world-event placement and persistence;
- day/night/weather effects on exploration.
