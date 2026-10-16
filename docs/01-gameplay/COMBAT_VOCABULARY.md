# Combat Vocabulary and Duration Rules

**Status:** Prototype rules locked enough for first implementation; values and some future-only statuses remain tunable
**Date:** 2026-10-16

This document is the shared combat language for the first Rookvale prototype. Class documents may define class-specific resources such as Resolve, Tempo, Aim, Ash, Frost, Grace, and Omens, but common status names must follow the meanings here.

The governing rule is simple:

> Two separately named statuses should not exist if they create the same decision.

## 1. Time vocabulary

### Natural Turn
A **Natural Turn** is a full turn earned from the Speed timeline.

A Natural Turn:
- processes natural-turn start effects;
- may tick/decrement eligible cooldowns;
- grants the normal standard action;
- processes natural-turn end effects;
- counts for target-turn durations.

### Bonus / Free Action
An action granted by a skill or special effect that is explicitly not a Natural Turn.

It does **not** by default:
- tick cooldowns;
- tick DoT/HoT;
- decrement target-turn duration;
- grant natural-turn resource income;
- trigger another full Reaction chain.

### Reaction
An out-of-turn response from the equipped Reaction layer.

It follows the same temporal safeguard as Bonus Actions:
- no ordinary cooldown tick;
- no target-turn duration tick;
- no ordinary DoT/HoT tick;
- cannot recursively trigger another Reaction unless a future effect explicitly overrides the global rule.

### Timeline Unit (TU)
The shared continuous combat timeline uses abstract **Timeline Units**.

At Speed 100, a standard-delay action schedules the next Natural Turn roughly 100 TU later before other modifiers.

Timeline Units are used for:
- one-shot Delay/Advance;
- battlefield fields;
- encounter timers;
- effects that must not become shorter simply because there are more combatants.

## 2. Duration clocks

Rookvale does not force every effect onto one timer type.

Every timed effect must declare one of the following clocks.

### A. Target Natural Turns — default action-bound clock
Use when the effect is intended to influence a fixed number of the affected unit's own actions.

Examples:
- Poison;
- Regeneration;
- Silence;
- Disarm;
- most ordinary Damage Up/Down or Defense Up/Down states;
- some Slow/Haste states.

Rules:
- a target Natural Turn begins even when the unit is unable to act because of hard control;
- start-of-turn effects still process;
- if the action is skipped, the turn still reaches an end boundary;
- the duration decrements once at the end of that Natural Turn;
- effects applied during the current Natural Turn do not immediately lose a duration count on that same turn.

This prevents Stun/Freeze from freezing their own timer forever.

### B. Until Source Next Natural Turn — prepared-window clock
Use for a state created now that should protect/respond until the creator naturally acts again.

Examples:
- Knight Guard;
- Marksman Overwatch;
- Duelist Riposte Stance;
- Oracle Premonition;
- some trap/readied-action windows.

Default expiry:
- at the start of the source's next Natural Turn, before the source chooses the next action.

This clock should usually also have an event cap so a very active enemy cannot produce unlimited value before the source returns.

### C. Eligible Event Charges — bounded trigger clock
Use when the effect is about a known number of future hits/triggers rather than elapsed turns.

Examples:
- Guard the next eligible direct hit;
- absorb the next two direct hits;
- prevent the next severe debuff;
- trigger on the next predicted Attack action;
- Signature protection for the next three eligible hostile actions.

Rules:
- only matching events consume charges;
- irrelevant events do not consume charges;
- an effect may also have a safety expiry such as `until source next Natural Turn`.

### D. Timeline Units — global/field clock
Use for effects that should have roughly the same real timeline duration in solo and four-player combat.

Examples:
- battlefield weather/field states;
- large Signature zones;
- encounter-wide danger windows;
- global phase timers.

This avoids a field expiring four times faster simply because four party members are generating more action events.

## 3. Periodic damage and recovery

Periodic effects normally tick at a Natural Turn boundary and never on Bonus Actions/Reactions.

### Burn
**Role:** stackable fire pressure / Pyromancer setup resource

