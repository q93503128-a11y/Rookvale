# Classes and Progression

**Status:** Core identity locked; exact class roster, tree depth, and slot counts open

## Player-character model

Rookvale is **not a party-collection game**. Each human player primarily controls and develops **one persistent player character**.

- Multiplayer parties are groups of separate human players, not a roster of collected combat characters controlled by one player.
- Long-term variety must therefore come from the player's own class path, specialization, equipment, stats, skill loadout, passives, and combat-resource choices.
- A player using the same class as another player should still be able to play meaningfully differently through build choices.
- Solo play uses that same persistent character and must not assume a collectible party roster.

## Confirmed direction

- Rookvale should contain a **broad and varied class roster** so different fantasies, combat styles, roles, aesthetics, and player preferences have meaningful options.
- Classes should support distinct multiplayer roles without forcing every class into a single rigid role.
- Branching advancement / class-change trees should exist where they create meaningful identity.
- Hybrid roles are allowed and desirable where they create interesting party choices.
- Classes should learn **more active skills than they can equip at once**.
- Before combat, players build a combat skill loadout from their learned skill pool.
- The loadout is a skill-selection system, not a randomized card-draw/deckbuilder system.
- Skill-slot limits should create build identity without making a single-avatar character feel artificially stripped of necessary tools.
- **Combat skills are class-bound.** Rookvale does not use Orna-style broad cross-class skill inheritance as the default.
- A character cannot assemble a universal best-of-every-class hotbar by collecting unrelated jobs.
- Parent/base abilities may remain available to their own descendant branches where the class tree explicitly treats them as part of the same lineage, but unrelated class branches do not freely share skills.

## Skill-loadout principle

A class may eventually know many attacks, defensive tools, buffs, debuffs, heals, setup skills, counters, formation tools, control skills, and resource spenders. Only a selected subset is equipped for combat.

This supports:

- multiple viable builds within the same class;
- specialization for solo, party, boss, farming, support, PvP, or other content;
- meaningful preparation before difficult encounters;
- continued rewards from learning new skills without placing every learned skill on the battle UI;
- readable mobile / web / Roblox combat interfaces.

Universal commands such as Defend, basic item access, escape, and other system actions do not necessarily need to consume normal skill-loadout slots. Class mechanics or class-resource controls may also live outside the ordinary skill slots when appropriate.

The exact maximum number of equipped skills is not locked yet. It must be tested with the fact that Rookvale gives each player only one persistent combat character rather than a collectible party roster.

## Role vocabulary

Possible roles include:

- sustained damage;
- burst damage;
- frontline protection;
- ally protection / interception;
- direct healing;
- regeneration / prevention;
- buffs;
- debuffs;
- crowd control;
- turn manipulation;
- resource support;
- summons / companions;
- hybrids.

Roles are not necessarily one-to-one with classes.

## Class-tree principle: deliberately asymmetric

Rookvale does **not** use a globally fixed rule such as “every class branches exactly twice,” “every node has exactly two children,” or “every lineage has the same depth.”

A class should branch only when there is a genuinely distinct fantasy, combat loop, resource pattern, role, passive identity, or build space worth separating.

Valid structures include all of the following:

```text
A -> B -> C -> D
```

A mostly linear lineage whose later promotions deepen the same identity.

```text
A
├─ B
├─ C
└─ D
```

A single major specialization point with several distinct fantasies.

```text
A
├─ B
│  ├─ E
│  └─ F
├─ C
└─ D
   ├─ G
   ├─ H
   └─ I
```

An asymmetric tree where only branches with meaningful further identities divide again.

Different class families may therefore have different branch counts and different depths.

### Advancement rule

A promotion that stays on a linear path must still feel like a new stage of mastery. It should not merely replace old skills with visually larger copies such as `Fireball -> Greater Fireball -> Ultimate Fireball` while keeping the same decision pattern.

A meaningful promotion should add or reshape at least some of the following:

- class passive or class mechanic;
- resource generation/spending pattern;
- skill interactions and combo rules;
- formation or threat behavior;
- status-effect interactions;
- cooldown/timeline manipulation;
- summon behavior;
- defensive or support responsibilities;
- new risk/reward rules;
- new build choices within the same fantasy.

Vertical growth may increase numbers, but **mechanical growth must accompany major class advancement**.

### Expansion rule

