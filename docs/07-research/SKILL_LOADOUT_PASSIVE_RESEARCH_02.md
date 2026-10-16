# Skill Loadout, Passive, Signature, and Skill-Variation Research 02

**Status:** Research synthesis used to define the first Rookvale loadout architecture

## Research rule

Rookvale ability design must not over-index on famous AAA/MMO references. When a class, active skill, passive, reaction, status interaction, or skill transformation enters production, research should deliberately include lesser-known RPGs, indie tactical games, and deep build-crafting games when they contain a useful mechanic.

The goal is not to collect names. The goal is to widen the mechanic vocabulary and then rebuild useful principles around Rookvale's sequential Speed timeline, one-normal-action turns, turn cooldowns, front/back rows, threat, class resources, and multiplayer pacing.

## References reviewed for this pass

### WAKFU
- Up to 12 active spells and 6 passive spells can be equipped.
- Demonstrates that a single persistent MMORPG character can support a fairly broad loadout without relying on a collectible party roster.
- Useful upper-bound reference, but Rookvale should use fewer visible choices for cleaner mobile/Roblox UI and faster turns.

### Guild Wars 2
- Separates weapon-derived skills, selectable utility skills, an elite skill, and profession mechanics.
- Specializations provide fixed minor traits plus selected major traits and can materially alter profession mechanics.
- Strong reference for separating an innate class mechanic from optional build traits and for giving a powerful class-defining skill its own presentation.

### Last Epoch
- Uses five active skills but gives specialized skills their own transformation trees.
- Shows that low slot count can still produce build depth when each equipped skill can change substantially.
- Rookvale should borrow the principle of meaningful skill variants, not the production burden of a full large tree for every skill across an 80-100+ concept class bank.

### Grim Dawn
- Active skills live on the action bar, passive skills do not consume bar space, and attached modifiers can alter specific active skills.
- Useful reference for local skill modifiers plus global passive/build layers.

### Fell Seal: Arbiter's Mark
- Separates active abilities, passive abilities, and a dedicated counter ability.
- Main class contributes built-in passive identity while additional passives and a counter can be chosen.
- Strong reference for giving reactions/counters their own slot rather than treating every automatic trigger as an ordinary passive.

### Darkest Dungeon II
- Heroes can unlock roughly eleven combat skills but equip five.
- Paths change how existing skills behave, sometimes improving one use at the expense of another.
- Useful evidence that changing the role of existing skills can be more interesting than simply adding stronger versions.

### Chained Echoes
- Separates normal active/passive slots from class-granted active/passive slots.
- Useful reference for keeping class identity visible as its own build layer.

### Battle Chasers: Nightwar
- Basic actions can generate temporary Overcharge, stronger abilities spend resources, and characters have powerful Burst abilities.
- Perks alter active skills and resource behavior.
- Useful for generator/spender design and for powerful signature actions, but Rookvale should not use a shared party Burst meter.

### TROUBLESHOOTER: Abandoned Children
- Uses a large mastery-board system with categorized slots, costs, mastery-set interactions, and many conditional rule-changing effects.
- Demonstrates how deep passive composition can create huge build variety.
- Also demonstrates the danger of slot-category bloat and filler choices when categories are forced too rigidly.
- Rookvale should take the depth principle while keeping a much cleaner loadout.

### Siralim Ultimate
- Uses many highly distinct specialization perks that reshape battle rules and create unusual build identities.
- Useful long-tail reference for aggressively different passive mechanics, restrictions, and build fantasies.
- The game is party-collection based, so its roster structure is not transferable to Rookvale; only individual mechanic ideas are relevant.

### Stolen Realm
- Broad skill trees mix active and passive abilities across many fantasy themes.
- Useful for scouting unusual active/passive interactions and hybrid build concepts, not as a template for unrestricted cross-class mixing.

### Horizon's Gate
- Allows a small number of freely chosen passive slots on top of class/subclass abilities.
- Useful evidence that a limited passive selection can materially shape a character without needing a huge always-on passive board.

## Rookvale synthesis

### 1. Normal active-skill loadout

**Mature target: 8 normal active-skill slots.**

Reasoning:
- five is attractive for UI clarity but too restrictive for a single-avatar RPG where the same character must remain credible in solo play;
- twelve is proven viable in WAKFU but would create too much combat-menu density for Rookvale's cross-platform target;
- eight leaves room for offense, defense, utility, resource generation, CC, and role tools while still forcing meaningful omissions.

The eight slots are unrestricted by rigid categories. Rookvale should not force a player to equip exactly N attacks, N defenses, and N support skills.

Universal commands such as basic attack, Defend, items, and escape do not consume these eight slots.

Early-game slots may unlock gradually for onboarding, but the player should reach the mature eight-slot structure before build complexity becomes a major part of progression. Slot unlocking is an onboarding tool, not a long-term monetized or grind-heavy power gate.

### 2. Innate class mechanic / passive

