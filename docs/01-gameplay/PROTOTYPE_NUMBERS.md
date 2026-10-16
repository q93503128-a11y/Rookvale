# First Combat Prototype — Numeric Skeleton

**Status:** Draft implementation baseline; all coefficients are deliberately easy to tune
**Date:** 2026-10-16

This document is not final game balance. It provides one coherent first set of numbers so the first eight class loops, status system, Break, threat, healing, barriers, and enemy set can be implemented and tested without every feature inventing its own scale.

Goals:
- small readable numbers;
- no hidden random damage variance;
- Speed matters without exploding turn frequency;
- Defense matters without creating immortal tanks;
- healing/barriers matter without forcing a healer every turn;
- Break is reachable solo and faster with a coordinated party;
- no universal Accuracy/Evasion or Status Hit stat in the first prototype.

## 1. Core player stat scale

First-slice advanced-class benchmark values:

| Class | Max HP | Power | Defense | Speed |
| --- | ---: | ---: | ---: | ---: |
| Knight | 760 | 88 | 75 | 90 |
| Duelist | 600 | 105 | 52 | 112 |
| Hunter | 590 | 100 | 50 | 104 |
| Marksman | 550 | 110 | 45 | 100 |
| Pyromancer | 540 | 112 | 42 | 98 |
| Cryomancer | 570 | 98 | 50 | 96 |
| Priest | 610 | 90 | 52 | 98 |
| Oracle | 570 | 88 | 48 | 106 |

Interpretation:
- **Power** is the first-prototype offensive/support scaling stat. It can scale damage, healing, and barriers with different skill coefficients.
- Do not add separate Attack / Magic Attack / Healing Power stats until testing proves the single Power scale cannot support meaningful equipment/build decisions.
- Physical/Magical remain skill tags for interactions, but the first prototype uses one Defense value.

This is intentional simplification. The combat prototype is testing class loops and timing, not final itemization mathematics.

## 2. Damage formula

### Direct damage

```text
RawDamage = Power * SkillCoefficient
DefenseMultiplier = 100 / (100 + EffectiveDefense)
FinalDamage = floor(RawDamage * DefenseMultiplier * FinalDamageModifiers * CritModifier)
```

Rules:
- no random damage variance in the first prototype;
- minimum successful direct damage: 1 unless the target is explicitly immune;
- EffectiveDefense cannot go below 0;
- ordinary Damage Up/Down combined modifier is clamped to roughly -50% / +50% before exceptional Signature/encounter effects;
- ordinary Defense Up/Down changes Defense itself, not final damage.

### Initial coefficient bands

| Skill type | Typical coefficient |
| --- | ---: |
| weak utility attack | 0.65-0.90 |
| basic attack | 1.00 |
| standard active attack | 1.10-1.45 |
| committed/heavy attack | 1.50-1.90 |
| large resource payoff | 1.80-2.40 |
| ordinary multi-target hit per target | 0.60-1.00 |

A skill may trade coefficient for Break, status, row reach, setup, healing, or protection.

## 3. Critical hits

Prototype baseline:
- base Crit Chance: **5%**;
- base Crit Damage: **150%**;
- no universal Accuracy stat;
- crits are bonus variance, not required for a class's normal rotation.

Precision classes should gain deterministic setup/payoff before they gain huge Crit RNG dependence.

## 4. Accuracy / Evasion decision

**No universal Accuracy or Evasion attributes in the first prototype.**

Default:
- a legal direct attack hits;
- skills can still be Dodged/Blocked by explicit states or scripted mechanics;
- `Obscured`, `Feinted`, `Evasive`, `Precise`, and similar explicit effects may alter a particular action without creating a permanent hit-chance arms race.

Recommended first `Obscured / Suppressed` model:
- -15% direct outgoing damage;
- -25% secondary Break/status potency;
- does not randomly turn an entire action into zero value.

Marksman anti-evasion tools can remove explicit Evasive/Obscured states or bypass their penalties.

## 5. Healing formula

```text
RawHeal = Power * HealCoefficient
FinalHeal = floor(RawHeal * HealingDoneModifier * HealingReceivedModifier)
```