Prototype identity:
- stackable Intensity, default cap 5;
- duration is normally Target Natural Turns;
- ticks at the **start** of the target's Natural Turn;
- direct fire skills may spread, refresh, intensify, consume, or transform Burn;
- Burn is therefore both DoT and stored tactical setup.

Burn does **not** globally reduce healing. Anti-heal is a separate effect so Pyromancer's Brand-style tools remain meaningful.

### Bleed
**Role:** wound pressure that punishes physical exertion

Prototype identity:
- stackable, default cap 3;
- ticks at the **end** of the target's Natural Turn;
- deals normal Bleed damage every tick;
- if that turn used a Movement-tagged or Weapon/Direct-attack-tagged action, the tick gains a moderate bonus;
- does not trigger on Bonus Actions/Reactions unless a skill explicitly says the extra action aggravates Bleed.

This makes Bleed behaviorally different from Burn and Poison.

### Poison
**Role:** stable attrition / anti-high-defense DoT

Prototype identity:
- normally one Poison instance with Potency rather than many independent stacks;
- ticks at the **start** of the target's Natural Turn;
- lasts longer than Burn by default;
- ignores part of Defense;
- reapplication normally refreshes duration or replaces the instance if the new Potency is stronger.

Poison is meant to be dependable attrition, not another consumable combo resource.

### Regeneration
**Role:** scheduled recovery

Prototype identity:
- ticks at the **start** of the target's Natural Turn;
- uses Target Natural Turns;
- does not automatically convert overheal into Barrier unless the originating skill/passive explicitly allows it;
- Bonus Actions/Reactions do not create extra Regen ticks.

## 4. Soft timeline control

### Slow
**Role:** persistent future-action slowdown

Slow changes the delay used when the target schedules its next Natural Turn.

Prototype baseline:
- ordinary Slow is around +15% to +20% next-action delay;
- stronger versions should usually be short or conditional;
- Slow is capped so repeated sources cannot multiply into near-permanent turn denial.

Slow does not directly move the target's already-scheduled next-action point unless the skill explicitly also applies Delay.

### Haste
**Role:** persistent future-action acceleration

Haste changes the delay used when the target schedules its next Natural Turn.

Prototype baseline:
- ordinary Haste is around -10% to -15% next-action delay;
- strong Haste is preferably charge-based (`next action`) rather than a long stat multiplier;
- Haste never grants an immediate full Natural Turn by itself.

### Delay
**Role:** one-time push backward on the current timeline

Delay directly moves the target's already-scheduled next-action point later.

It:
- has no duration;
- is not the same as Slow;
- is strongly capped on bosses;
- cannot push a target indefinitely through repeated small effects.

### Advance
**Role:** one-time pull forward on the current timeline

Advance directly moves an ally's already-scheduled next-action point earlier.

It:
- has no duration;
- is not the same as Haste;
- cannot cross the global minimum-distance floor from the present timeline point;
- cannot create an immediate infinite-turn loop.

### Chill
**Role:** Cryomancer soft control / Freeze setup

Chill is a cold-specific soft-control state.

Prototype identity:
- mild Slow-like scheduling penalty;
- improves Frost/Freeze-related interactions;
- weaker as raw timeline control than dedicated Slow;
- may be stacked/converted by Cryomancer mechanics.

Chill is not itself hard CC.

### Shock
**Role:** conductive setup / interrupt and Break vulnerability

Prototype identity:
- not a Stun;
- the next eligible direct hit against a Shocked target gains additional Break/interrupt potency and consumes or weakens Shock;
- selected lightning effects may refresh/chain it later.

Shock is included in the vocabulary bank but is not required for the first eight-class implementation.

## 5. Hard control — deliberately non-identical

### Stun
**Role:** immediate interrupt / timeline shove

Stun is primarily an **interrupt event**, not a stored one-turn debuff.

Against a normal target:
- if the target is preparing an interruptible telegraphed action, Stun cancels that preparation;
- otherwise Stun applies a strong bounded Delay to the current next-action point;
- Stun then resolves; it does not sit for multiple target turns.

Against bosses/elites:
- only explicitly interruptible actions may be cancelled;
- otherwise Stun converts to bounded Delay + Break contribution.

