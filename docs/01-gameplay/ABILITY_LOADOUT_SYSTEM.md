# Ability Loadout System

**Status:** Core loadout architecture locked for prototype; exact unlock levels and per-class content counts remain tunable

Rookvale is a single-avatar RPG. The same persistent player character must support solo play, party roles, class identity, and meaningful build variety without becoming a collectible-party interface or a giant MMO hotbar.

## Mature combat loadout

A mature character uses the following layers:

- **8 normal active-skill slots**
- **1 Signature slot**
- **1 Reaction slot**
- **4 selectable passive slots**
- **1 innate class mechanic/passive**, always active and not slotted
- universal combat commands outside the loadout, such as basic attack, Defend, item access, and escape where allowed

This is the target architecture to prototype. Early progression may unlock some slots gradually for onboarding, but the full structure should become available before serious buildcraft begins.

## Normal active skills

The eight normal active slots are intentionally **not divided into fixed attack / defense / support quotas**.

A player may build a highly defensive, offensive, control-heavy, support-heavy, hybrid, or solo-oriented loadout as long as the chosen class provides those tools.

Class lineages should learn more normal active skills than can be equipped at once. The point of the slot limit is meaningful omission and preparation, not artificial starvation.

### Universal commands

The following normally do not consume normal skill slots:

- weapon/basic attack;
- Defend;
- items;
- escape where the encounter allows it;
- context/system actions.

A class mechanic may also expose its own control outside the eight slots when doing so is clearer than pretending it is an ordinary skill.

## Innate class mechanic

Every mature class has one primary innate class mechanic or passive identity.

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

Advanced classes normally evolve or reinterpret the ancestral mechanic rather than accumulating a separate always-on passive from every prior promotion.

## Selectable passives

A mature character equips **4 selectable class-bound passives**.

These passives are a major build layer and should usually alter decisions or interactions rather than only provide generic stat increases.

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
- mature classes should eventually offer more than one Signature candidate where practical so the slot can also express a build choice.

The word `Signature` is intentional: not every class fantasy should culminate in a giant damage nuke.

## Skill transformation: Techniques

Important active skills may unlock **Techniques**, mutually exclusive variants chosen outside combat.

Technique rules:

- a skill may have roughly 2-3 meaningful variants when that skill justifies them;
- only one Technique for that skill is active at a time;
- Techniques do not consume additional active slots;
- not every minor or utility skill requires Techniques;
- a Technique should change how or why the skill is used, not merely provide a small coefficient increase.

Useful transformation axes include:

- target pattern;
- front/back-row access;
- status application or consumption;
- resource generation versus spending;
- cooldown length versus impact;
- delayed versus immediate effect;
- damage versus protection/support hybridization;
- risk/reward;
- summon or mark behavior.

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

These are not per-class quotas. Rookvale does not force identical skill counts, Technique counts, Reaction counts, or Signature counts across all classes.

## Anti-bloat rules

Avoid:

- twelve-plus ordinary visible skill buttons by default;
- dozens of small +stat passive nodes masquerading as build diversity;
- one massive specialization tree attached to every single skill;
- mandatory attack/defense/support slot quotas;
- a universal `charge bar -> press ultimate` pattern for every class;
- excessive free actions or reactions that create a second hidden turn system;
- unrestricted cross-class passive/skill mixing that erases class identity;
- Technique choices that differ only by damage percentage.

## Research requirement for future ability production

Before a class kit is finalized, research must include both famous and lesser-known games. Each production pass should normally include:

- at least one turn-based/tactical reference;
- at least one deep class/build-system reference;
- at least one lesser-known or indie game with an unusual mechanic;
- additional references appropriate to that class fantasy.

Useful long-tail sources may include tactical indies, niche MMORPGs, build-heavy ARPGs, and games with unusual passive/reaction systems. Rookvale should keep expanding its mechanic vocabulary instead of repeatedly mining the same few famous titles.