Initial coefficients:
- light utility heal: 0.60-1.00;
- reliable single-target heal: 1.50-1.90;
- emergency heal: 2.00-2.60 plus resource/cooldown cost;
- party heal: 0.65-1.00 per target;
- Regeneration tick: 0.25-0.40.

Suggested Priest first values:
- `Mend`: 1.75;
- `Group Prayer`: 0.80 per target;
- ordinary `Regeneration`: 0.32 per tick.

### Healing reduction

Ordinary Healing Received reduction is capped at **-60%**.

100% anti-heal is reserved for clearly telegraphed exceptional encounter mechanics, not routine status stacking.

## 6. Barrier formula and caps

Default barrier formula:

```text
Barrier = floor(SourcePower * BarrierCoefficient + TargetMaxHP * MaxHPFactor)
```

Initial bands:
- small barrier: 0.45 Power + 2% target Max HP;
- standard barrier: 0.80 Power + 3% Max HP;
- strong standard-action barrier: 1.10 Power + 5% Max HP;
- emergency/Signature barrier: may exceed the ordinary band with explicit cost.

Stacking rules:
- same named/source barrier refreshes or replaces itself; it does not add infinitely;
- ordinary single-source barrier cap: **25% target Max HP**;
- ordinary total barrier cap from all sources: **40% target Max HP**;
- Signatures/encounter effects may explicitly raise the total cap to **60%**;
- Defense mitigates the incoming hit first, then Barrier absorbs remaining damage;
- Barrier does not automatically prevent secondary statuses.

## 7. Periodic effect coefficients

DoT does not use ordinary Defense in the first prototype. Its coefficient is lower and status resistance/cleanse is the counterplay.

DoT cannot critically hit by default.

### Burn
- max Intensity: **5**;
- default duration: **2 target Natural Turns**;
- start-of-turn tick per stack: **0.07 * applier Power**;
- adding Burn refreshes duration to the skill's allowed maximum unless the skill says otherwise;
- Pyromancer can consume stacks with Combust-style skills.

At 5 stacks from a 112-Power Pyromancer, a tick is about 39 damage before Burn-specific modifiers.

### Bleed
- max stacks: **3**;
- default duration: **2 target Natural Turns**;
- end-of-turn tick per stack: **0.06 * applier Power**;
- if the target used a Movement or Weapon/Direct-attack tagged Natural Action that turn, Bleed tick damage is **x1.5**.

### Poison
- normally one instance;
- default duration: **3 target Natural Turns**;
- start-of-turn tick: **0.22 * applier Power**;
- reapplying a weaker/equal Poison refreshes duration;
- reapplying a stronger Poison replaces Potency and refreshes duration.

These are first-test values only. The important locked distinction is behavior, not coefficient.

## 8. Speed and timeline formula

### Base schedule

```text
StandardDelayTU = 10000 / EffectiveSpeed
NextActionTime = CurrentTime + StandardDelayTU * ActionDelayMultiplier * TempoModifier
```

At Speed 100, a standard action produces approximately **100 TU** until the next Natural Turn.

### First-prototype Speed range

Expected ordinary values:
- slow: 85-94;
- average: 95-105;
- fast: 106-115;
- exceptional normal enemy: up to about 125.

Temporary final effective Speed is hard-clamped to **60-160** for the first prototype.

Long-term progression should keep Speed much narrower than HP/Power growth.

### Action Delay multipliers

| Action class | Multiplier |
| --- | ---: |
| quick | 0.85 |
| normal | 1.00 |
| heavy | 1.15 |
| major commitment / large Signature | 1.25 |

A skill should not use a different delay solely to add fake complexity. Use it where action commitment is part of the decision.

### Haste / Slow

Prototype ordinary values:
- Haste: next scheduling delay **-15%**;
- Slow: next scheduling delay **+20%**.

Combined scheduling modifier is clamped to roughly **0.75-1.35** before exceptional encounter rules.

### Delay / Advance

Ordinary one-shot values:
- small: 8-12 TU;
- medium: 15-20 TU;
- strong: 25-30 TU.

