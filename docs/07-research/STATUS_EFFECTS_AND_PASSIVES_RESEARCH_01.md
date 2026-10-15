# Status Effects, Crowd Control & Passive Identity Research 01

**Status:** Research note — exact effect list and formulas remain open.

## Rookvale requirements from current design discussion

- CC, buffs, and debuffs should be broad enough that support/control classes feel genuinely different.
- Effects should not be cosmetic copies that only change color or damage type.
- Class passives are a major source of identity and should alter gameplay rules, resource loops, formation, threat, timing, or skill interactions.
- Bosses and elite enemies must not make control-focused classes useless simply by being universally immune to CC.
- Rookvale is a sequential turn-based RPG with a Speed timeline, one normal action per natural turn, front/back rows, class-bound skill loadouts, cooldowns, and class-specific resources. Status design must fit those systems rather than copy real-time games literally.

## External references

### Guild Wars 2 — boon / condition vocabulary

Useful principle: divide combat effects into clear functional families instead of giving every class bespoke unreadable rules.

Guild Wars 2 has standardized positive `boons`, negative `conditions`, and separate hard control effects. Different professions specialize in different subsets, and skills/traits can remove, convert, or interact with those effects.

Relevant ideas for Rookvale:

- buffs can be standardized enough to remain readable across many classes;
- conditions can stack by duration or intensity depending on effect type;
- class identity can come from how a class applies, consumes, converts, spreads, or exploits common statuses rather than inventing a new status name for every skill;
- cleanses, resistance, buff removal, buff stealing, and condition conversion create support/counterplay depth.

Sources:
- https://wiki.guildwars2.com/wiki/Boon
- https://wiki.guildwars2.com/wiki/Condition

### Guild Wars 2 — control effects and Defiance bars

Useful principle: bosses can resist direct hard CC without making CC skills worthless.

Against enemies with Defiance bars, control effects do not simply stun-lock the target. Instead, hard and soft CC damage a separate control bar. Breaking it interrupts/staggers the target and may create a vulnerability window.

This is highly relevant to Rookvale because a turn-skipping stun is much stronger in a sequential turn game than a short real-time stun.

Candidate Rookvale adaptation:

- ordinary enemies: direct CC can function normally;
- elites/bosses: major hard CC contributes `Break / Resolve / Poise` damage instead of repeatedly deleting full turns;
- when the control bar breaks, the enemy can lose or delay an action, interrupt a telegraphed skill, become Exposed, or suffer another encounter-specific penalty;
- this keeps controller classes useful in boss fights without enabling permanent stun chains.

Sources:
- https://wiki.guildwars2.com/wiki/Control_effect
- https://wiki.guildwars2.com/wiki/Defiance_bar

### Guild Wars 2 — traits / specializations

Useful principle: passive choices should define builds, not just add tiny statistics.

Guild Wars 2 traits can modify skills, grant automatic effects under conditions, interact with boons/conditions, or alter profession mechanics. Major traits are chosen from mutually exclusive options, while minor traits are inherent to an equipped specialization.

Candidate Rookvale adaptation:

- every class has one or more innate identity passives/mechanics;
- classes may additionally unlock class-bound selectable passive traits;
- selectable passives should create different builds within the same class;
- major passives should alter behavior instead of being dominated by generic `+3% damage` choices.

Sources:
- https://wiki.guildwars2.com/wiki/Trait
- https://wiki.guildwars2.com/wiki/Specialization

### Necromancer / Blood Magic examples

Guild Wars 2 treats Necromancer as a full profession, with Blood Magic as one specialization focused on life steal, healing and revival. Diablo treats Necromancer as a full class with several major playstyle families including Blood, Bone, Darkness, and Army/minions.

The important lesson is not the exact hierarchy. It is that `blood`, `death`, `minions`, `curses`, and `life force` can be related while still deserving separate mechanical identities if their combat loops are genuinely different.

Sources:
- https://wiki.guildwars2.com/wiki/Necromancer
- https://wiki.guildwars2.com/wiki/Blood_Magic
- https://news.blizzard.com/en-gb/article/23816542/diablo-iv-quarterly-updatejune-2022

## Candidate Rookvale effect taxonomy

The exact names are placeholders. The goal is to reserve distinct mechanical jobs for different status families.

### Hard control

Effects that directly deny or replace an action. These are extremely powerful in a one-action-per-turn game and therefore need strong resistance rules.

Candidate types:

- **Stun** — next natural action is lost or heavily delayed.
- **Sleep** — cannot act until duration expires or a wake condition occurs; damage may break it.
- **Freeze / Petrify** — stronger lock with a distinct break or vulnerability rule.
- **Daze** — restricts the next action rather than fully deleting it.
- **Fear / Panic** — may force a defensive/basic behavior or manipulate formation/threat instead of simply duplicating Stun.

