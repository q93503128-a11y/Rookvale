# World Layout, Encounter Placement, and Readability Research 02

**Status:** Active research record and required design protocol

## Purpose

Rookvale's world, starting Region, enemy ecology, dungeon entrances, landmarks, and traversal routes must not be laid out from intuition alone.

This document records a broad reference pass and defines a repeatable process for producing and auditing world layouts before they become canonical.

The user-facing goal is deliberately dual:

> **The basic direction of play should be easy to understand, while optional exploration should still feel self-discovered.**

Rookvale should not force players to consult an external map just to understand the main route, but it also should not cover the world in objective arrows and undiscovered icons.

## Reference games and retained lessons

### Elden Ring

Useful lessons:

- a broad route can be suggested without preventing detours;
- visible major landmarks create destination pull;
- caves, ruins, tunnels, field bosses, and legacy-scale dungeons coexist at different scales;
- dangerous enemies can be visible early without becoming mandatory blockers;
- the world should support several viable traversal/combat approaches rather than force one exact route.

Risk to avoid:

- a 2D web RPG cannot rely on distant 3D skyline visibility as heavily, so equivalent guidance must also use road geometry, silhouettes, map framing, signage, NPC clues, terrain channels, and screen composition.

### Breath of the Wild

Useful lessons:

- landmarks and topography can form a mental map;
- major paths and districts can be legible without dense waypoint UI;
- high places and visible destinations help players choose their own route;
- terrain can hide/reveal points of interest in deliberate rhythm.

Risk to avoid:

- extreme legibility can make geography feel artificially partitioned if every region is designed primarily as a perfect navigation diagram.

### Ghost of Tsushima

Useful lesson:

- directional guidance can be integrated into the world presentation rather than always shown as a floating HUD arrow.

Rookvale does not need to copy Guiding Wind. The structural lesson is to use diegetic/visual guidance where it is clearer than another UI marker.

### Xenoblade Chronicles / Xenoblade Chronicles X

Useful lessons:

- visible places should often be genuinely reachable or meaningfully contextualized;
- hard-to-reach detours need worthwhile content;
- unusually strong unique monsters can make the world feel independent of player level;
- landmarks and fast-travel anchors support exploration of very large spaces;
- side exploration should be designed so returning to the main path is not unnecessarily tedious.

Risk to avoid:

- huge empty expanses only justified by spectacle do not fit Rookvale's density-first 2D structure.

### The Witcher 3

Useful lessons:

- settlement placement should follow roads, water, farmland, industry, defense, and local economy;
- monster encounters and abandoned locations work better when local conditions explain why they are there;
- an introductory region can teach the broader world's loop without being a tiny linear tutorial corridor.

Risk to avoid:

- dense map-question-mark cleanup is not Rookvale's exploration model.

### Skyrim

Useful lessons:

- roads naturally connect major settlements while nearby ruins/caves pull the player sideways;
- random or semi-random encounters can make roads feel lived in;
- silhouettes and unusual structures create curiosity before formal discovery.

Risk to avoid:

- procedural/radiant content must not replace authored location identity.

### CrossCode

Useful lessons:

- a 2D/top-down Region can contain a clear macro route while individual screens/rooms support many optional branches;
- side caves, puzzles, observation sites, shortcuts, and treasure can make compact regions dense;
- region maps can be connected in a graph rather than one straight corridor;
- old areas can gain later content and reasons to return.

Risk to avoid:

- Rookvale should not repeat a fixed `field -> town -> temple` structure in every Region.

### Hyper Light Drifter

Useful lessons:

- 3D level-design principles can transfer to 2D spaces;
- map readability and uncertainty can coexist;
- hard enemies, secrets, visual storytelling, and exploration can share the same rooms;
- combat scenarios should be tactical compositions, not piles of filler enemies;
- extensive playtesting is essential when the game deliberately reduces explicit handholding.

Risk to avoid:

- Rookvale uses text/dialogue and should not inherit Hyper Light Drifter's self-imposed near-textless communication constraint.

### Octopath Traveler II

Useful lessons:

- with a fixed camera, desirable destinations can be deliberately framed on the current screen;
- reachable-looking treasure, ladders, waterways, town silhouettes, and dungeon clues create exploratory pull;
- different traversal methods can make previously seen geography newly useful.

