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

## 2026-10-16 — Research-first active/passive design

**Decision:** Active skills, passive traits, class mechanics, reactions, and skill transformations must be designed through broad external research rather than from a single reference game or internal intuition alone. Production-ready class kits should synthesize several distinct references, including turn-based examples, strong class/build systems from other RPG subgenres, and useful lesser-known or indie games when applicable. Exact skills, names, text, rotations, numbers, and distinctive kits must not be copied wholesale.

**Decision:** When adapting external mechanics, explicitly audit them against Rookvale's sequential Speed timeline, natural-turn cooldown ticking, bonus-action rules, front/back formation, multiplayer pacing, solo viability, and class-specific resources.

## 2026-10-16 — Mature ability-loadout architecture

**Decision:** Prototype a mature loadout with **8 normal active-skill slots**, **4 selectable passive slots**, **1 innate class mechanic/passive**, **1 dedicated Reaction slot**, and **1 separate Signature slot**. Universal commands such as basic attack, Defend, items, and escape do not consume the eight normal active slots.

**Decision:** The eight normal active slots are not divided into mandatory attack/defense/support quotas. A class may support offensive, defensive, control, support, hybrid, boss, or solo loadouts using the same slot structure.

**Decision:** Early progression may unlock some slots gradually for onboarding, but the mature structure should become available before serious buildcraft. Slot unlocking is not intended as a long-term grind wall.

## 2026-10-16 — Innate and selectable passives

**Decision:** Every mature class has one primary innate class mechanic/passive that does not consume a selectable passive slot. Advanced classes normally evolve, replace, or reinterpret the ancestral mechanic instead of stacking endless innate passives from every promotion.

**Decision:** A mature build equips four class-bound selectable passives. Major passive choices should normally change rules, resources, statuses, threat, rows, cooldown/timeline behavior, summons, or role interactions rather than consist mainly of generic stat increases.

## 2026-10-16 — Reactions

**Decision:** Prototype one dedicated Reaction slot for out-of-turn class responses such as Riposte, Intercept, reactive cleanse, emergency protection, or retaliation. Reactions are not natural full turns, do not tick normal full-turn cooldowns/durations, and do not recursively trigger further reactions by default. Exact reaction availability is class-dependent rather than symmetric across all classes.

## 2026-10-16 — Signature abilities

**Decision:** Use one separate **Signature** slot rather than forcing every class into the same universal ultimate-meter pattern. A Signature may be a burst attack, transformation, stance, summon, rescue, curse, defensive oath, row effect, or timeline intervention. It normally consumes the character's ordinary action and may be limited by cooldown, class resource, charges, battle conditions, or once-per-battle rules. There is no shared party ultimate gauge.

## 2026-10-16 — Skill transformation

**Decision:** Important active skills may use **Techniques**: normally 2-3 mutually exclusive meaningful variants selected outside combat. Techniques do not consume additional active slots and should change targeting, resource interaction, cooldown, status behavior, row access, timing, risk/reward, or role—not merely provide a slightly larger damage coefficient.

**Decision:** Rookvale does not plan a giant dedicated specialization tree for every active skill. Build depth comes from the combination of active loadout, Techniques on important skills, selectable passives, the innate class mechanic, weapons, Reaction, Signature, equipment, and class progression.

## 2026-10-15 — Platform order

**Decision:** Develop and visually validate the web version first while preserving future portability to Roblox and mobile.

## 2026-10-15 — Reference boundary

**Decision:** Hero of Aethric is a reference for the broad overworld exploration -> turn-based battle format. Other systems should be designed using broader external research rather than treating Hero of Aethric as the complete template.
