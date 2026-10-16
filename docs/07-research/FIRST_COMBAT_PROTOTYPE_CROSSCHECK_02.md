# First Combat Prototype — Cross-Check 02

**Status:** Design audit after vocabulary, duration, numeric skeleton, and enemy-set pass
**Date:** 2026-10-16

Scope:
- common status vocabulary;
- duration clocks;
- Speed/timeline rules;
- Break and boss control;
- Threat/formation/protection;
- first numeric skeleton;
- first normal/elite/boss enemy set;
- compatibility with Knight, Duelist, Hunter, Marksman, Pyromancer, Cryomancer, Priest, and Oracle.

## 1. Status identity audit

### Stun / Freeze / Sleep / Break / Delay
**Pass.** They no longer collapse into renamed `lose one turn` effects.

- Stun = immediate interrupt or bounded timeline shove.
- Freeze = thresholded stored action denial on ordinary enemies; boss conversion into Break/Delay/cold setup.
- Sleep = fragile control that ends on damage and creates a wake-hit decision; reserved for later content.
- Delay = direct one-time timeline movement with no duration.
- Break = posture threshold that creates Exposed/timing value and cancels only explicitly Breakable actions.

Risk:
- UI must clearly distinguish current timeline Delay from persistent Slow and from Break-gauge pressure. If all three are represented with similar backward-arrow icons, the mechanical distinction will be lost despite the rules being different.

### Burn / Bleed / Poison
**Pass.** They create different decisions.

- Burn = stackable setup/consumption resource for fire interactions.
- Bleed = end-turn wound pressure amplified by physical exertion/movement.
- Poison = stable longer attrition with one Potency instance.

Risk:
- do not later add another generic `Shadow DoT` that is only Poison with a different damage type.

### Mark / Prey / Exposed
**Strong pass.**

- Exposed = universal short vulnerability window.
- Mark = source-owned setup tag with no universal damage multiplier.
- Prey = Hunter-specific coordinated target designation.

This directly protects Hunter/Marksman separation from the earlier class-kit audit.

## 2. Duration-clock audit

**Pass with one documentation reconciliation note.**

Four clocks cover materially different jobs:
1. Target Natural Turns;
2. Until Source Next Natural Turn;
3. Eligible Event Charges;
4. Timeline Units.

This solves the main continuous-Speed problem:
- fast targets do not receive an arbitrary number of actions under a fixed caster-turn debuff;
- Bonus Actions/Reactions do not accelerate DoT/HoT/cooldowns;
- Guard/Overwatch/Premonition do not need awkward target-turn durations;
- global fields do not expire faster just because more party members exist.

Reconciliation note:
- the earlier Cryomancer draft described `Rime Field` as an action-event field; the new global rule should supersede that open question and use a Timeline-Unit field with a separate event cap if needed.
- the earlier Priest draft left Regeneration clock open; the new default resolves it to Target Natural Turns.

These are Draft class-doc wording mismatches, not mechanical blockers.

## 3. Speed exploit audit

**Pass for first prototype.**

Safeguards now exist on all multiplicative paths:
- narrow expected Speed range;
- hard temporary Speed clamp;
- Haste/Slow scheduling-modifier clamp;
- Delay per-target cap;
- smaller boss Delay cap;
- Advance minimum-distance floor;
- no immediate full Natural Turn grant;
- Bonus Actions/Reactions do not recharge cooldowns;
- Hunter beast assists are capped per Hunter Natural-Turn cycle.

Remaining intentional consequence:
- Speed still improves ordinary action frequency **and** the real-time rate at which owner-turn cooldowns recycle.

This is not currently treated as a bug; it is part of the locked combat model. The prototype must measure whether the chosen Speed band keeps the double benefit healthy.

## 4. Cooldown audit

**Pass.**

`Cooldown N` now has an unambiguous implementation meaning: after use, the skill is unavailable for N future owner Natural Turns. Bonus Actions/Reactions do not count.

Risk:
- UI copy must say the number of unavailable future turns, or show the remaining number directly; avoid tooltips whose wording could imply `usable after N turns including this turn`.