This differentiates Stun from Freeze and Sleep.

### Freeze
**Role:** thresholded stored action denial / Shatter interaction

Against ordinary enemies:
- Freeze is normally reached through enough cold/Frost setup rather than one low-cost button;
- on the target's next Natural Turn, the action is replaced by a **Thaw** event and the target loses that standard action;
- Freeze then ends;
- while Frozen, the target cannot voluntarily change rows and is especially susceptible to designated Shatter/Break interactions;
- Fire-tagged counterplay may remove Freeze early where specified.

Against elites/bosses:
- raw lost-turn Freeze normally converts into **Deep Freeze pressure**: Break contribution + bounded Delay + cold vulnerability/setup value;
- designated encounter windows may allow stronger Freeze effects.

### Sleep
**Role:** fragile long control / wake-up payoff

Against ordinary enemies:
- the target cannot take a standard action while asleep;
- Sleep may cover more than one Target Natural Turn;
- any eligible damaging hit wakes the target immediately;
- the first wake-up hit receives a defined bonus such as extra damage or Break;
- non-damaging setup can therefore exploit the control window without waking the target.

Against bosses:
- full Sleep normally converts to **Drowsy**: bounded Delay plus a bonus on the next eligible wake-style hit/Break event.

Sleep differs from Freeze because damage deliberately ends it and creates a payoff decision.

### Petrify
**Role:** sequestration / defensive hard control

**Future-bank status; not required in the first slice.**

Planned identity:
- target cannot use normal actions;
- target also gains substantial Defense and displacement immunity;
- useful for removing a unit from the fight temporarily, poor for burst focus;
- boss conversion should emphasize Break/Defense interactions rather than full action deletion.

Petrify must never become `Freeze with a stone icon`.

## 6. Capability restriction

### Silence
**Role:** disable magic/chanted capability without deleting the whole turn

For its duration:
- Spell/Chant-tagged skills are unavailable or severely weakened;
- legal weapon/basic/Defend/item actions remain available;
- if an enemy script has no legal alternative, it uses an explicit fallback rather than losing the turn automatically.

Bosses may convert Silence into cast-delay, secondary-effect reduction, or Break instead of losing signature mechanics.

### Disarm
**Role:** disable weapon capability without deleting the whole turn

For its duration:
- Weapon-tagged skills are unavailable or downgraded;
- spells, items, Defend, innate actions, or explicit fallback attacks remain available;
- major bosses often convert Disarm into reduced weapon-action damage/Break instead of total disable.

### Root
**Role:** voluntary row-movement lock

Root prevents:
- voluntary row change;
- Movement-tagged reposition skills where the movement is required.

It does not prevent:
- attacking;
- casting;
- forced movement from another source unless the effect also says **Pinned**.

### Pinned / Row Lock
**Role:** stronger positional lock

Pinned prevents both voluntary and ordinary forced row movement for a short bounded window.

Against immovable bosses, row-lock value converts into Break/Slow as defined by the skill.

### Fear
**Role:** positional/behavioral disruption, not random turn loss

**Future-bank default:**
- pushes or pressures ordinary targets away from the source/front line;
- restricts aggressive advance behavior for the affected Natural Turn;
- bosses normally convert Fear into Damage Down / Threat-behavior disruption rather than fleeing or skipping turns.

Do not implement Fear as an opaque random `maybe do nothing` status by default.

### Disrupted
**Role:** generic soft interruption when a class needs non-hard control

Prototype identity:
- weakens the next eligible non-basic secondary effect, or increases its action delay;
- consumed by that action;
- used for skills such as Dazzling Prayer where full Silence/Stun would be too strong.

## 7. Break / Stagger

### Break Gauge
Break is a **posture system** shared by ordinary enemies, elites, and bosses.

Break damage reduces a visible Break Gauge.

When the gauge reaches zero, a **Break Event** occurs.

### Break Event
Default result:
1. cancel the current action only if that action is explicitly Breakable;
2. apply a bounded one-shot Delay;
3. apply **Exposed**;
4. restore/rebuild the Break Gauge according to target tier and repeated-break rules.

Break is therefore valuable even when there is no action to cancel because it still creates timing and vulnerability value.

