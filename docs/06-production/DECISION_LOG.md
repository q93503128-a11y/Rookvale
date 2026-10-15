# Decision Log

This file records major project decisions so later work can distinguish an actual decision from an old idea.

## 2026-10-15 — Project identity

**Decision:** The project title is **Rookvale**.

## 2026-10-15 — Core format

**Decision:** Rookvale is a 2D pixel open-world RPG with turn-based combat.

## 2026-10-15 — World model

**Decision:** Exploration uses an in-game handcrafted world. It does not use GPS.

## 2026-10-15 — Multiplayer

**Decision:** Multiplayer and party play are foundational design assumptions. Solo play should also remain viable.

## 2026-10-15 — Character progression

**Decision:** The game should support varied party roles and branching class advancement.

## 2026-10-15 — Single-avatar class model

**Decision:** Rookvale is not a collectible-party RPG. Each human player primarily develops one persistent combat character, so long-term build variety comes from class lineage, skill loadout, equipment, stats, passives, weapons, and class resources.

## 2026-10-15 — Class-bound skills

**Decision:** Active combat skills are class/lineage-bound by default. Related descendants may inherit ancestral skills, but unrelated classes do not freely combine a universal best-of-every-class skill bar.

## 2026-10-15 — Asymmetric class trees

**Decision:** Class trees do not follow a fixed branch count or fixed depth. A lineage branches only when there is a meaningful new fantasy or play pattern. Linear promotions are allowed, but major promotions must add or reshape mechanics rather than only replace skills with stronger copies.

## 2026-10-15 — Broad design, narrow implementation

**Decision:** Maintain a very large long-term class design bank, approximately 80-100+ advanced concepts across roughly 11 broad origin disciplines, but implement only a small representative subset first. Large-roster design is not a promise that every concept ships.

## 2026-10-15 — First class implementation subset

**Decision:** The first vertical slice starts with four origin disciplines and two immediate branches each:

- Armsman -> Knight / Duelist
- Ranger -> Hunter / Marksman
- Arcanist -> Pyromancer / Cryomancer
- Acolyte -> Priest / Oracle

The symmetrical `2 branches each` shape is only a test-scope convenience and is explicitly **not** a global class-tree rule.

## 2026-10-15 — Weapon ancestry

**Decision:** Origin disciplines are anchored to broad related weapon pools, not exactly one weapon. Descendants normally retain ancestral weapon compatibility, may specialize in part of the pool, and may unlock additional/signature weapon types where justified. The equipment taxonomy must remain much smaller than the class roster.

## 2026-10-15 — Class mechanics and resources

**Decision:** Cooldowns coexist with class-specific resources, stacks, marks, summons, HP-sacrifice mechanics, or other class rules where useful. There is no requirement for universal MP or for every class to have a visible resource bar. A class resource must remain functional in low-enemy-count and single-boss encounters; kill-based triggers may accelerate a resource but should not normally be its only engine.

## 2026-10-15 — Passives and status identity

**Decision:** Innate class passives/mechanics are a major identity layer. Major passives should usually change rules or decisions rather than only provide small generic stat bonuses. CC, buffs, debuffs, threat, front/back rows, timeline manipulation, cooldown changes, summons, and status interactions are all valid class-identity axes.

## 2026-10-15 — Platform order

**Decision:** Develop and visually validate the web version first while preserving future portability to Roblox and mobile.

## 2026-10-15 — Reference boundary

**Decision:** Hero of Aethric is a reference for the broad overworld exploration -> turn-based battle format. Other systems should be designed using broader external research rather than treating Hero of Aethric as the complete template.