Oracle `Borrowed Moment` remains high-risk even with this definition. It should not be part of the first minimal implementation until normal cooldown pacing is measured.

## 5. Boss-control audit

**Strong pass.**

The boss-control model has three layers instead of binary immunity:
- soft control remains useful at reduced/capped strength;
- hard control converts into Break/Delay/setup value;
- repeated same-family control gains temporary resistance;
- Break itself becomes harder to repeat within a phase.

This preserves Cryomancer, Hunter, Duelist, Knight Break builds and Oracle timeline tools without permitting permanent stun-lock.

Risk:
- if conversion values are too high, players can still achieve a `soft stun-lock` through Break + Delay even without raw Freeze/Stun. The Black Banner Captain is specifically designed to expose this.

## 6. Threat / formation audit

**Pass.**

Threat is per enemy and decays. Front row, Knight identity, temporary Taunt and enemy AI preferences all modify target score rather than becoming absolute target locks.

Prototype enemies deliberately challenge the system:
- Cutthroat follows ordinary Threat;
- Crossbowman prefers Back row;
- Enforcer uses Back-row pressure;
- Captain mixes Threat-respecting direct attacks, row attacks and marked direct attacks.

This should make Knight valuable without making other players untargetable.

Risk:
- exact `damage = 1 threat`, healing/barrier coefficients and Knight multipliers are Draft. AI target telemetry should be logged during implementation so target distribution can be measured rather than guessed.

## 7. Accuracy / status-RNG audit

**Pass for prototype simplification.**

The first prototype does not add universal Accuracy, Evasion, Status Hit and Status Resistance stats simultaneously.

Advantages:
- fewer opaque failures during class-loop testing;
- Marksman precision identity can use deterministic setup rather than generic hit chance;
- Duelist Feint / Marksman Suppression / Cryomancer Whiteout can reduce action effectiveness or secondary potency through explicit states.

Risk:
- the current class drafts still contain words such as `accuracy` in some skill descriptions. They should be interpreted as explicit per-skill `Obscured/Suppressed` behavior, not evidence that a universal Accuracy stat has been locked.

## 8. Numeric-scale audit

**Pass as an implementation baseline, not final balance.**

The scale is intentionally compact:
- player HP roughly 540-760;
- Power roughly 88-112;
- Defense roughly 42-75;
- Speed roughly 90-112 for the first eight;
- ordinary enemy stats live in the same readable order of magnitude.

A single first-prototype `Power` and `Defense` stat avoids prematurely testing an itemization problem instead of a combat-loop problem.

Risk:
- final equipment/class progression may require separate physical/magical/support scaling later. Do not split those stats before combat telemetry demonstrates a real design need.

## 9. Class-by-class audit

### Knight
**Pass.**
- Resolve works without adds or kills.
- ordinary Threat, Back-row hunters, AoE and target-preference exceptions all exist.
- Guard and Intercept have distinct clocks and roles.
- dedicated Break has visible boss value.

Watch:
- party Knight may generate too much Threat from both protection and ordinary damage; measure actual target distribution.

### Duelist
**Pass.**
- intent categories exist on normal, elite and boss actions.
- Feint/Parry can exploit direct actions.
- Shieldman/Chirurgeon provide buff-removal targets.
- Tempo Break obeys global Delay caps.

Watch:
- Duelist and Oracle both manipulate timing. Duelist must remain short-range precision pressure; Oracle owns broader predictive timeline support.

### Hunter
**Pass.**
- Runner creates trap/Overwatch movement triggers.
- Prey is explicitly protected from generic Cleanse.
- boss loop works with one target and no kill requirement.
- companion frequency has a first numerical cap.

Watch:
- if automatic assist frequency feels invisible at low Speed but oppressive at high Speed, use a Timeline-Unit internal cooldown instead of raising the raw per-turn count.

### Marksman
**Pass.**
- back-row priority enemies exist.
- forced movement pressures Aim without making one disruption erase the class.
- Break/Exposed windows reward prepared shots.
- personal Mark does not overlap with Hunter Prey.

Watch:
- do not make Aimed Shot + Exposed + Crit RNG the only competitive payoff. Precision should remain primarily setup-deterministic.