### Repeated-break safeguard
Elites/bosses become temporarily harder to Break repeatedly.

Prototype direction:
- after each boss Break in the same phase, the next Break maximum increases;
- the increase has a cap;
- major phase changes may partially/reset the escalation;
- successful boss Natural Turns recover a small portion of Break Gauge.

This creates coordination without permanent stagger-lock.

## 8. Vulnerability / designation states

### Exposed
**Role:** universal short vulnerability window

Prototype identity:
- increases direct damage taken;
- increases incoming Break contribution;
- normally lasts for a small number of eligible direct hits or until the target completes its next Natural Turn, whichever comes first.

Exposed is the common payoff state. Do not make Mark and Prey duplicate it.

### Mark
**Role:** source-owned setup tag

Global rule:
- Mark has **no automatic universal damage bonus**;
- the skill/class that created the Mark defines what can consume/read it;
- Marks are source-owned so one class's mark does not automatically activate every other class's mark payoff;
- a character may normally maintain one primary Mark at a time unless a class says otherwise.

This preserves Marksman identity and prevents every mark from becoming `+20% party damage`.

### Prey
**Role:** Hunter-specific designation

Prey is not a generic debuff.

It:
- identifies the Hunter's current coordinated target;
- enables Hunter/beast/trap interactions;
- may be changed with an opportunity cost;
- has no universal party damage multiplier;
- is normally not removed by an ordinary generic Cleanse/Dispel because it is a source-owned designation rather than a magical buff/debuff.

Specific anti-mark mechanics may still remove it.

## 9. Protection / targeting

### Barrier
**Role:** temporary extra HP

Global rules:
- damage is mitigated by Defense, then Barrier absorbs the resulting incoming damage unless a skill says it bypasses Barrier;
- Barrier does not automatically block statuses/secondary effects;
- reapplying the same Barrier source refreshes/replaces that source rather than infinitely stacking itself;
- different sources may stack only up to the global Barrier cap;
- ordinary barriers have lower caps than Signature/encounter-specific barriers.

### Guard
**Role:** prepared redirection

Guard is a state connecting a **guardian** and a **guarded target**.

Default eligibility:
- direct single-target hostile attacks;
- not ordinary AoE/row-wide damage;
- scripted `Unredirectable` attacks ignore it.

On trigger:
- the eligible attack is redirected to the guardian according to the skill's split/full-redirect rule;
- the guardian's Defense/Barrier then resolves the redirected damage;
- Guard normally uses event charges and/or `until source next Natural Turn`.

### Intercept
**Role:** emergency Reaction redirection

Intercept is an out-of-turn Reaction, not merely another name for Guard.

Difference:
- Guard is prepared proactively with a standard action;
- Intercept happens reactively when a qualifying attack targets an ally;
- Intercept is weaker/more limited and obeys Reaction cooldown/charge rules.

### Threat
Threat is tracked **per enemy, per player character**.

Threat influences target score; it does not create an absolute target lock by itself.

Sources may include:
- damage;
- effective healing/barrier support;
- Defend/protection skills;
- explicit threat-generation skills;
- scripted AI preferences.

Threat decays over time/enemy turns so one early action does not permanently determine targeting.

### Taunt / Challenge
Taunt is a temporary **Threat/target-score modifier**, not a universal mind-control status.

It:
- heavily raises the user's target score for the affected enemy's next eligible direct action;
- cannot override `Unredirectable`, AoE, puzzle/scripted, or explicit backline-hunter actions;
- remains useful on bosses without requiring bosses to obey it 100% of the time.

## 10. Generic stat modifiers

### Damage Up / Damage Down
Modify final outgoing damage.

Prototype rule:
- same-category modifiers combine additively before the final multiplier;
- global clamps prevent extreme stacking.

### Defense Up / Defense Down
Modify the Defense value used by the mitigation formula.

Defense Down is not the same as Exposed:
- Defense Down changes mitigation;
- Exposed is a short final vulnerability + Break window.

### Healing Up / Healing Down
Modify final healing done/received.

### Healing Reduction / Anti-Heal
A negative Healing Received modifier.

