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

**Decision:** Production class research should use a broad discovery pass rather than only checking a few famous games. As a normal quality target, inspect roughly **10-20 candidate games/classes/mechanic systems**, then retain roughly **6-10 genuinely useful references** for synthesis. Include multiple lesser-known, indie, older, regional, or otherwise non-obvious sources when useful. These are quality targets, not quotas.

## 2026-10-16 — Mature ability-loadout architecture

**Decision:** Prototype a mature loadout with **8 normal active-skill slots**, **4 selectable passive slots**, **1 innate class mechanic/passive package**, **1 dedicated Reaction slot**, and **1 separate Signature slot**. Universal commands such as basic attack, Defend, items, and escape do not consume the eight normal active slots.

**Decision:** The eight normal active slots are not divided into mandatory attack/defense/support quotas. A class may support offensive, defensive, control, support, hybrid, boss, or solo loadouts using the same slot structure.

**Decision:** Use progressive onboarding rather than exposing the entire build screen immediately. Prototype direction is approximately **4 -> 6 -> 8 normal active slots** as the character develops, while passive, Reaction, Signature, and Technique layers are introduced before serious buildcraft. Exact unlock levels remain tunable.

## 2026-10-16 — Innate and selectable passives

**Decision:** Every mature class has one primary innate class-mechanic/passive package that does not consume a selectable passive slot. This may be a linked core rule set rather than literally one effect. Advanced classes normally evolve, replace, or reinterpret the ancestral mechanic instead of stacking endless innate passives from every promotion.

**Decision:** A mature build equips four class-bound selectable passives. Major passive choices should normally change rules, resources, statuses, threat, rows, cooldown/timeline behavior, summons, or role interactions rather than consist mainly of generic stat increases.

**Decision:** Prototype equal passive slots rather than weighted passive costs. If a passive is too strong for one slot, first redesign or rebalance it instead of immediately adding a second passive-cost economy.

## 2026-10-16 — Reactions

**Decision:** Prototype one dedicated Reaction slot for out-of-turn class responses such as Riposte, Intercept, reactive cleanse, emergency protection, or retaliation. Reactions are not natural full turns, do not tick normal full-turn cooldowns/durations, and do not recursively trigger further reactions by default. Exact reaction availability is class-dependent rather than symmetric across all classes.

## 2026-10-16 — Signature abilities

**Decision:** Use one separate **Signature** slot rather than forcing every class into the same universal ultimate-meter pattern. A Signature may be a burst attack, transformation, stance, summon, rescue, curse, defensive oath, row effect, or timeline intervention. It normally consumes the character's ordinary action and may be limited by cooldown, class resource, charges, battle conditions, or once-per-battle rules. There is no shared party ultimate gauge.

**Decision:** A newly advanced class may initially have one Signature candidate. Mature classes should generally aim for multiple viable Signature choices when the design genuinely supports them; do not create filler just to make counts symmetrical.

## 2026-10-16 — Skill transformation

**Decision:** Important active skills may use **Techniques**: normally 2-3 mutually exclusive meaningful variants selected outside combat. Techniques do not consume additional active slots and should change targeting, resource interaction, cooldown, status behavior, row access, timing, risk/reward, weapon interaction, or role—not merely provide a slightly larger damage coefficient.

**Decision:** Rookvale does not plan a giant dedicated specialization tree for every active skill. Build depth comes from the combination of active loadout, Techniques on important skills, selectable passives, the innate class mechanic, weapons, Reaction, Signature, equipment, and class progression.

**Decision:** Current mature-lineage content targets are roughly **12-16 normal active choices**, **7-10 selectable passive choices**, **2-4 Reaction candidates for reaction-oriented classes**, **2-3 Signature candidates when justified**, and Techniques on roughly **3-5 important active skills**. These are production targets, not quotas or symmetry rules.

## 2026-10-15 — Platform order

**Decision:** Develop and visually validate the web version first while preserving future portability to Roblox and mobile.

## 2026-10-15 — Reference boundary

**Decision:** Hero of Aethric is a reference for the broad overworld exploration -> turn-based battle format. Other systems should be designed using broader external research rather than treating Hero of Aethric as the complete template.

## 2026-10-16 — Combat temporal vocabulary

**Decision:** Treat a Speed-earned full action opportunity as a **Natural Turn**. Bonus/Free Actions and Reactions are not Natural Turns and do not, by default, tick ordinary cooldowns, Natural-Turn durations, DoT/HoT ticks, or natural-turn resource recovery. Reactions do not recursively trigger additional Reactions by default.

**Decision:** Prototype continuous Timeline Units with a reciprocal Speed model. The first implementation uses `StandardDelayTU = 10000 / EffectiveSpeed`, with action-delay and bounded timing modifiers layered on top. The constant, long-term Speed progression, and final caps remain tunable; the continuous next-action model is the important decision.

**Decision:** Separate persistent **Haste/Slow** from one-shot **Advance/Delay**. Haste/Slow change how future Natural Turns are scheduled; Advance/Delay move an already-scheduled next action. First-slice effects cannot grant an immediate unrestricted full Natural Turn.

## 2026-10-16 — Status duration clocks