This is especially relevant to Rookvale's eventual 2D presentation.

### Chained Echoes

Useful lessons:

- large 2D towns can feel like places rather than service menus;
- later traversal tools can reopen the map and support revisits;
- world-map structure can create a sense of connected geography even without one continuously simulated surface.

Risk to avoid:

- oversized towns are expensive to populate convincingly; settlement size must be justified by actual content and population logic.

### Outward / Crystal Project and similar nonlinear RPG structures

Useful lessons:

- Regions can have authored danger rather than automatic level scaling;
- stronger areas may be encountered before the player is ready;
- exploration order can be flexible without making every route equally safe;
- a small number of strongly differentiated Regions can feel larger than a long list of shallow biomes.

## Main-route readability contract

Rookvale must distinguish **orientation** from **discovery**.

The player should normally be able to answer:

1. where is the nearest settlement / safe return route?
2. what is the broad route toward my current major objective?
3. which nearby path is obviously optional or more dangerous?

The player does **not** need to know in advance:

- every secret;
- every dungeon entrance;
- every rare monster;
- every treasure;
- the exact contents of every side route.

### Guidance tools available to designers

Use a mix of:

- primary road hierarchy;
- bridges, gates, ferries, passes, and other natural route funnels;
- distinctive silhouettes / structures;
- visible destination framing on screen;
- road signs and local signage;
- NPC direction and rumor language;
- terrain elevation / river channels / walls / hedges / cliffs;
- lighting, animation, sound, smoke, water, banners, traffic, or other visual activity;
- map/journal broad objective areas;
- optional explicit pins for accessibility or direct quests when ambiguity would add nothing.

Rookvale does not treat withholding directions as inherently sophisticated. If the intended task is simply `reach the town`, the town should not be hidden behind needless confusion.

## Side-path contract

A side path can be subtle, but after the player commits time to following it, it should usually justify that curiosity.

Possible payoffs:

- treasure;
- shortcut;
- rare enemy;
- strong enemy visible for later return;
- environmental story;
- NPC;
- micro-site;
- dungeon entrance;
- material node;
- scenic landmark;
- class / quest / world clue;
- alternate connection to another Area.

Repeated empty dead ends are a failure unless emptiness itself is intentionally communicating something specific.

## Enemy-placement research rules

Enemy placement is not `fill empty tiles with mobs`.

Each ordinary encounter must answer at least one of:

- what is this creature doing here?
- what does it feed on / defend / hunt / infest?
- what human route or resource does it threaten?
- what terrain makes this enemy tactically interesting?
- what other creature/faction does it coexist or conflict with?
- what does the encounter teach before a harder version appears?

### Encounter composition

Use varied compositions:

- isolated predator;
- pack / swarm;
- territorial creature near nest;
- ranged enemy using terrain;
- support + frontline pair;
- patrol crossing a road;
- ambush near a plausible choke point;
- monster occupying an abandoned human structure;
- rare/elite creature visible before engagement;
- conflict between two hostile groups the player may exploit or avoid.

Avoid repeatedly dropping statistically equivalent groups at fixed intervals along roads.

### Safety gradient

The starting Region should have readable threat gradients.

The route immediately around the main settlement is safer, but not sterile. Moving away from maintained roads, approaching abandoned structures, entering dense wilderness, crossing natural barriers, or following visibly damaged routes can raise danger.

This creates readable risk without requiring an explicit `Level 12 Zone` banner.

## Dungeon-placement rules

A dungeon entrance needs a reason to exist at its location.

Examples:

- mine near an extraction settlement;
- fort controlling a pass/bridge;
- tomb near an old settlement or religious site;
- drainage/service tunnels under civic infrastructure;
- monster lair around food/water/shelter;
- smuggler cave near a trade route/coast;
- ruined estate connected to former land ownership;
- buried/older construction exposed by later mining or erosion.

### Dungeon visibility

Different dungeons can be:

- obvious landmarks known by locals;
- visible but inaccessible until a route is found;
- hidden through environmental clue chains;
- discovered through rumors/maps;
- entered accidentally from another site;
- revealed only on a later revisit.

