# Rookvale Starting Region Layout Research 01

**Status:** Active research record. Structural lessons only; no external map geometry, names, enemy kits, or exact content is copied.

## Research question

How should Rookvale's first Region be arranged so that:

- a first-time player can read the broad direction of normal progression;
- optional exploration remains voluntary and rewarding;
- side paths reconnect conveniently rather than creating repeated backtracking;
- enemy distribution feels ecological and authored rather than evenly sprinkled;
- dungeons and bosses have geographic/historical reasons to exist;
- dangerous future content can be seen early without blocking ordinary progression;
- the layout works in a 2D pixel presentation rather than depending on a 3D skyline;
- the Region remains useful when the player returns at higher Character Tiers.

## Reference set inspected

The broader reference pass includes or cross-checks lessons from:

- Elden Ring / Limgrave;
- Xenoblade Chronicles / Bionis' Leg and Gaur Plain;
- Xenoblade Chronicles X;
- Xenoblade Chronicles 3;
- The Legend of Zelda: Breath of the Wild;
- CrossCode / Autumn's Rise and Bergen Trail;
- TUNIC;
- Hyper Light Drifter;
- Dark Souls / Undead Burg and interconnected-world structure;
- Demon's Souls early-world teaching structure;
- Hollow Knight / Forgotten Crossroads;
- Chained Echoes / Rohlan Fields;
- Crystal Project;
- UNSIGHTED;
- Octopath Traveler II;
- Outward;
- Sable;
- Children of Morta for encounter-density and level-iteration lessons;
- selected open-world/level-design production material such as Horizon Forbidden West blockout/iteration methodology.

The strongest retained references for the first Region are not necessarily the most visually similar games. They are the references that solve a specific navigation, pacing, encounter, or iteration problem.

## Retained lessons

### 1. Main direction can be clear without pre-solving the map

Xenoblade's field design deliberately gives the player a story destination while placing tempting detours along the route. The important part is that returning from those detours is not excessively inconvenient.

Xenoblade Chronicles 3 later added optional navigation assistance because elevation and complex terrain could create frustration when players could not infer the route. The lesson is not to add a permanent breadcrumb line by default; it is to provide a fallback when authored geography alone is insufficient.

Rookvale therefore separates:

- **basic navigation clarity**, which should be easy;
- **optional discovery**, which may remain uncertain.

### 2. Visible curiosity targets matter

Elden Ring's open-world philosophy strongly supports seeing a place and being able to go investigate it.

TUNIC similarly distinguishes essential information, which is often placed where the player is likely to find it, from deeper optional knowledge, which may be hidden or require reinterpretation.

For a 2D game this means composing screens so bridges, towers, smoke, unusual tree lines, cliffs, large ruins, moving silhouettes, roads, lights, or other landmarks pull the eye even without an objective icon.

### 3. Side paths need value and convenient re-entry

Dark Souls and Xenoblade both demonstrate the value of routes that reconnect, unlock shortcuts, or produce spatial understanding rather than remaining isolated dead-end branches.

A detour does not always need equipment, but it should regularly provide one or more of:

- a shortcut;
- a new sightline;
- a landmark;
- an NPC;
- a dungeon/site;
- treasure/material;
- a boss/rare encounter;
- lore/environmental evidence;
- a later-return mystery;
- a second route into another Area.

### 4. Open spaces still need authored structure

Xenoblade Chronicles X explicitly discussed the difficulty of helping players understand what to do in very large fields and used field segmentation/activities to give large spaces readable structure.

Rookvale should not create a large empty field solely to communicate scale. A 2D field needs terrain channels, road hierarchy, landmarks, quiet spaces, encounter pockets, and route intersections.

### 5. Enemy density must be tuned, not maximized

CrossCode development records show an exploration area being remixed to reduce enemy density while increasing reward and speeding progression/looting. Its area design also deliberately varied map structure and used branching paths rather than repeating one corridor shape.

Hyper Light Drifter emphasizes tactical encounter compositions instead of cannon-fodder enemies waiting in place.

Rookvale therefore avoids:

- one encounter every fixed number of tiles;
- enemies filling every side route;
- identical packs repeated across adjacent screens;
- monsters standing in places that make no ecological or tactical sense.

### 6. Early strong enemies teach world rules when they are avoidable

Souls games and Xenoblade use early encounters that communicate that not every visible threat is intended to be fought immediately.

The Rookvale starting Region can include a clearly avoidable over-Tier creature/site, but it must not sit on the only understandable progression route.

### 7. First Region should teach the grammar of later Regions

Strong opening areas teach more than combat controls. They introduce:

- safe versus dangerous route cues;
- optional detours;
- shortcut logic;
- readable monster territories;
- visible future-return spaces;
- small versus major dungeon commitments;
- environmental storytelling;
- the value of returning to town or a checkpoint.

The first Region should establish these expectations before later Regions become larger or less forgiving.

### 8. Layout must be iterated as a graph before art polish

Horizon Forbidden West production material describes paper prototypes, blockout/greybox, first playable testing, and repeated iteration before final presentation.

For Rookvale, Region art should not lock a bad movement graph in place. The route graph is reviewed before decorative polish.

## Candidate topology comparison

### Candidate A — Central hub and three spokes

Structure:

```text
         North
           |
West -- Settlement -- East/river
           |
         South
```

Strengths:

- extremely readable;
- easy tutorialization;
- easy to control difficulty by direction;
- simple Fast Travel logic.

Failures:

- feels artificially arranged around the player;
- repeated return through the same hub;
- side paths tend to become isolated dead ends;
- weak sense of a real road network;
- the Region can feel like a level-select wheel disguised as geography.

Verdict: reject as the main topology, though a settlement may still function as a local service hub.

### Candidate B — Asymmetric valley loops

Structure:

- one obvious old north-south road;
- settlement offset near the principal river crossing rather than geometrically centered;
- south fields form the low-risk introduction;
- west paths branch into woodland/upland exploration and later reconnect to the northern road;
- east bank is a smaller optional/high-risk pocket visible from the settlement/bridge;
- northern road narrows toward the first Major Dungeon and next-Region route;
- at least one Small Dungeon creates a functional shortcut or route relationship rather than existing as an isolated cave.

Strengths:

- main route remains legible;
- loops reduce return friction;
- geography looks less player-centric;
- distinct enemy ecologies fit naturally by sub-area;
- Major Dungeon can plausibly control the northern route;
- high-threat content can remain visible but optional;
- supports later-return routes without replacing the original low-Tier space.

Risks:

- needs strong 2D road/landmark framing so loops do not become visually muddy;
- too many cross-links would reduce the feeling of distance;
- east-bank danger must be telegraphed clearly enough that new players do not mistake it for the required path.

Verdict: strongest base topology.

### Candidate C — Split-bank / twin-settlement network

Structure:

- the river divides the settlement and opening Region into two heavily used banks;
- multiple bridges/roads offer immediate route choice;
- dungeons and later routes can be approached from several directions.

Strengths:

- strong realism for a river/trade settlement;
- high route redundancy;
- excellent later-return and shortcut potential;
- many opportunities for environmental storytelling through different districts.

Failures for the opening Region:

- too much information immediately;
- difficult to establish one obvious safe orientation route;
- higher risk of map/UI dependence in 2D;
- central settlement itself becomes more expensive to build before the core exploration loop is proven.

Verdict: retain ideas for a later major city/Region, not the first vertical slice.

## Recommended topology

Use Candidate B as the current preferred draft.

The first Region should not become a literal three-spoke hub or a labyrinth. It should feel like a real valley whose old road and river crossing make the broad geography understandable, while loops and side terrain create optional discovery.

## Enemy-placement lessons for Rookvale

### Maintained road

- lowest ordinary encounter density;
- travelers/guards/farm workers or signs of use communicate relative safety;
- any attack here should feel like a meaningful breach rather than background noise.

### Farmland and river margin

- small scavengers, crop feeders, burrowers, river-edge predators, or displaced creatures;
- enemy presence concentrated around hedges, abandoned fields, water, nests, livestock remains, or damaged storage rather than the center of every road.

### Woodland/upland branch

- hunting packs and territorial predators;
- ambushes only where vegetation/topography supports them;
- a Field Boss territory foreshadowed through tracks, carcasses, damaged fencing, warnings, sound, or visible movement.

### Abandoned northern road

- higher danger and more intelligent occupation;
- ruined checkpoints, barricades, abandoned inns, carts, or walls create tactical positions;
- enemies may use elevation, cover, patrol routes, or support relationships rather than simply having larger numbers.

### Optional over-Tier pocket

- one readable high-threat creature/site rather than a dense high-level zone covering an ordinary route;
- visible before commitment;
- avoidable;
- remembered for later return.

## Dungeon-placement lessons

### Small Dungeon

Preferred first-slice role: a quarry, service tunnel, drainage site, mine, cellar network, or similar place whose location follows local economy/geography.

It should ideally connect to the route graph by:

- opening a shortcut;
- revealing another exit;
- showing a later sealed branch;
- explaining local monster movement;
- creating a useful connection between west exploration and the northern route.

### Major Dungeon

Preferred first-slice role: a fortified road-control site near the narrowing northern route.

It exists because there is something worth controlling: the pass/road/crossing into the next area.

The location can combine multiple historical layers and later reveal a deeper or older structure, but the player's first understanding should remain simple: this is a former route-control facility now made dangerous by its current occupants.

## Navigation fallback

The map should make the main route legible through world design first.

If the active objective remains difficult to locate, the game may provide an optional navigation aid such as:

- direction/distance in the journal/map;
- a temporary compass pointer;
- an accessibility/navigation setting;
- clearer NPC directions;
- a highlighted known road.

The default should not require following a glowing breadcrumb line across every screen.

## Draft audit checklist for the next map pass

Before Candidate B is locked, build a node/route draft and check:

1. Is the north-south road recognizable from every major junction?
2. Can a player leave town and find the safe southern area without UI help?
3. Can the west detour rejoin useful routes without a long backtrack?
4. Is the high-threat east pocket visibly optional?
5. Does every dungeon location have a geographic/historical reason?
6. Are quiet screens present between authored encounter pockets?
7. Are at least several detours non-combat discoveries?
8. Are encounter compositions distinct by sub-area?
9. Does the player see at least one future-return mystery early?
10. Can the Major Dungeon be reached by a route that feels inevitable in hindsight but not corridor-like?
11. Does completing the Small Dungeon improve spatial understanding or traversal?
12. Can the first implemented slice be reduced without breaking the Region's eventual topology?