Do not extend every lineage forever just because a new tier is possible. Future updates may add:

- new sibling branches;
- a deeper promotion to only selected lineages that genuinely support it;
- entirely new base class families;
- hidden or unusual advancement paths;
- side-grade specializations.

Tree shape follows design quality, not symmetry.

## Passive identity

Class passives are a major part of class identity, not filler.

Each playable class stage should normally have an **innate class passive / mechanic** that is always associated with that class or lineage. Advanced classes may strengthen, replace, or reinterpret the parent's mechanic.

Good passives change rules or decisions, for example:

- gaining Resolve when intercepting damage rather than merely gaining +5% Defense;
- spreading Ash when a burning enemy dies;
- converting overhealing into a temporary barrier;
- gaining Momentum when attacking a marked target;
- altering how Mana is restored or spent;
- changing how threat, rows, cooldowns, CC, or summons work.

Rookvale may additionally use **selectable class-bound passive traits** to differentiate two players of the same class. Exact passive-slot counts and UI are still open.

Avoid passive trees dominated by small generic stat bumps. Flat numbers may support a build, but major passive choices should usually change behavior.

## Resource direction

Cooldowns are already part of combat. Classes may additionally use distinct combat resources rather than forcing one universal MP model on every class.

Candidate examples, not yet individually locked:

- martial rage / momentum;
- tank resolve / guard resource;
- healer grace / faith;
- caster mana or another magical resource;
- rogue momentum / combo-style resource;
- ranged focus.

A class resource should change how that class is played rather than merely rename a generic mana bar.

## Class diversity rule

Class variety should be broad in **fantasy and mechanics**, not merely in element names or damage colors.

For example, magical branches may include elemental specialists, summoners, curse/debuff casters, barriers/control casters, time/turn manipulators, battle mages, blood magic, necromancy, soul magic, or other mechanically distinct fantasies. If elemental branches exist, Fire / Ice / Storm should play differently rather than being the same spell kit with different VFX.

Likewise martial, support, ranged, nature, occult, crafting/combat-hybrid, pet/summon, defensive and agile fantasies can receive their own class families where they justify distinct gameplay.

## Do not overload the Mage tree

Not every supernatural or spell-using fantasy should automatically descend from `Mage`.

Current proposal for later discussion:

```text
Mage / Arcane family
├─ Elemental paths
├─ pure arcane / mana paths
├─ time / space / control paths
└─ other conventional spellcraft

Occult / forbidden-arts family
├─ Necromancer
├─ Blood Mage / Hemomancer
├─ Hexer / Cursemancer
└─ soul / ritual branches
```

This is a structural proposal, not locked naming.

The reason is mechanical and organizational: if Mage owns elemental magic, summoning, necromancy, blood magic, curses, time magic, and every other spell fantasy, its tree becomes disproportionately large and its base identity becomes meaningless.

External games show multiple viable models. Guild Wars 2 treats Necromancer as its own profession and Blood Magic as one of its internal specializations; Diablo IV makes Necromancer its own class with Blood, Bone, Darkness, and Army playstyle families. Rookvale can instead make Necromancer and Blood Mage sibling descendants of an occult root if their mechanics are distinct enough.

**Rule:** create a separate class node only when it has enough mechanical identity to deserve one. If Blood Mage and Necromancer ultimately share nearly all gameplay, Blood may be better as a Necromancer specialization. If Blood Mage revolves around HP sacrifice, lifesteal, self-inflicted risk, and blood-resource management while Necromancer revolves around corpses, minions, life force, and death effects, they should be separate branches.

## Open questions

- Exact number and identity of starting/base classes.
- Final magic-family structure and whether `Occultist` (working name) is a starting class or a later branch.
- Exact Necromancer / Blood Mage relationship.
- Can players switch between already-unlocked sibling branches outside combat, and at what cost/location?
- Is progression primarily character level, class level, equipment, skill mastery, or a combination?
- How much build identity comes from equipment versus class?
- Exact number of equipped active skill slots at early, mid, and endgame.
- Exact structure and number of selectable passive traits.
- Whether a dedicated signature/ultimate slot exists outside the normal skill loadout.
- Whether loadout presets can be saved and swapped outside combat.
- Which classes use Mana and which use other class-specific resources.
- Should party role shortages be mitigated by consumables, flexible hybrids, encounter scaling, or another system without turning the game into a collectible-party RPG?