Not every dungeon should be a conspicuous black cave mouth beside the main road.

## Required multi-pass layout workflow

No major Rookvale Region layout becomes canonical after one draft.

### Pass 1 — reference decomposition

Before designing the Region, inspect a broad set of relevant games/maps and extract structural patterns rather than cosmetic resemblance.

Normal target: at least 10-20 useful reference maps/areas, including several 2D/top-down examples.

### Pass 2 — world-logic skeleton

Place first:

- water;
- terrain/elevation barriers;
- old/new roads;
- settlements;
- industries/resources;
- crossings;
- strategic chokepoints;
- major historical structures.

Do not start by scattering gameplay icons.

### Pass 3 — player route graph

Draw the movement graph separately from the art map.

Mark:

- obvious primary route;
- alternate routes;
- safe return paths;
- loops;
- shortcuts;
- dead ends;
- gates;
- future-return paths;
- dungeon entrances;
- fast-travel anchors.

Audit that the main route is readable without turning the entire Region linear.

### Pass 4 — discovery / landmark pass

Add visual pulls, rumors, optional landmarks, secrets, micro-sites, and later-return mysteries.

Check sight/readability from likely approach directions.

### Pass 5 — enemy ecology and encounter pass

Place enemies only after geography and human use are understandable.

Audit:

- ecology / faction logic;
- encounter variety;
- threat gradient;
- road safety;
- solo vs party pressure;
- excessive unavoidable fights;
- farming/exploit routes;
- proximity to checkpoints.

### Pass 6 — dungeon/content pass

Place/adjust dungeons, bosses, events, quest sites, and loot sources.

Verify that content is geographically and narratively justified and that one side of the Region is not accidentally empty.

### Pass 7 — navigation clarity pass

Test as if the player has never seen the map.

Questions:

- Can a new player identify the broad next direction?
- Can they return to town without memorizing dozens of identical screens?
- Are road hierarchy and landmarks sufficient?
- Do optional routes look optional rather than mistaken main routes?
- Are danger cues readable before unavoidable punishment?
- Are exact pins used where ambiguity is merely annoying?

### Pass 8 — curiosity/reward pass

Trace every meaningful detour.

Ask:

- why would I notice this?
- why would I go there?
- what do I get/learn/see?
- how hard is it to rejoin useful routes afterward?

Remove or repurpose low-value empty branches.

### Pass 9 — pacing and repetition pass

Audit encounter/destination spacing.

Avoid patterns such as:

`fight -> 20 sec walk -> fight -> 20 sec walk -> chest -> repeat`.

Mix quiet travel, environmental observation, small combat, landmark arrival, NPC/social space, danger spikes, and dungeon commitment.

### Pass 10 — external comparison and self-critique

Compare the completed draft again with several strong references and explicitly identify:

- where Rookvale is too linear;
- where it is too confusing;
- where it is too empty;
- where it is too dense/noisy;
- where encounter placement feels gamey;
- where dungeon locations feel arbitrary;
- where main-path communication depends too much on UI;
- where world logic is sacrificing gameplay clarity or vice versa.

Revise before locking.

## Naming direction added by user review

Rookvale should **not** overproduce transparent English fantasy compounds.

Names should often function as opaque proper nouns to a modern speaker, much like many real-world place names whose historical meaning is no longer obvious in everyday use.

Allowed naming sources include:

- old personal/family names that changed phonetically over time;
- older language words whose meaning is no longer transparent;
- borrowed names from previous populations;
- shortened or corrupted older settlement names;
- arbitrary explorer/settler names;
- names taken from an animal, object, event, owner, saint/hero, ship, landmark, or local story;
- occasional transparent descriptive names where they make historical/social sense.

The player does not need to be able to decompose every location into two English dictionary nouns.

## Locked quality bar

For future Rookvale map work:

- external research is mandatory before placement;
- several references must be compared, not one copied;
- 2D-specific references are mandatory alongside 3D open-world references;
- layout receives multiple explicit passes before locking;
- enemy placement follows geography/ecology/tactical role;
- dungeon placement follows location history/function;
- basic progression direction remains readable;
- optional discovery remains meaningfully less explicit;
- playtest/navigation evidence should eventually override elegant paper design when the two disagree.
