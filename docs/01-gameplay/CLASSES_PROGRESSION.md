# Classes and Progression

**Status:** Core identity locked; exact class tree depth and slot counts open

## Player-character model

Rookvale is **not a party-collection game**. Each human player primarily controls and develops **one persistent player character**.

- Multiplayer parties are groups of separate human players, not a roster of collected combat characters controlled by one player.
- Long-term variety must therefore come from the player's own class path, specialization, equipment, stats, skill loadout, and combat-resource choices.
- A player using the same class as another player should still be able to play meaningfully differently through build choices.
- Solo play uses that same persistent character and must not assume a collectible party roster.

## Confirmed direction

- Rookvale should contain a **broad and varied class roster** so different fantasies, combat styles, roles, aesthetics, and player preferences have meaningful options.
- Classes should support distinct multiplayer roles without forcing every class into a single rigid role.
- Branching advancement / class-change trees should exist.
- Hybrid roles are allowed and desirable where they create interesting party choices.
- Classes should learn **more active skills than they can equip at once**.
- Before combat, players build a combat skill loadout from their learned skill pool.
- The loadout is a skill-selection system, not a randomized card-draw/deckbuilder system.
- Skill-slot limits should create build identity without making a single-avatar character feel artificially stripped of necessary tools.
- **Combat skills are class-bound.** Rookvale does not use Orna-style broad cross-class skill inheritance as the default.
- A character cannot assemble a universal best-of-every-class hotbar by collecting unrelated jobs.
- Parent/base abilities may remain available to their own descendant branches where the class tree explicitly treats them as part of the same lineage, but unrelated class branches do not freely share skills.

## Skill-loadout principle

A class may eventually know many attacks, defensive tools, buffs, debuffs, heals, setup skills, counters, movement/formation tools, and resource spenders. Only a selected subset is equipped for combat.

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

## Class-tree principle

A branch should change how the character is played, not just provide larger numbers. Advancement choices should create meaningful tradeoffs and a stronger class fantasy.

Current research recommendation, **not yet locked:** use a finite tree with roughly **two meaningful branching moments after the starting class**, rather than endless recursive branching.

Conceptually:

```text
Base class
  -> first specialization / fantasy branch
       -> advanced specialization / play-style branch
```

Example only:

```text
Mage
  -> Pyromancer
       -> Infernalist
       -> Ashcaller
  -> Cryomancer
       -> Frostwarden
       -> Glaciomancer
  -> Storm Mage
       -> Tempestcaller
       -> Thunder Sage
```

The point is not the names above. The first branch should establish a clear fantasy and core mechanic; a later branch should deepen or redirect the way that fantasy plays.

Infinite or routinely expanding vertical branching is currently discouraged because it geometrically multiplies class count, skill production, balance combinations, UI complexity, and maintenance burden. Future updates should usually add new sibling branches, side-grade specializations, or new base class families rather than extending every existing branch forever.

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

For example, magical branches may include elemental specialists, summoners, curse/debuff casters, barriers/control casters, time/turn manipulators, battle mages, or other mechanically distinct fantasies. If elemental branches exist, Fire / Ice / Storm should play differently rather than being the same spell kit with different VFX.

Likewise martial, support, ranged, nature, occult, crafting/combat-hybrid, pet/summon, defensive and agile fantasies can receive their own class families where they justify distinct gameplay.

## Open questions

- Exact number and identity of starting/base classes.
- Whether the recommended two-branching-stage structure becomes the global default or whether a small number of exceptional classes use a different topology.
- Can players switch between already-unlocked sibling branches outside combat, and at what cost/location?
- Is progression primarily character level, class level, equipment, skill mastery, or a combination?
- How much build identity comes from equipment versus class?
- Exact number of equipped active skill slots at early, mid, and endgame.
- Whether passives have separate slots, come from talent trees, or use another system.
- Whether a dedicated signature/ultimate slot exists outside the normal skill loadout.
- Whether loadout presets can be saved and swapped outside combat.
- Which classes use Mana and which use other class-specific resources.
- Should party role shortages be mitigated by consumables, flexible hybrids, encounter scaling, or another system without turning the game into a collectible-party RPG?
