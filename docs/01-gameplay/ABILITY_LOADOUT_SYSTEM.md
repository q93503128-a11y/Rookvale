# Ability Loadout System

**Status:** Core loadout architecture locked for prototype; exact unlock levels and per-class content counts remain tunable

Rookvale is a single-avatar RPG. The same persistent player character must support solo play, party roles, class identity, and meaningful build variety without becoming a collectible-party interface or a giant MMO hotbar.

## Mature combat loadout

A mature character uses the following layers:

- **8 normal active-skill slots**
- **1 Signature slot**
- **1 Reaction slot**
- **4 selectable passive slots**
- **1 innate class mechanic/passive package**, always active and not slotted
- universal combat commands outside the loadout, such as basic attack, Defend, item access, and escape where allowed

This is the target architecture to prototype. The numbers are system targets, not a requirement that every class contain exactly the same amount of content.

## Progressive onboarding

Rookvale should not expose the full mature build screen immediately.

Prototype progression target:

1. **Origin / early play**
   - around 4 normal active slots;
   - universal commands;
   - the class's basic innate mechanic is introduced early.
2. **Developing class / first meaningful advancement**
   - expand toward 6 normal active slots;
   - begin selectable passive choices;
   - introduce Reaction and/or Signature when the class fantasy can support them clearly.
3. **Mature buildcraft**
   - 8 normal active slots;
   - 4 selectable passives;
   - 1 Reaction slot;
   - 1 Signature slot;
   - Techniques on important skills.

Exact levels and unlock moments remain open. The point is to teach layers gradually while reaching the full build system well before endgame.

## Normal active skills

The eight normal active slots are intentionally **not divided into fixed attack / defense / support quotas**.

A player may build a highly defensive, offensive, control-heavy, support-heavy, hybrid, or solo-oriented loadout as long as the chosen class provides those tools.

Class lineages should learn more normal active skills than can be equipped at once. The point of the slot limit is meaningful omission and preparation, not artificial starvation.

### Mature lineage content target

A mature class lineage should usually have access to roughly **12-16 meaningful normal active choices across its ancestry and current specialization**, with 8 equipped at once.

This range is a production target, not a quota. A class with 11 excellent, mechanically distinct actives is better than one padded to 16 with filler. Likewise, an unusually complex class may justify more.

Inherited ancestral actives count toward this pool; every promotion does not need to create an entirely new 12-16-skill kit.

### Universal commands

The following normally do not consume normal skill slots:

- weapon/basic attack;
- Defend;
- items;
- escape where the encounter allows it;
- context/system actions.

A class mechanic may also expose its own control outside the eight slots when doing so is clearer than pretending it is an ordinary skill.

## Innate class mechanic

Every mature class has one primary **innate class-mechanic package** that is always active.

This is not required to be literally one sentence or one passive icon. It may be a compact linked rule set that defines the class's core loop.

Examples of mechanic types:

- Resolve / Rage / Mana or another resource;
- marks or stacks;
- summons or companion rules;
- HP sacrifice;
- threat / interception behavior;
- front/back-row rules;
- cooldown / Speed / timeline manipulation;
- status conversion;
- stance or transformation logic.

Advanced classes normally evolve, redirect, or reinterpret the ancestral mechanic rather than accumulating a permanent always-on passive from every prior promotion.

The innate mechanic should be recognizable even when two players equip completely different active and passive loadouts.

## Selectable passives

A mature character equips **4 selectable class-bound passives**.

Four is the prototype target because it is large enough to create combinations but small enough that individual choices stay readable. Octopath-style four-support-skill builds and Fell Seal's four-total-passive structure both demonstrate that a small count can still create meaningful identity, while deeper systems such as TROUBLESHOOTER show how quickly passive composition can become difficult to parse when every interaction becomes another board slot.

Rookvale initially uses **equal passive slots** rather than Bravely Default-style variable slot costs. If one passive is too strong for one slot, first redesign or rebalance the passive instead of immediately adding a weighted-cost metagame.

Strong passive themes include:

- changing resource generation or spending;
- modifying several related active skills;
- changing buff/debuff or CC interactions;
- altering threat, rows, guarding, or interception;
- changing cooldown or timeline behavior;
- changing summon rules;
- introducing risk/reward conditions;
- converting one role into a hybrid form;
- changing how a weapon family interacts with the class.

Flat statistical bonuses may exist as secondary progression, but they should not crowd out the four major passive choices.

### Mature passive content target

A mature lineage should usually expose roughly **7-10 serious selectable passive choices** across ancestry and specialization so equipping four requires real tradeoffs.

Again, this is not a symmetry rule. Passive quality and distinctness matter more than count.

## Reaction slot

Rookvale prototypes **one dedicated Reaction slot**.

A Reaction is an out-of-turn response such as Riposte, Intercept, emergency protection, reactive cleanse, retaliation, or a triggered dodge follow-up.

Reaction rules:

- reactions are not natural full turns;
- reactions do not advance normal turn cooldowns or natural-turn durations;
- reactions cannot recursively trigger additional reactions by default;
- reactions may use their own cooldowns, charges, per-cycle limits, or conditions;
- not every class needs the same number or style of Reaction options;
- leaving the slot empty is allowed if a class/build has no desired Reaction.

Reaction design must remain readable in multiplayer and must not create long automatic chains that make players watch the game play itself.

### Reaction content target

A mature class that meaningfully uses reactions should normally have around **2-4 Reaction candidates** over its lineage, with one equipped.

A class whose fantasy does not benefit from reaction play should not receive filler reactions merely to hit the range.