### Pyromancer
**Pass.**
- Captain accepts Burn and lasts long enough to test maintenance vs consumption.
- Ash is not kill-dependent.
- Chirurgeon creates anti-heal and enemy-cleanse interaction.
- Phase adds are optional acceleration/AoE value rather than the resource engine.

Watch:
- Purging Salts must not erase Burn so frequently that Pyromancer becomes useless; support AI cooldown and target priority matter.

### Cryomancer
**Strong pass.**
- normal Runner/Hexer can be meaningfully controlled;
- elite repeat resistance can be observed;
- boss Freeze conversion is explicit;
- Shatter can choose Break/protection value instead of merely cold Combust;
- predictable row attacks give Barrier/Ice Wall value.

Watch:
- Freeze->Break plus Shatter->Break can become the dominant boss-control route if conversion coefficients are too generous.

### Priest
**Pass.**
- Poison, Bleed, Healing Reduction and predictable heavy hits make Cleanse/prevention/rescue distinct.
- Barrier has a real pre-damage use case.
- proactive prevention can generate meaningful Grace.
- there are stable turns where Smite/control can be used instead of healing.

Watch:
- Grace generation from Barrier should count only meaningful prevented damage, not barrier application itself if no damage is ever absorbed.

### Oracle
**Pass with intentional complexity warning.**
- all players receive useful baseline telegraphs;
- Oracle reveals deeper target/secondary/breakability information;
- Delay/Advance are globally bounded;
- enemy buffs/support create manipulation opportunities;
- no class feature requires manual ally turn-order negotiation.

Watch:
- `Borrowed Moment` should remain deferred from the minimal first build.
- Oracle onboarding should stage information layers; displaying every future detail immediately would make the class and UI harder to read than necessary.

## 10. Solo compatibility audit

**Pass by design.**

No first-eight core loop now requires:
- another specific player class;
- enemy death;
- multiple enemies;
- a party-only target;
- a guaranteed hard CC on bosses.

Support/tank classes receive offensive/Break/control paths; damage classes receive enough self-protection/control to progress alone.

The remaining question is efficiency, not logical viability. That can only be settled by simulation/playtest.

## 11. Four-player compatibility audit

**Pass as a first model.**

The prototype uses sublinear boss HP scaling plus composition/mechanic pressure rather than `party size x HP`.

Potential risk:
- four players also bring four separate cooldown pools, resources, Signatures and Reactions. A 3.0x boss-HP multiplier may still be too low if synergy raises effective output far above linear assumptions.

Required telemetry:
- time-to-kill by party size;
- player Natural Turns per kill;
- boss Natural Turns per kill;
- Break count;
- hard-control conversion count;
- damage prevented/healed;
- idle/support turns;
- Signature uses;
- average target distribution.

## 12. Prototype-lock versus Draft boundary

### Locked enough to implement
- the existence and meaning of Natural Turn vs Bonus/Reaction;
- four duration-clock categories;
- Stun / Freeze / Break / Delay distinction;
- Mark / Prey / Exposed distinction;
- Guard / Intercept distinction;
- per-enemy Threat model;
- no universal Accuracy/Evasion/Status Hit contest in the first prototype;
- reciprocal Speed-to-timeline formula as the first implementation model;
- owner-Natural-Turn cooldown semantics;
- boss CC conversion + repeat resistance principle;
- visible Break gauge + repeated-break safeguard;
- first enemy-role set and boss mechanics as test harness requirements.

### Still Draft / expected to change after evidence
- almost every numeric coefficient;
- class base stats;
- Speed bounds;
- Break maxima/recovery;
- Threat coefficients;
- Barrier caps;
- DoT damage;
- boss HP/damage;
- party-size scaling values;
- enemy names/lore;
- exact AI utility scoring;
- exact intent UI depth;
- which future-bank statuses enter the first production region.

## 13. Verdict

**Ready for implementation of the first deterministic combat simulator / playable combat slice.**

No user decision is required before that step. The remaining uncertainties are best answered by executable simulation and play rather than additional abstract design.