Safeguards:
- same target cannot receive more than **30 TU net hostile Delay** between its completed Natural Turns from ordinary player effects;
- bosses use an ordinary hostile Delay cap of **15 TU** between completed Natural Turns unless a Break/phase rule explicitly allows more;
- Advance can never pull a unit closer than **20 TU** from the current timeline point through ordinary effects;
- no first-slice skill grants an immediate full Natural Turn.

## 9. Cooldown semantics

Cooldowns are owned by the character using the skill.

When a skill with `Cooldown N` is used:
1. set remaining cooldown to N;
2. on each **future Natural Turn**, the skill is unavailable while remaining cooldown is above 0;
3. at the end of that Natural Turn, reduce remaining cooldown by 1;
4. Bonus Actions/Reactions do not reduce it.

Therefore:
- CD 0: usable every Natural Turn if other costs allow;
- CD 1: miss one future Natural Turn, then available;
- CD 2: miss two future Natural Turns, then available.

Typical first-slice ranges:
- baseline/filler active: 0;
- ordinary utility/payoff: 1-2;
- strong control/protection: 2-3;
- major standard active: 3-4;
- Signature: 5-7, major class-resource gate, condition gate, or once-per-battle rule.

## 10. Break / Stagger numbers

### Break Gauge targets

| Enemy tier | Typical Break Max |
| --- | ---: |
| fragile normal | 40-45 |
| normal | 50-60 |
| sturdy normal | 65-75 |
| elite | 100-120 |
| first boss initial gauge | 180 |

### Break values by action

| Action | Typical Break |
| --- | ---: |
| ordinary basic hit | 4-6 |
| utility attack | 7-12 |
| dedicated Break skill | 18-28 |
| major Break spender | 30-40 |
| boss hard-CC conversion | usually 15-30 |

### Break recovery

After a target **successfully completes** a Natural Turn:
- recover **8% of Break Max**;
- no recovery if that action was cancelled by a valid Break/interrupt before completion;
- Break Gauge cannot exceed current maximum.

### Break event

On reaching 0:
- cancel an in-progress action only if tagged Breakable;
- apply `Exposed`;
- normal/elite: +20 TU Delay;
- boss: +10 TU Delay;
- restore Break Gauge to its next maximum.

### Exposed

Prototype baseline:
- **+20% final direct damage taken**;
- **+25% incoming Break damage**;
- lasts for the next **2 eligible direct hits** or until the target completes its next Natural Turn, whichever comes first.

### Repeated boss Break

Within one phase:
- 1st Break Max: 180;
- after first Break: x1.25 -> 225;
- after second: x1.50 -> 270;
- later: cap around x1.75 -> 315.

A major phase transition may reset part/all of this escalation.

## 11. Hard-control repeat resistance

Each hard-control family tracks temporary Repeat Resistance.

Prototype model:
- successful hard-control event: +1 stack for that family;
- max 3 stacks;
- each stack reduces subsequent hard-control buildup/effect from that same family by **25%**;
- after **2 completed Natural Turns** without another successful application of that family, remove one stack;
- phase changes may clear some stacks.

Bosses normally convert hard control rather than suffering raw stored action loss, but Repeat Resistance also reduces conversion efficiency enough to stop one-control spam from being optimal forever.

### Initial boss conversion examples

These are defaults, not overrides for every boss script:
- failed/raw Stun on non-interruptible boss action: +20 Break and up to 8 TU Delay;
- Freeze threshold on boss: +25 Break and up to 10 TU Delay, then Cryomancer-specific Frost/Shatter interaction remains available;
- Root/forced-move attempt on Immovable boss: only gains Break if the skill explicitly has an Immovable conversion clause.

## 12. Threat skeleton

Threat is per enemy.

Each enemy stores:

```text
Threat[player]
```

### Baseline threat generation

- direct damage: +1 Threat per damage dealt to that enemy;
- effective healing: +0.35 Threat per HP actually restored, applied to each living hostile enemy that can observe/participate in the encounter;
- barrier granted: +0.25 Threat per barrier point actually created;
- dedicated tank/protection actions may add explicit flat Threat;
- overhealing and barrier overcap do not generate Threat from wasted value.

