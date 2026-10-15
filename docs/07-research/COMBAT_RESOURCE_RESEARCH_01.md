# Combat Resource Research 01

**Status:** Research note — proposal only, not yet locked.

## Question

Rookvale already uses one standard action per natural turn, turn-based skill cooldowns, a Speed-driven continuous timeline, and special bonus/free actions that are not full turns. The next question is whether skills also need MP/stamina/shared points/class-specific gauges, and how those systems should interact with Speed.

## External references

### Honkai: Star Rail
- The party shares one Skill Point pool.
- Skills consume Skill Points and basic attacks restore them.
- Energy is a second resource that charges through combat and enables Ultimates.
- Useful lesson: a shared resource makes party composition and action choice interact, but it also means one player's decision can consume a resource wanted by another player.

Source:
- https://wiki.hoyolab.com/pc/hsr/entry/1618?lang=en-us

### OCTOPATH TRAVELER
- Each character accumulates Boost Points over turns and may bank them for stronger attacks, healing, or support effects.
- Useful lesson: a small bankable per-character combat resource creates timing decisions without permanently exhausting the character.

Sources:
- https://www.square-enix-games.com/en_GB/news/octopath-traveler-i-and-ii-now-available-current-console-platforms
- https://www.square-enix-games.com/tagged/products%3AOCTOPATH%20TRAVELER%20II

### Bravely Default II
- Brave Points can be saved or spent to take multiple actions.
- Useful lesson: banking actions can create strong burst windows, but Rookvale should not copy routine multi-action turns because its multiplayer target is faster and each player's ordinary turn should remain one action.

Source:
- https://eu.store.square-enix-games.com/bravely-default-ii---digital

### Guild Wars 2
- Professions use distinct profession mechanics such as adrenaline, life force, initiative, illusions, and other unique gauges/mechanics.
- The profession mechanic is a major part of class identity rather than a universal resource imposed on every class.
- Thief Initiative is especially useful as a warning case: replacing cooldowns with a shared skill resource enables rapid burst, but changes the whole cadence of the class.

Sources:
- https://wiki.guildwars2.com/wiki/Profession_mechanic
- https://wiki.guildwars2.com/wiki/Skill_bar
- https://wiki.guildwars2.com/wiki/Initiative

### World of Warcraft
- Different classes/specs use different resources: for example Warrior Rage, Paladin Mana/Holy Power, and Druid forms with Mana/Rage/Energy/Astral Power.
- Current class design continues to use resource generation/spending as part of class identity.
- Useful lesson: tanks, healers, and damage classes do not need to share one universal resource model.

Sources:
- https://worldofwarcraft.blizzard.com/en-us/game/classes/druid
- https://worldofwarcraft.blizzard.com/en-us/game/classes/paladin
- https://worldofwarcraft.blizzard.com/en-us/news/24301514/

### Darkest Dungeon
- Combat has strong class differentiation, limited equipped skills, formation requirements, statuses, and opportunity costs without relying on a universal mana bar for every action.
- Useful lesson: cooldown/resource complexity is not required on every skill if targeting, formation, statuses, and role interactions already create meaningful choices.

Sources:
- https://darkestdungeon.wiki.gg/wiki/Getting_Started
- https://darkestdungeon.wiki.gg/wiki/Stress

## Options considered

### A. Cooldowns only

Advantages:
- Very readable on web/mobile/Roblox.
- No resource starvation.
- Easy for new players to understand.

Risks:
- Players can fall into a fixed rotation: use the strongest available skill, then the next, then repeat.
- Speed already increases action frequency and cooldown recovery, so fast builds become especially efficient without another constraint.
- Different classes may feel mechanically similar if only skill lists differ.

### B. Cooldowns + universal MP/stamina for everyone

Advantages:
- Familiar RPG language.
- Long fights gain attrition and resource conservation.
- Can counterbalance very fast characters by letting them exhaust resources faster.

Risks:
- Cooldown plus universal cost can become a double tax: a skill may be ready but still unusable.
- Every class gets pushed toward similar resource management.
- Creates potion/rest/recovery balance problems across open-world exploration.
- Especially dangerous for healers: running out of the universal resource can make the whole party helpless.

