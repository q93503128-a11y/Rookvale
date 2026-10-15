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
| Turn-based combat | [`01-gameplay/COMBAT.md`](01-gameplay/COMBAT.md) | Open |
| Classes & progression | [`01-gameplay/CLASSES_PROGRESSION.md`](01-gameplay/CLASSES_PROGRESSION.md) | Open |
| Multiplayer & parties | [`01-gameplay/MULTIPLAYER.md`](01-gameplay/MULTIPLAYER.md) | Draft |
| World structure | [`02-world/WORLD_STRUCTURE.md`](02-world/WORLD_STRUCTURE.md) | Draft |
| Content systems | [`03-content/CONTENT_SYSTEMS.md`](03-content/CONTENT_SYSTEMS.md) | Open |
| Art direction | [`04-art-ux/ART_DIRECTION.md`](04-art-ux/ART_DIRECTION.md) | Draft |
| UI / UX | [`04-art-ux/UI_UX.md`](04-art-ux/UI_UX.md) | Open |
| Platform architecture | [`05-technical/PLATFORM_ARCHITECTURE.md`](05-technical/PLATFORM_ARCHITECTURE.md) | Draft |
| First vertical slice | [`06-production/VERTICAL_SLICE.md`](06-production/VERTICAL_SLICE.md) | Open |
| Decision history | [`06-production/DECISION_LOG.md`](06-production/DECISION_LOG.md) | Active |
| External references | [`07-research/REFERENCE_MATRIX.md`](07-research/REFERENCE_MATRIX.md) | Active |

## Current design questions

The next high-value decisions are:

1. What makes Rookvale's turn-based combat distinct?
2. How many players form a standard party, and how does co-op battle flow work?
3. What is the initial class model and how do branching advancements work?
4. How is the open world partitioned into regions, towns, dungeons, and level bands?
5. Which systems belong in the first playable vertical slice versus later production?