Do not create five names that all mean `skip one turn`.

### Action restrictions

Control that preserves a turn but limits options.

Examples:

- Silence — magic-tagged skills unavailable.
- Disarm — weapon-tagged skills unavailable.
- Seal — class mechanic or signature action disabled.
- Item lock — item command unavailable.
- Guard break — defensive commands or protection effects weakened.

These can often be healthier than hard turn deletion because the target still gets to make a decision.

### Timeline control

Especially important because Rookvale uses a continuous Speed timeline.

Examples:

- Slow — reduces effective Speed or increases next-action delay.
- Haste — increases effective Speed.
- Delay — pushes the target backward on the timeline once.
- Advance — pulls an ally forward on the timeline.
- Interrupt — cancels a telegraphed/charging action and applies timeline penalty.

Timeline effects must be balanced carefully because Speed also accelerates natural cooldown cycling.

### Formation / threat control

Examples:

- Taunt / Provoke — forces or heavily biases target selection.
- Guard / Intercept — redirects an attack.
- Threat up/down — modifies target weight.
- Push / Pull — changes front/back row when an ability supports displacement.
- Anchor — prevents forced row movement.
- Mark — makes one target strategically attractive to allies or enemies.

### Offensive debuffs

Examples:

- Vulnerable / Exposed — incoming damage increased.
- Armor break — physical mitigation reduced.
- Ward break — magical mitigation reduced.
- Weakness — outgoing damage reduced.
- Accuracy / evasion manipulation if an accuracy system is adopted.
- Healing received reduction.
- Resource-generation reduction.
- Cooldown disruption, only on rare/telegraphed effects because it can be oppressive.

### Damage-over-time conditions

DoT types should not differ only by element.

Possible identities:

- Bleed — physical stacking damage, perhaps stronger from repeated hits.
- Burn — high pressure and possible spread/execute interactions.
- Poison — damage plus healing reduction.
- Curse / Decay — low immediate damage but scaling or detonation interactions.
- Frostbite — damage plus Speed/timeline interaction.

Not all of these need to exist. Each included DoT should justify its own gameplay.

### Defensive/support buffs

Examples:

- Barrier — temporary extra effective HP.
- Guard / Protection — percentage or flat mitigation.
- Aegis — blocks one attack.
- Regeneration — healing over natural turns.
- Resistance — reduces or ignores specific debuff categories.
- Stability — prevents hard displacement/control.
- Cleanse shield — blocks the next negative status.
- Haste — timeline acceleration.
- Resource support — increases class-resource generation rather than generic damage.
- Threat manipulation — helps tanks or protects fragile allies.

### Conversion / exploitation mechanics

A major source of class identity can be interaction with statuses rather than just applying them.

Examples:

- consume Bleed stacks for burst damage;
- spread Burn when a target dies;
- convert enemy buffs into debuffs;
- convert ally debuffs into buffs;
- gain class resource when cleansing;
- heal allies based on conditions removed;
- detonate curses;
- extend one status while consuming another;
- transfer conditions between targets;
- steal or copy a buff.

## Passive-design rule

Every major class should answer:

1. What does this class do automatically that no generic character does?
2. What behavior does the passive reward?
3. How does the passive interact with the class resource, cooldowns, rows, Speed, threat, or status effects?
4. Can two players of the same class select passives that produce meaningfully different builds?

Bad passive:

`+5% attack.`

Better passive:

`Whenever you intercept damage for an ally, gain 1 Resolve. At 3 Resolve, your next Guard skill gains no cooldown.`

Bad promotion:

`Fireball II: Fireball but +40% damage.`

Better promotion:

`Ash Memory: enemies that die while Burning leave Ash. Ash can be consumed by selected skills to reduce cooldowns, spread Burn, or create a defensive smoke effect.`

## Key balance warning for Rookvale

Hard CC is unusually valuable because one natural turn usually equals one full action. Therefore:

- ordinary trash enemies can be more vulnerable to direct control;
- elites/bosses should usually use control resistance / break bars / diminishing returns;
- PvP, if added, will need its own anti-stunlock rules;
- status duration should specify whose turn clock it follows: caster turns, target turns, natural turns only, timeline units, or encounter phases;
- bonus actions must not accidentally tick every buff/debuff/cooldown unless explicitly intended.

## Recommendation for next design step

Before naming dozens of classes, define a shared status vocabulary and then decide which class families specialize in:

- direct damage;
- DoT;
- hard CC;
- soft control / timeline manipulation;
- buffing;
- debuffing;
- cleansing / conversion;
- threat / formation control;
- summon control.

This makes it easier to create many classes that are genuinely different instead of visually different versions of the same damage dealer.