Prototype safeguard:
- ordinary anti-heal is capped and should not casually reach 100%;
- scripted encounter mechanics may exceed the ordinary cap only when clearly telegraphed.

## 11. Status operations

### Cleanse
Removes eligible **negative** effects from an ally/self.

Cleanse does not remove:
- class resources;
- source-owned designations such as Prey by default;
- unique boss mechanics tagged Uncleanseable;
- permanent encounter states.

Skills may specialize by family:
- DoT cleanse;
- control cleanse;
- curse/hex cleanse;
- broad cleanse.

### Dispel
Removes eligible **positive** effects from an enemy.

Dispel does not automatically delete:
- innate mechanics;
- class resources;
- Signature states tagged Unremovable;
- Barrier unless the skill explicitly says it can dispel/strip Barrier.

### Buff Steal
Remove one eligible positive effect from the enemy and apply an allowed copy to the thief.

Safeguards:
- copied duration is capped;
- unique/Signature/innate effects are unstealable;
- target-specific mechanics may convert into a generic weaker equivalent instead of being copied literally.

### Debuff Transfer
Move one eligible negative effect from one unit to another.

Safeguards:
- the receiving target's immunity/resistance/conversion rules still apply;
- source ownership is preserved or explicitly reassigned by the skill;
- unique boss mechanics are non-transferable;
- transferred DoTs cannot bypass boss caps merely because they originated on a player.

## 12. Row displacement

### Push
Front -> Back when legal.

### Pull
Back -> Front when legal.

### Swap
Exchange row positions of two legal units.

### Immovable conversion
If the target cannot move:
- the movement portion fails;
- a skill may explicitly convert movement value into Break, Slow, Threat, or another listed secondary benefit.

Do not silently give every displacement skill free Break; the conversion must be declared by the skill.

## 13. Status resistance model

The first prototype does **not** use a universal `Status Hit Chance` stat contest.

### Soft statuses
Normally deterministic when the attack/skill succeeds.

Targets may have visible category resistance:
- Normal: 100% duration/potency;
- Resistant: reduced duration/potency;
- Highly Resistant: strongly reduced duration/potency;
- Immune: no direct application, but the skill may have a declared fallback.

### Hard-control families
Hard control also tracks **temporary repeat resistance**.

After a successful hard-control event:
- the target becomes more resistant to that same hard-control family;
- repeated immediate applications have reduced effect or require more buildup;
- resistance relaxes after the target completes meaningful Natural Turns and/or after a phase transition.

Bosses normally use control conversion rather than raw hard-control chance rolls.

## 14. Interaction rules that are globally forbidden

- Reaction -> Reaction recursion by default.
- Bonus Action -> full ordinary cooldown/duration/resource processing.
- Mark, Prey, and Exposed all becoming the same party damage multiplier.
- Stun, Freeze, Sleep, and Petrify all becoming `skip one turn` with different icons.
- Slow and Delay being synonyms.
- Haste and Advance being synonyms.
- Guard and Intercept being synonyms.
- Cleanse removing positive buffs or Dispel removing ordinary negative debuffs.
- generic status immunity causing an entire control class to have no boss function.
- ordinary anti-heal reaching effortless permanent 100% healing shutdown.
- unlimited Barrier stacking from repeated copies of the same source.

## 15. First-slice implementation priority

Implement now:
- Burn;
- Bleed;
- Poison;
- Chill;
- Freeze + boss conversion;
- Stun/Interrupt;
- Slow;
- Haste;
- Delay;
- Advance;
- Break / Broken;
- Exposed;
- Mark;
- Prey;
- Barrier;
- Guard;
- Intercept;
- Threat/Taunt;
- Regeneration;
- Healing Reduction;
- Damage/Defense Up/Down;
- Cleanse;
- Dispel;
- Row Push/Pull/Swap;
- Root/Pinned;
- Disrupted.

Can wait until later unless an implemented skill requires it:
- Shock;
- Sleep;
- Silence;
- Disarm;
- Fear;
- Petrify;
- Buff Steal;
- Debuff Transfer.

The vocabulary is defined now so later classes do not reinvent incompatible versions of the same concept.
