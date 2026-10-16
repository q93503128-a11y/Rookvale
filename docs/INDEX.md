# Rookvale Design Index

This directory is the canonical design source for Rookvale. The goal is to keep decisions separated by domain so the project can grow without turning one giant GDD into an unmaintainable document.

## Document rules

- Record only agreed decisions as **Locked**.
- Mark proposals as **Draft** and unresolved points as **Open**.
- Do not silently turn reference-game behavior into a Rookvale requirement.
- A reference may inspire a specific solution, but Rookvale should combine multiple references rather than copy one game wholesale.
- If implementation and design disagree, update the relevant design document or explicitly record the deviation in the decision log.
- Cross-platform constraints must be considered before a design becomes Locked.

## Canonical map

| Area | Document | Status |
| --- | --- | --- |
| Product identity | [`00-product/VISION.md`](00-product/VISION.md) | Draft |
| Core gameplay loop | [`01-gameplay/CORE_LOOP.md`](01-gameplay/CORE_LOOP.md) | Draft |
| Turn-based combat | [`01-gameplay/COMBAT.md`](01-gameplay/COMBAT.md) | Core locked / prototype specified |
| Combat vocabulary & duration | [`01-gameplay/COMBAT_VOCABULARY.md`](01-gameplay/COMBAT_VOCABULARY.md) | Prototype specified |
| Combat numeric skeleton | [`01-gameplay/PROTOTYPE_NUMBERS.md`](01-gameplay/PROTOTYPE_NUMBERS.md) | Draft implementation baseline |
| First combat enemy set | [`01-gameplay/PROTOTYPE_ENEMIES.md`](01-gameplay/PROTOTYPE_ENEMIES.md) | Draft implementation target |
| Classes & progression | [`01-gameplay/CLASSES_PROGRESSION.md`](01-gameplay/CLASSES_PROGRESSION.md) | Core direction locked / content expanding |
| Ability loadout | [`01-gameplay/ABILITY_LOADOUT_SYSTEM.md`](01-gameplay/ABILITY_LOADOUT_SYSTEM.md) | Core architecture locked |
| First eight class kits | [`01-gameplay/classes/`](01-gameplay/classes/) | Draft for prototype |
| Multiplayer & parties | [`01-gameplay/MULTIPLAYER.md`](01-gameplay/MULTIPLAYER.md) | Draft / core party assumptions set |
| World structure | [`02-world/WORLD_STRUCTURE.md`](02-world/WORLD_STRUCTURE.md) | Draft |
| Content systems | [`03-content/CONTENT_SYSTEMS.md`](03-content/CONTENT_SYSTEMS.md) | Open |
| Art direction | [`04-art-ux/ART_DIRECTION.md`](04-art-ux/ART_DIRECTION.md) | Draft |
| UI / UX | [`04-art-ux/UI_UX.md`](04-art-ux/UI_UX.md) | Open |
| Platform architecture | [`05-technical/PLATFORM_ARCHITECTURE.md`](05-technical/PLATFORM_ARCHITECTURE.md) | Draft |
| First vertical slice | [`06-production/VERTICAL_SLICE.md`](06-production/VERTICAL_SLICE.md) | Scope mostly defined |
| Decision history | [`06-production/DECISION_LOG.md`](06-production/DECISION_LOG.md) | Active |
| External references | [`07-research/REFERENCE_MATRIX.md`](07-research/REFERENCE_MATRIX.md) | Active |
| Combat/status research | [`07-research/COMBAT_STATUS_PROTOTYPE_RESEARCH_03.md`](07-research/COMBAT_STATUS_PROTOTYPE_RESEARCH_03.md) | Active research record |
| Combat prototype cross-check | [`07-research/FIRST_COMBAT_PROTOTYPE_CROSSCHECK_02.md`](07-research/FIRST_COMBAT_PROTOTYPE_CROSSCHECK_02.md) | Audit |

## Current high-value next work

The immediate design-to-implementation sequence is now:

1. Build a deterministic combat simulation/core around Natural Turns, Timeline Units, cooldowns, four duration clocks, statuses, Break, Threat, rows, Guard/Intercept, and the first numeric formulas.
2. Implement the minimal representative first-eight class kits identified in the existing class cross-check rather than every learned skill at once.
3. Implement the prototype normal enemies, Elite, and Black Banner Captain test encounter as a mechanical harness; names/lore remain replaceable.
4. Instrument combat telemetry before attempting serious balance: Natural Turns, damage/healing/prevention, target distribution, Break/control frequency, resource flow, TTK, and party-size scaling.
5. Only after the deterministic rules survive simulation should the web combat UI/animation layer become the main source of balance feedback.
6. In parallel/after the combat core is credible, continue world/vertical-slice work: starting settlement, exploration area, dungeon/special area, rewards/equipment, NPC/quest content, and early multiplayer validation.

The next useful user review point is playable/simulated evidence rather than another abstract combat-rule round, unless implementation reveals a genuine design fork.
