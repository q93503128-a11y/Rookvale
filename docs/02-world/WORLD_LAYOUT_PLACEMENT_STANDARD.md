# World Layout and Placement Standard

**Status:** Locked design process; individual Region layouts remain Draft until they pass the required review cycle

## Core goal

Rookvale's map must support two things at once:

1. the player can understand the broad direction of normal progression without constant confusion;
2. optional exploration still feels discovered rather than pre-solved by the UI.

The game does not treat obscurity itself as depth.

If the intended task is simply to reach a major settlement or follow the primary route, the environment, roads, landmarks, dialogue, or map should communicate that clearly enough.

Secrets, optional dungeons, rare enemies, alternate routes, and hidden stories may require greater observation.

## Research requirement

Major Region layouts, enemy distributions, dungeon positions, boss placements, and settlement connections are not finalized from intuition alone.

Before a Region layout is locked:

- inspect a broad set of relevant external games/maps;
- normally compare at least 10-20 useful area/layout references;
- include multiple 2D/top-down RPG references, not only 3D open worlds;
- compare navigation clarity, encounter density, dungeon placement, settlement logic, detour value, and later-return structure;
- extract structural principles rather than copying visual geometry.

The active detailed reference record is `../07-research/WORLD_LAYOUT_ENCOUNTER_PLACEMENT_RESEARCH_02.md`.

## Required multi-pass workflow

A Region does not become canonical after one map draft.

### 1. World-logic skeleton

Establish terrain and human use first:

- rivers, lakes, coasts;
- elevation and natural barriers;
- old/new roads;
- settlements;
- crossings;
- agriculture/industry/resource sites;
- strategic positions;
- major historical structures.

Do not begin by scattering gameplay icons across an empty canvas.

### 2. Route graph

Design player movement as a graph independently of decorative art.

Mark:

- primary routes;
- alternate routes;
- loops;
- safe return paths;
- shortcuts;
- dead ends;
- gates;
- later-return branches;
- dungeon entrances;
- travel anchors.

The main progression route must remain readable without forcing the whole Region into one corridor.

### 3. Landmark and discovery pass

Add visual and informational pulls:

- silhouettes;
- ruins;
- towers;
- bridges;
- smoke/lights/activity;
- rumors;
- unusual terrain;
- optional landmarks;
- hidden sites;
- future-return mysteries.

Important destinations should be readable from likely approaches when appropriate.

### 4. Enemy ecology pass

Enemies are placed only after geography and human activity make sense.

Placement considers:

- food/shelter/territory;
- monster or faction ecology;
- human routes/resources threatened;
- terrain that makes the encounter mechanically distinct;
- pack/support relationships;
- ambush logic;
- proximity to settlement/checkpoint;
- threat progression.

Rookvale does not fill empty space with evenly spaced generic encounters.

### 5. Dungeon and boss pass

Every major dungeon/boss site must have a geographic or historical reason to be there.

Examples include mines, forts controlling routes, old estates, tombs, service tunnels, monster nests around resources, smuggling routes, exposed older structures, or later reuse of existing architecture.

Dungeon entrances may be obvious, rumored, hidden, visible-but-inaccessible, accidentally connected from another site, or revealed on a later visit.

### 6. Navigation clarity audit

Test the Region from the perspective of a first-time player.

Verify that the player can normally infer:

- where the nearest major safe settlement is;
- the broad direction of the current major objective;
- which routes appear optional, dangerous, blocked, or exploratory.

Use roads, signs, framing, terrain, traffic, sound, NPC directions, map information, and selective explicit markers where useful.

Rookvale does not refuse a clear objective marker simply because indirect guidance is theoretically more immersive. Ambiguity must create meaningful exploration, not wasted time.

### 7. Curiosity and reward audit

Trace every meaningful detour.

Ask:

- what attracts attention to this path?
- why would the player follow it?
- what does the player receive, learn, see, or unlock?
- is returning to a useful route unnecessarily tedious?

Repeated empty dead ends are treated as a layout problem unless the emptiness itself has intentional narrative value.

### 8. Pacing audit

Avoid mechanical repetition such as fixed-distance combat encounters.

Regions should mix:

- ordinary traversal;
- environmental observation;
- social/NPC spaces;
- small encounters;
- dangerous spikes;
- landmarks;
- discoveries;
- dungeon commitment;
- quiet intervals.

### 9. Reference re-check and self-critique

After the first complete draft, compare it again against strong references.

Explicitly identify where the draft is:

- too linear;
- too confusing;
- too empty;
- too noisy/dense;
- dependent on UI arrows;
- ecologically implausible;
- repetitive in encounter composition;
- arbitrary in dungeon placement;
- inconvenient to revisit;
- visually repetitive.

Revise before locking.

### 10. Playtest override

When implemented, navigation and encounter telemetry/playtesting outrank elegant paper design.

If multiple first-time players repeatedly miss the intended main route, cannot read danger, or stop taking side paths because previous detours felt empty, the layout must be revised.

## Enemy placement standard

Enemy encounters should be authored situations rather than statistical filler.

Useful encounter shapes include:

- territorial predator;
- hunting pack;
- swarm around food/nest;
- ranged enemies exploiting elevation/cover;
- frontline + support composition;
- patrol crossing a road;
- ambush at a plausible choke point;
- monsters occupying abandoned structures;
- rare creature visibly avoidable before engagement;
- competing hostile groups.

The starting Region should communicate danger through geography and behavior rather than only numeric labels.

Maintained roads and settlement outskirts are generally safer. Abandoned roads, deep wilderness, ruins, blocked crossings, dense monster signs, or visibly damaged infrastructure can communicate increasing risk.

## Main route versus optional route

Rookvale distinguishes clarity from completionism.

The player should understand enough to keep playing normally without a walkthrough.

The player should not automatically know:

- every secret;
- every treasure;
- every optional dungeon;
- every rare enemy;
- every shortcut;
- every later-return location.

## 2D presentation requirement

Because Rookvale is 2D, it cannot rely on distant 3D skyline visibility alone.

Equivalent navigation cues must use combinations of:

- screen composition;
- road width/material;
- bridges/gates/fences;
- landmark sprites/silhouettes;
- terrain channels;
- parallax/background structures where appropriate;
- signs;
- smoke/light/motion;
- ambient sound;
- NPC traffic;
- map/journal information.

Important optional destinations can sometimes be deliberately framed within a screen, similar to strong fixed-camera RPG map design, without explicitly marking them as objectives.

## Locked quality principle

> **The player should get lost because they chose to explore, not because the game failed to communicate its basic geography.**