### C. Cooldowns + party-shared combat resource

Advantages:
- Strong party coordination and tradeoffs.
- One player's cheap action can fund another player's expensive action.

Risks for Rookvale:
- Rookvale is multiplayer with separate human players. Shared spending can create friction or griefing: one player can consume points another player expected to use.
- Requires more communication, conflicting with the goal of making ordinary party play work without constant voice/chat coordination.

Recommendation: do not use a mandatory shared pool as the main skill resource. A later optional party mechanic or specific class can interact with shared resources, but not the base system.

### D. Cooldowns + class-specific combat resource

Advantages:
- Strongest class identity.
- Generation rules can reward the behavior that class is supposed to perform.
- Resource systems can differ by branch or advanced class without changing the one-action-per-turn baseline.
- Supports solo and party roles without forcing every class into the same rhythm.

Risks:
- More UI/tutorial complexity.
- Poorly designed resources can become decorative gauges that always fill automatically.
- If every resource simply gains +1 each natural turn, Speed becomes too multiplicative.

## Current proposal for Rookvale

Use **turn cooldowns as the universal limiter** and add a **small class-specific resource/mechanic only where it creates identity**.

Do **not** require every normal skill to consume a resource.

Suggested hierarchy:

1. **Basic/core actions** — usually no resource cost and little/no cooldown.
2. **Normal class skills** — primarily balanced by turn cooldowns.
3. **Signature/spender skills** — consume the class's unique resource and may also have a cooldown if necessary.
4. **Ultimate-style skills** — may use a larger class gauge, charges, encounter condition, or long cooldown; exact system remains open.

This keeps ordinary turns readable while giving each class a different combat rhythm.

## Example class-resource directions — examples only

These are mechanic sketches, not class names or locked designs.

- Martial attacker: builds **Rage/Drive** by dealing or receiving meaningful damage; spends it on burst attacks, counters, or armor breaking.
- Guardian/tank: builds **Resolve/Guard** by being targeted, blocking, intercepting, or successfully protecting allies; spends it on powerful protection and threat-control actions.
- Mage: uses **Mana/Arcana** as a finite or slowly recoverable personal pool, making high-Speed casting capable of strong burst but not infinite sustained spam.
- Healer/support: builds **Grace/Faith** through effective healing, prevention, cleansing, or allies surviving dangerous hits; spends it on burst saves, barriers, mass cleanse, or revival support.
- Rogue/agile class: builds **Momentum** through successful attacks, crits, exploiting marked targets, or attacking from favorable conditions; spends it on finishers or evasion/position tricks.
- Ranger/controller: builds **Focus** through marking, precise attacks, or maintaining pressure on a target; spends it on powerful shots or control.

## Important Speed interaction

Speed already does two valuable things in Rookvale:

1. grants more natural turns over time;
2. therefore advances personal turn-based cooldowns faster.

If every class also regenerates its resource automatically on every natural turn, Speed would additionally accelerate resource generation. That can create a triple benefit.

Therefore:
- avoid a universal rule of `+1 resource every turn` for all classes;
- prefer generation tied to class-relevant events/actions, finite starting pools, target interactions, taking damage, protecting allies, successful hits, or other gameplay conditions;
- if a resource does regenerate on turns, tune that class around the interaction deliberately;
- bonus/free actions should not automatically trigger full-turn passive resource regeneration unless explicitly stated;
- Speed soft caps/diminishing returns still need to be designed and tested.

## Recommendation

Prototype **Option D: cooldowns + selective class-specific resources**.

Do not add universal MP to every class by default. Mana can still exist as the defining personal resource of magical branches, while martial, tank, healer, agile, and other branches can use mechanics that reinforce their intended play.

## Next decisions

Before locking actual classes, decide:

1. Whether every base class needs a unique resource, or only advanced/specialized classes.
2. Whether class resources persist between field battles or reset/start at a defined value each encounter.
3. Whether there is a separate universal Ultimate gauge at all.
4. What the no-cooldown/basic action does for each class so there are no dead turns.
5. How many active skills are equipped/available in battle.
6. Whether items consume the standard action and whether item use has its own cooldown/limits.
