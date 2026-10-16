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
| Character progression & rewards | [`01-gameplay/PROGRESSION_REWARDS.md`](01-gameplay/PROGRESSION_REWARDS.md) | Core progression philosophy locked |
| Advancement content | [`01-gameplay/ADVANCEMENT_CONTENT.md`](01-gameplay/ADVANCEMENT_CONTENT.md) | Core advancement philosophy locked |
| Equipment foundation | [`01-gameplay/EQUIPMENT_FOUNDATION.md`](01-gameplay/EQUIPMENT_FOUNDATION.md) | Core equipment philosophy locked |
| Equipment stats & affixes | [`01-gameplay/EQUIPMENT_STATS_AFFIXES.md`](01-gameplay/EQUIPMENT_STATS_AFFIXES.md) | Core architecture locked |
| Equipment crafting & refinement | [`01-gameplay/EQUIPMENT_CRAFTING_REFINEMENT.md`](01-gameplay/EQUIPMENT_CRAFTING_REFINEMENT.md) | Core philosophy locked |
| Multiplayer & parties | [`01-gameplay/MULTIPLAYER.md`](01-gameplay/MULTIPLAYER.md) | Core party/loot/trade direction locked |
| Multiplayer loot & trade | [`01-gameplay/MULTIPLAYER_LOOT_TRADE.md`](01-gameplay/MULTIPLAYER_LOOT_TRADE.md) | Core rules locked |
| Death / revival / failure / retreat | [`01-gameplay/DEATH_FAILURE_RETREAT.md`](01-gameplay/DEATH_FAILURE_RETREAT.md) | Core philosophy locked |
| World structure | [`02-world/WORLD_STRUCTURE.md`](02-world/WORLD_STRUCTURE.md) | Core world model locked |
| Detailed world exploration rules | [`01-gameplay/WORLD_STRUCTURE_EXPLORATION.md`](01-gameplay/WORLD_STRUCTURE_EXPLORATION.md) | Core exploration philosophy locked |
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

The immediate design sequence is now:

1. Design the **actual world geography**: continent/world count, launch Region count, Region themes, cultures, biomes, Tier ranges, and connections.
2. Define the **starting Region and settlement** strongly enough to support the first playable vertical slice.
3. Connect world geography to content density: dungeons, bosses, settlements, secrets, advancement content, equipment sources, and multiplayer activities.
4. Continue deterministic combat implementation/simulation using the already locked Natural-Turn/timeline/status/Break/Threat rules rather than reopening core combat structure without evidence.
5. After world/content structure is credible, specify quests, world events, gathering/crafting-life content, economy, and endgame repeat structures against that actual geography.

The next useful world-design review point is a concrete Region roster and connection map rather than another abstract discussion of whether Rookvale should be open-world at all.