Every mature class has **one innate class mechanic** that does not consume a passive slot.

This can be:
- a visible resource such as Resolve or Mana;
- a stack/mark rule;
- a summon rule;
- an HP-sacrifice rule;
- a threat/formation rule;
- a cooldown/timeline rule;
- another persistent mechanic.

Advanced classes normally evolve, replace, or reinterpret the ancestral mechanic rather than stacking endless innate passives from every ancestor.

### 3. Selectable passive loadout

**Mature target: 4 selectable class-bound passive slots.**

A mature class/lineage should normally offer substantially more than four viable passive choices so two players of the same class can diverge.

Passives should prioritize:
- resource-rule changes;
- conditional effects;
- active-skill interactions;
- status conversion/spread;
- threat/row behavior;
- summon behavior;
- cooldown/timeline manipulation;
- risk/reward changes;
- role conversion.

Small stat bonuses may exist as supporting progression but should not dominate the four major passive choices.

### 4. Reaction slot

Prototype **one dedicated Reaction slot** outside the eight normal active slots and four passive slots.

A Reaction is an automatic or prompted out-of-turn response such as:
- Riposte;
- Intercept;
- emergency barrier;
- retaliatory spell;
- reactive cleanse;
- dodge follow-up;
- ally-protection trigger.

Rules:
- a reaction is not a natural full turn;
- triggering it does not tick ordinary turn cooldowns or full-turn durations;
- reactions should have cooldowns, charges, once-per-cycle limits, or trigger restrictions where needed;
- reactions do not recursively trigger further reactions by default;
- classes are not required to have equally many reaction options.

This slot is inspired by Fell Seal's separate counter layer but adapted to Rookvale's bonus-action safeguards.

### 5. Signature slot instead of a universal 'ultimate nuke'

Use **one separate Signature slot** for mature advanced classes.

A Signature is a class-defining high-impact action. It is not required to be a giant damage attack. Depending on the class it may be:
- a burst attack;
- a transformation;
- a stance;
- a major summon;
- a party rescue;
- a field/row effect;
- a powerful curse;
- a timeline manipulation;
- a defensive oath.

Rules:
- the Signature normally consumes the character's ordinary action when used;
- it does not grant a free extra full turn unless explicitly designed to do so;
- it may be limited by a long turn cooldown, high class-resource cost, battle condition, charge, or once-per-battle rule;
- there is no universal shared party Ultimate gauge;
- mature classes should eventually have more than one Signature candidate so this slot can also support build choice.

### 6. Skill transformation: Techniques

Do **not** build a giant Last-Epoch-sized tree for every Rookvale skill. That would multiply content and balance cost across the planned class bank.

Instead use **Techniques**:
- important active skills may unlock 2-3 mutually exclusive meaningful variants;
- the player chooses one Technique for that skill outside combat;
- a Technique does not consume another normal active slot;
- not every minor skill needs Techniques;
- variants should change a decision, target pattern, resource interaction, cooldown, row access, status effect, risk, or party role rather than merely add +10% damage.

Examples of valid transformation dimensions:
- direct hit -> lower damage but applies a stack/status;
- single-target -> row pressure with lower potency;
- resource generator -> resource spender;
- long cooldown burst -> weaker but faster-cycling version;
- damage skill -> protection/utility hybrid;
- consume status -> preserve status but gain a different payoff.

### 7. Two layers of modification

Rookvale therefore has two distinct skill-modification layers:

1. **Technique** — local modification of one active skill.
2. **Selectable passive** — broader rule that may affect several skills, a resource, statuses, weapons, rows, or the class mechanic.

This provides depth without forcing every individual skill to carry a huge tree.

### 8. Target content breadth, not rigid quotas

Planning targets for a mature lineage:
- enough normal active skills that choosing only eight creates real tradeoffs;
- enough major passives that choosing four creates multiple coherent builds;
- several reaction candidates when the class fantasy supports reactions;
- more than one Signature candidate where practical;
- Techniques concentrated on important/core skills.

These are content targets, not symmetry requirements. A class may have more or fewer options if its design justifies it.

## Anti-bloat rules

- Do not force every class to have the same number of reaction skills, Techniques, or Signature variants.
- Do not create a skill variant whose only purpose is a slightly larger coefficient.
- Do not make the passive page a wall of generic +stat nodes.
- Do not make every class use the same `build gauge -> press ultimate` loop.
- Do not create a second hidden action bar through excessive free actions.
- Do not let skill customization erase class identity by importing unrelated class abilities.

## Production research rule for future abilities

Before finalizing a mature class kit, intentionally sample both mainstream and long-tail references. A normal research pass should include:

- at least one close turn-based/tactical analogue;
- at least one strong class/build game;
- at least one lesser-known or indie reference with an unusual mechanic;
- additional references when the class fantasy has rich precedents.

The research pool should continue expanding over time rather than repeatedly mining the same famous games.