## Signature slot

Rookvale uses **one Signature slot** rather than forcing every class into the same traditional ultimate-meter design.

A Signature is a high-impact, class-defining ability. It can be offensive, defensive, supportive, summoning, transformational, positional, or timeline-based.

Examples include:

- a major attack;
- a transformation or stance;
- an emergency party rescue;
- a major summon;
- a defensive oath;
- a battlefield curse;
- a row-wide field effect;
- a powerful timeline intervention.

Signature rules:

- using a Signature normally consumes the character's ordinary action for that turn;
- it does not inherently grant a bonus full turn;
- limitation may come from a long turn cooldown, high class-resource cost, charge, condition, or once-per-battle rule;
- there is **no shared party ultimate resource**;
- a Signature does not have to be a damage nuke or even resemble a conventional 'ultimate';
- mature classes should eventually offer more than one Signature candidate where practical so the slot can also express a build choice.

### Signature content target

A newly advanced class may begin with **1 Signature**. A mature specialization should normally aim for **2-3 viable Signature candidates** when its design supports them.

The word `Signature` is intentional: not every class fantasy should culminate in a giant damage nuke.

## Skill transformation: Techniques

Important active skills may unlock **Techniques**, mutually exclusive variants chosen outside combat.

Technique rules:

- a Technique modifies one existing skill rather than occupying another action-bar slot;
- a skill may have roughly 2-3 meaningful variants when that skill justifies them;
- only one Technique for that skill is active at a time;
- not every minor or utility skill requires Techniques;
- a Technique should change how or why the skill is used, not merely provide a small coefficient increase;
- changing Techniques happens outside combat as part of loadout preparation.

Useful transformation axes include:

- target pattern;
- front/back-row access;
- status application or consumption;
- resource generation versus spending;
- cooldown length versus impact;
- delayed versus immediate effect;
- damage versus protection/support hybridization;
- risk/reward;
- summon or mark behavior;
- interaction with weapon family or class passive.

### Technique content target

Do **not** attach a giant skill tree to every active. For a mature class, roughly **3-5 build-defining active skills** may be strong candidates for Techniques, normally with 2-3 meaningful variants each.

Some classes may use fewer Techniques because their diversity lives in stances, summons, passives, weapons, or resources. Others may justify more. The mechanic follows the class, not a global quota.

Technique unlock method — class mastery, level progression, quests, exploration, or another system — remains open and should be researched separately before final progression design.

## Passive + Technique interaction

Rookvale deliberately separates two modification layers:

1. **Technique:** modifies one specific active skill.
2. **Selectable passive:** modifies broader class rules, skill groups, statuses, resources, rows, weapons, or the innate mechanic.

A class may also have a Signature or Reaction that interacts with either layer.

This provides meaningful build depth without requiring a giant dedicated skill tree for every active ability in a very large class roster.

## Weapon interaction

Weapons should influence class play without replacing the class skill system.

A weapon family may:

- enable a skill;
- change a skill's reach or legal rows;
- interact with a Technique;
- activate a class passive;
- unlock an advanced class's signature interaction.

Do not create a full unique copy of every class skill for every compatible weapon. Use weapon-specific transformations only when they create a meaningful gameplay distinction.

## Loadout changes

Loadouts are changed outside combat.

The game should support saved presets for common contexts such as:

- solo exploration;
- party play;
- boss encounters;
- farming / repeatable content;
- experimental build.

Exact preset count and unlock UX can be decided with the UI system, but switching between already-saved valid presets should not require tedious manual re-equipping.

## Content targets, not symmetry rules

A mature lineage should normally provide enough choices that:

- eight active slots force real tradeoffs;
- four passive slots support several coherent builds;
- Reaction choice matters when that class supports reactions;
- Signature choice matters when multiple options exist;
- core active skills can be reshaped with Techniques.

Current planning targets are therefore approximately:

- 12-16 normal active choices across a mature lineage;
- 7-10 selectable passive choices;
- 2-4 Reactions for reaction-oriented classes;
- 2-3 Signatures for mature classes when justified;
- Techniques on roughly 3-5 important active skills.

These numbers are **not per-class quotas**. Rookvale does not force identical skill counts, Technique counts, Reaction counts, Signature counts, or passive counts across all classes.

## Anti-bloat rules

Avoid:

- twelve-plus ordinary visible skill buttons by default;
- dozens of small +stat passive nodes masquerading as build diversity;
- one massive specialization tree attached to every single skill;
- mandatory attack/defense/support slot quotas;
- a universal `charge bar -> press ultimate` pattern for every class;
- excessive free actions or reactions that create a second hidden turn system;
- unrestricted cross-class passive/skill mixing that erases class identity;
- Technique choices that differ only by damage percentage;
- forcing every class to use every loadout layer equally strongly;
- padding a class with filler abilities just to meet a target count.

## Research requirement for future ability production

Before a class kit is finalized, research must include both famous and lesser-known games. Follow `docs/07-research/RESEARCH_POLICY.md`.

For production class kits, normally:

- perform a broad discovery survey across roughly 10-20 possible external references or mechanic systems;
- retain roughly 6-10 references that contributed meaningful lessons;
- include multiple lesser-known / indie / older / non-obvious games where useful;
- include turn-based/tactical references and deep class/build-system references;
- inspect active, passive, reaction, resource, Signature-like, and skill-transformation mechanics separately;
- search for bad or degenerate implementations as well as good ones.

These are research-quality targets, not citation quotas. Rookvale should keep expanding its mechanic vocabulary instead of repeatedly mining the same famous franchises.
