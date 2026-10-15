# Classes and Progression

**Status:** Core identity locked; exact class tree and slot counts open

## Player-character model

Rookvale is **not a party-collection game**. Each human player primarily controls and develops **one persistent player character**.

- Multiplayer parties are groups of separate human players, not a roster of collected combat characters controlled by one player.
- Long-term variety must therefore come from the player's own class path, specialization, equipment, stats, skill loadout, and combat-resource choices.
- A player using the same class as another player should still be able to play meaningfully differently through build choices.
- Solo play uses that same persistent character and must not assume a collectible party roster.

## Confirmed direction

- Classes should support distinct multiplayer roles.
- Branching advancement / class-change trees should exist.
- Hybrid roles are allowed and desirable where they create interesting party choices.
- Classes should learn **more active skills than they can equip at once**.
- Before combat, players build a combat skill loadout from their learned skill pool.
- The loadout is a skill-selection system, not a randomized card-draw/deckbuilder system.
- Skill-slot limits should create build identity without making a single-avatar character feel artificially stripped of necessary tools.

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

A branch should change how the character is played, not just provide larger numbers. Advancement choices should create meaningful tradeoffs.

Example concept only, **not locked**:

```text
Base vocation
  -> martial branch
       -> defender specialization
       -> aggressive specialization
       -> hybrid specialization
  -> arcane branch
       -> damage specialization
       -> control specialization
       -> summon specialization
  -> support branch
       -> healing specialization
       -> prevention/buff specialization
       -> offensive support specialization
  -> agile branch
       -> assassination specialization
       -> ranged specialization
       -> utility specialization
```

The exact names and topology will be designed later. Bard-style support does not need to originate from a thief branch unless the final world/class logic specifically justifies it.

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

## Open questions

- Fixed starting classes or classless beginning?
- Can characters unlock multiple class branches?
- Can players switch learned classes freely outside combat?
- Is progression primarily character level, class level, equipment, skill mastery, or a combination?
- How much build identity comes from equipment versus class?
- Exact number of equipped active skill slots at early, mid, and endgame.
- Whether passives have separate slots, come from talent trees, or use another system.
- Whether a dedicated signature/ultimate slot exists outside the normal skill loadout.
- Whether loadout presets can be saved and swapped outside combat.
- Which classes use Mana and which use other class-specific resources.
- Should party role shortages be mitigated by consumables, flexible hybrids, encounter scaling, or another system without turning the game into a collectible-party RPG?