**Decision:** Do not force every timed effect into one universal turn duration. Every timed effect declares one of four clocks: **Target Natural Turns**, **Until Source Next Natural Turn**, **Eligible Event Charges**, or **Timeline Units**.

**Decision:** Bonus/Free Actions and Reactions do not advance Target-Natural-Turn or source-Natural-Turn duration clocks by default. A hard-controlled unit still reaches Natural-Turn start/end boundaries so its duration cannot freeze forever merely because its action was denied.

## 2026-10-16 — Status identity and boss control

**Decision:** Differently named statuses must create different decisions. `Stun`, `Freeze`, `Sleep`, `Break`, and `Delay` are not interchangeable one-turn skips; `Burn`, `Bleed`, and `Poison` are not merely recolored DoTs; `Mark`, `Prey`, and `Exposed` are not interchangeable damage-amplification tags.

**Decision:** Prototype `Stun` primarily as an interrupt/bounded shove, `Freeze` as thresholded stored action denial on ordinary enemies, and `Break` as a posture threshold that can cancel only explicitly Breakable preparation while also creating bounded Delay and an Exposed payoff window.

**Decision:** Boss control uses **conversion + temporary repeat resistance**, not blanket immunity. Hard control against bosses normally converts into bounded Break, Delay, vulnerability/setup, or eligible telegraph interruption. Repeating the same hard-control family becomes temporarily less efficient, and repeated boss Breaks within a phase require increasing Break pressure.

## 2026-10-16 — Mark, Prey, Exposed and protection vocabulary

**Decision:** `Exposed` is the shared short vulnerability state. A generic `Mark` is a source-owned setup tag with no automatic universal party damage bonus. `Prey` is Hunter-specific coordination and is not removed by an ordinary generic Cleanse by default.

**Decision:** `Guard` is proactive prepared redirection of eligible direct attacks. `Intercept` is a bounded out-of-turn Reaction. Area/row attacks and explicit Unredirectable/scripted attacks are not automatically swallowed by either mechanic.

## 2026-10-16 — Threat model

**Decision:** Threat is stored **per enemy, per player character** rather than as one global aggro value. Damage, effective healing/barriers, protection actions, and explicit threat skills can contribute. Enemy-specific Threat decays over time. Front/back row, Knight identity, temporary Taunt/Challenge, and enemy AI preferences modify target score rather than making target selection absolute.

**Decision:** Taunt/Threat does not override Area attacks, Unredirectable/scripted mechanics, or explicit enemy identities such as Back-row hunters. The tank should concentrate risk, not make allies untargetable.

## 2026-10-16 — First numeric combat skeleton

**Decision:** Use one compact first-prototype `Power` stat and one `Defense` stat with different skill coefficients for damage, healing, and barriers. Do not split physical attack, magic attack, healing power, physical defense, magical defense, universal Accuracy/Evasion, and Status Hit/Resistance into separate baseline stats before the combat loop itself has been tested.

**Decision:** Prototype deterministic legal hits and mostly deterministic soft-status application. Explicit states may reduce effectiveness or create dodge/block behavior, but the first combat test should not be dominated by opaque miss/status-chance RNG.

**Decision:** Prototype direct mitigation with `100 / (100 + EffectiveDefense)`, no random damage variance, capped ordinary Barrier stacking, and visible soft-status resistance tiers. Exact coefficients and class base stats are Draft balance values rather than long-term production locks.

## 2026-10-16 — First Break and party-scale baselines

**Decision:** The first prototype uses a visible Break Gauge, bounded Break values per skill, partial Break recovery after successful enemy Natural Turns, Exposed after Break, and escalating boss Break maximums after repeated Break Events in the same phase. Exact numeric values remain Draft.

**Decision:** First boss party scaling is intentionally sublinear in HP and adds composition/mechanic pressure for larger parties. Four-player difficulty must not be solved by simply multiplying boss HP by four. Exact scaling multipliers remain Draft until telemetry exists.

## 2026-10-16 — First combat enemy harness

**Decision:** The first deterministic combat test uses a role-complete enemy ladder: baseline melee, Back-row attacker, defensive Guard/Barrier unit, fast positional unit, status user, healer/support, mixed-pressure Elite, and a multi-phase Boss.

**Decision:** The first boss must exercise Threat, Guard/Intercept, Front/Back rows, Break, Burn, Chill/Freeze conversion, Cleanse/Dispel, Barrier/healing, intent prediction, Mark/Prey, companion cadence, Reactions, and Signature windows. It must include tactical state changes and Breakable telegraphs rather than function as a pure HP sponge.

**Decision:** Enemy names, faction identity, lore, exact stats, exact AI weights, rewards, and final art are not locked by this mechanical harness.

## 2026-10-16 — Combat implementation order

**Decision:** The next high-value step is a deterministic combat core/simulator with telemetry before serious visual balancing. Implement Natural Turns, Timeline Units, cooldowns, duration clocks, statuses, Break, Threat, rows, Guard/Intercept, representative first-eight abilities, the enemy ladder, and combat logging first; use the results to tune before expanding the full class ability pool or polishing every combat presentation detail.