### Decay

At the start of each enemy Natural Turn:
- all its stored Threat values decay by **20%**.

### Target score

```text
TargetScore = (100 + Threat) * RowModifier * ClassModifier * TemporaryModifier * AIPreference
```

Prototype modifiers:
- front row: **1.50**;
- back row: **1.00**;
- Knight `Oath of the Line` while front: additional **x1.35**;
- `Challenge/Taunt` for the next eligible direct action: roughly **x4.0** temporary modifier;
- enemy archetypes may apply an AI preference such as x1.8 toward back-row, low-HP, marked, healer, etc.

Default ordinary melee AI targets the legal character with highest TargetScore. Special enemies may use a different declared policy.

Threat never overrides:
- row-wide/AoE actions;
- `Unredirectable` scripted target rules;
- explicit puzzle/phase targeting;
- skills whose identity is to hunt the back row/lowest HP/etc.

## 13. Soft-status resistance

No universal Status Accuracy vs Status Resistance dice roll in the first prototype.

Visible resistance tiers:
- Normal: 100%;
- Resistant: 67%;
- Highly Resistant: 50%;
- Immune: 0% direct status value, with declared fallback where applicable.

For multi-turn states, the resistance normally reduces duration first.
For a one-action/one-charge state, resistance normally reduces potency instead of rounding it to zero.

## 14. First-slice class-resource caps

Keep the already-designed varied resource model.

| Class | Prototype resource baseline |
| --- | --- |
| Knight | Resolve cap 6, start 2 |
| Duelist | Tempo cap 5 |
| Hunter | 1 Prey designation; no mandatory generic Bond bar in first implementation; beast assist frequency is capped separately |
| Marksman | Aim cap 5 |
| Pyromancer | Ash cap 6 |
| Cryomancer | Frost max 5 per target; Cold Front threshold/counter target 3 for first test |
| Priest | Grace cap 5 |
| Oracle | Omen cap 3 |

Important:
- no resource automatically gains +1 every Natural Turn unless that class explicitly needs it after testing;
- no core loop requires enemy kills;
- overcap conversion must be explicit and capped.

## 15. Hunter companion cadence baseline

First test:
- beast has no independent Natural Turn slot;
- at most **1 automatic assist per Hunter Natural Turn cycle**;
- `Coordinated Strike` may include one explicit beast follow-up as part of skill resolution;
- Reaction-triggered beast protection does not also create an offensive assist from the same event;
- `Beast Command` begins around CD 1-2 depending on command strength.

This is intentionally conservative. Companion action frequency can be raised after confirming it does not become a second player character.

## 16. Party-size encounter scaling — first test only

This is not yet a global progression lock. It is the first combat-test scaling curve.

### Boss HP multiplier

| Party size | Boss HP multiplier |
| --- | ---: |
| 1 | 1.00 |
| 2 | 1.75 |
| 3 | 2.40 |
| 4 | 3.00 |

### Boss outgoing damage multiplier

| Party size | Damage multiplier |
| --- | ---: |
| 1 | 1.00 |
| 2 | 1.05 |
| 3 | 1.10 |
| 4 | 1.15 |

Do **not** solve party scaling only with HP.

For 3-4 players, prefer adding:
- another legal target pattern;
- an extra support add;
- wider row pressure;
- additional mechanic responsibility;
- slightly faster phase cadence.

The target is comparable time-to-reward, with party play gaining safety and tactical options rather than fourfold efficiency.

## 17. Values explicitly left Draft

- final class base stats;
- final enemy HP/damage curves;
- exact Crit ecosystem;
- final Speed cap/soft-cap formula for long-term progression;
- exact DoT coefficients and whether late-game gear can scale them separately;
- final Break recovery rate and repeated-boss-break escalation;
- exact Threat coefficients;
- exact Barrier caps in late game;
- final party-size reward scaling.

The formulas and categories above exist so first implementation produces useful playtest evidence. Do not treat them as immutable content balance.
