# Active / Passive Ability Design Research 01

**Status:** Research baseline — not a final skill list.

This note establishes how Rookvale should research active and passive abilities before production-class kits are finalized.

## Design premise

Rookvale is a single-avatar RPG. Each player controls one persistent combat character, so class identity and build variety must come from the depth of that character rather than from swapping among a roster of collectible units.

Therefore active and passive design must support:

- meaningful loadout choice inside one class;
- different builds for two players using the same class;
- viable solo play and distinct multiplayer roles;
- class-bound skill identity;
- interaction with turn cooldowns, Speed, front/back rows, threat, CC, resources and passives;
- future expansion without requiring every old skill to be replaced by a numerically stronger clone.

## Reference: Guild Wars 2

Useful principles:

- profession-specific mechanics help make the class itself feel different before individual skills are considered;
- specializations/trait lines let passives reinforce different aspects of one profession;
- minor traits can define a specialization automatically, while major traits provide player-selected build differences;
- elite specializations have historically changed weapons, profession mechanics, utility skills and traits rather than merely adding stronger numbers;
- current expansion design also demonstrates that a specialization can change mechanics and traits without requiring a new weapon every time.

Rookvale takeaway:

- innate class passive/mechanic and selectable passives should be separate concepts;
- advanced classes may reinterpret the parent's class mechanic;
- passive choices should change behavior, not just stats;
- weapon unlocks are a useful advancement tool but should not be mandatory for every branch.

Sources:
- https://www.guildwars2.com/en/news/specializations-part-two-reward-tracks-and-elite-specializations/
- https://www.guildwars2.com/en-gb/news/specializations-part-one-a-primer/
- https://www.guildwars2.com/en-gb/news/from-the-wilds-to-whats-next/
- https://wiki.guildwars2.com/wiki/Specialization

## Reference: Last Epoch

Useful principles:

- a character can know many skills but only a limited number are placed on the action bar;
- the game currently uses five skill-specialization slots;
- each specialized skill can have its own skill tree;
- skill nodes can change resource cost, delivery, targeting, element, behavior or even transform the skill into a substantially different version;
- class and mastery passives provide another independent customization layer.

Rookvale takeaway:

- limited active slots can still provide deep build variety if each class learns substantially more skills than it can equip;
- one active skill does not have to remain mechanically static forever;
- selected skill-modification choices may be valuable later, but Rookvale should avoid copying Last Epoch's full per-skill-tree complexity before the core turn combat is proven;
- a smaller transformation/augmentation layer could let the same class support multiple builds without multiplying the active-skill count infinitely.

Sources:
- https://support.lastepoch.com/hc/en-us/articles/46363203944859-Skill-Specialization
- https://support.lastepoch.com/hc/en-us/articles/46363194853915-Unlocking-Skills
- https://lastepoch.com/skills/

## Reference: Diablo IV

Useful principles:

- one class contains active skills, enhancements, passive skills and key passives that are intended to create coherent playstyle packages;
- passive and active synergies are communicated together rather than designed as unrelated systems;
- class-specific skill categories support several fantasies within one class.

Rookvale takeaway:

- each mature class should have multiple coherent build packages rather than a random collection of individually strong skills;
- key-passive-like choices can be useful if they meaningfully commit a build to a strategy;
- do not let one universal passive dominate every loadout of a class.

Source:
- https://news.blizzard.com/en-us/article/23938756/make-sanctuary-yoursplay-your-way-in-diablo-iv

## Reference: Orna / Hero of Aethric class design

Useful principles:

- class pages combine learned active skills with class abilities/passives;
- some abilities meaningfully interact with crits, Mana, extra turns, status conditions, followers and ward rather than acting only as static stat bonuses;
- hybrid classes can share broad equipment families while keeping distinct mechanics.

Rookvale takeaway:

- passive abilities can modify the combat loop itself;
- class abilities may act outside the normal active-skill loadout;
- Rookvale should keep the idea of deep single-avatar class identity while rejecting broad cross-class skill mixing as a default.

Example sources:
- https://playorna.com/codex/classes/56/
- https://playorna.com/codex/classes/10/
- https://playorna.com/codex/classes/4/

## Rookvale ability-design rules

### 1. Active skills need jobs, not just damage values

Each active skill should justify its slot through one or more functions:

- reliable damage;
- burst damage;
- resource generation;
- resource spending;
- setup;
- payoff;
- threat manipulation;
- protection/interception;
- healing/prevention;
- cleanse/dispel;
- buff/debuff;
- CC/break contribution;
- row/formation manipulation;
- timeline manipulation;
- summon interaction;
- enemy-intent interaction;
- emergency recovery;
- conditional finisher.

Two skills with the same tactical job should not coexist merely because one is a later, stronger numeric version unless another meaningful distinction exists.

### 2. Passive types should be varied

Passives may:

- change resource gain or spending;
- alter a skill under a condition;
- transform overheal, excess resource or blocked damage into another benefit;
- modify threat or interception;
- change front/back-row rules;
- interact with statuses;
- change cooldown or timeline behavior;
- alter summons;
- create risk/reward states;
- provide conditional reactions or follow-ups;
- change how a weapon family works for that class.

Flat stat passives can exist as supporting nodes but should not dominate major passive choices.

### 3. Class kits should contain internal loops

A class should normally have at least one coherent loop such as:

`setup -> build resource/status -> spend/consume -> recovery/reset`

or

`protect -> gain class state -> counter/retaliate -> restore defensive state`

or

`mark -> exploit -> reposition/timeline reward -> mark again`.

The loop must work in single-target boss fights as well as ordinary encounters unless the skill is explicitly a niche/add-control tool.

### 4. Do not make all builds use the same mandatory active core

If every Pyromancer always equips the same seven of eight skills, the loadout system has failed. Learned skill pools need enough competing tools that different content and playstyles produce real choices.

### 5. Avoid research monoculture

When a production class is designed, inspect several games rather than selecting one title and translating its kit into Rookvale. A tank, for example, may study threat from one MMORPG, guard/interception from another, turn manipulation from a tactical RPG and passive structure from a build-heavy ARPG.

### 6. Adapt to Rookvale's clocks

External abilities must be translated carefully because Rookvale uses:

- sequential natural turns;
- Speed-based turn frequency;
- bonus actions that do not count as natural turns;
- turn-based cooldowns;
- front/back rows rather than free movement/grid positioning;
- multiplayer humans controlling separate characters.

A mechanic that is healthy in real-time combat may become broken when Speed grants extra natural turns, so cooldown/resource/status clocks must be audited when adapting it.

## Research targets for the first eight branches

Before production skill lists are locked, research at least these thematic areas:

- Knight: threat, guard, interception, counter-tanking, mitigation that still works solo.
- Duelist: parry/riposte, precision, tempo, conditional Speed/timeline rewards.
- Hunter: marks, companion interaction, prey states, utility that remains useful without a pet-focused build.
- Marksman: setup shots, armor/weak-point exploitation, slow/high-value attacks, back-row pressure.
- Pyromancer: burn/DoT, detonation, heat/Ash-like resources, controlled burst and spreading effects.
- Cryomancer: slow/freeze distinctions, barriers, shatter/payoff, boss-CC contribution without hard-locking bosses.
- Priest: healing that is more than spam, prevention, cleanse, rescue, overheal conversion, solo offensive route.
- Oracle: enemy-intent reading, buffs/debuffs, prediction, timeline manipulation and anti-loop safeguards.

## Next step

Use this research standard when deciding:

- number of active slots;
- passive-slot structure;
- innate class mechanic vs selectable passives;
- signature/ultimate slot;
- skill augmentation/transformation;
- skill unlock progression;
- the first production-ready skill and passive kits.
