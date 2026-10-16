# Combat Status / Timeline / Prototype Research 03

**Status:** Active synthesis research for the first combat prototype
**Date:** 2026-10-16

This pass exists to support the first shared combat vocabulary, duration rules, numerical skeleton, and prototype enemy set. It follows `RESEARCH_POLICY.md`: broad discovery first, then Rookvale-specific synthesis. The purpose is mechanic vocabulary and failure-case detection, not surface copying.

## Research questions

- How can hard CC remain valuable against bosses without enabling permanent turn denial?
- How should Speed, one-shot timeline movement, cooldowns, and status duration interact on a continuous sequential timeline?
- How can Burn / Bleed / Poison / Freeze / Stun / Sleep / Silence / Disarm avoid becoming renamed copies of each other?
- How should Break differ from hard CC?
- How should threat, guard, interception, marks, and vulnerability states remain readable?
- What status clocks are least exploitable when fast characters receive more natural turns?

## Discovery pool

### 1. Octopath Traveler — shield Break
Useful lesson:
- weaknesses remove shield points;
- breaking creates a clear payoff window and denies actions;
- the player can plan toward a visible threshold rather than fish for low-probability control.

Rookvale use:
- visible Break buildup and a payoff window are good;
- Rookvale should not copy the exact shield/weakness-count system or make every Break a full lost round.

Reference:
- https://octopathtraveler.fandom.com/wiki/Octopath_Traveler

### 2. Final Fantasy XIII — stagger as vulnerability state
Useful lesson:
- repeated pressure builds toward Stagger;
- Stagger primarily changes vulnerability and how other actions behave;
- some enemies differ in how easily they reach the state.

Rookvale use:
- Break should create a temporary tactical conversion window, not merely `stun with another icon`.

Reference:
- https://finalfantasy.fandom.com/wiki/Stagger_(Final_Fantasy_XIII)

### 3. Star Renegades — timeline stagger limits
Useful lesson:
- stagger pushes enemy timing;
- enemies have a limited stagger budget;
- the budget recovers after enemy actions, so control must be timed rather than spammed indefinitely.

Rookvale use:
- Break/Delay pressure benefits from per-target caps and recovery after meaningful enemy actions.

Reference:
- https://starrenegades.fandom.com/wiki/How_to_play_guide_for_Star_Renegades

### 4. Etrian Odyssey — accumulative resistance and Binds
Useful lesson:
- repeated successful ailments/binds create accumulative resistance;
- later entries let that added resistance wear off after enough turns;
- Binds disable categories of abilities/stat functions rather than simply deleting a turn.

Rookvale use:
- repeated hard CC should create temporary family-specific resistance;
- Silence / Disarm / Root can restrict capability instead of copying Stun.

References:
- https://etrian.fandom.com/wiki/List_of_Status_Effects
- https://etrian.fandom.com/wiki/Bind

### 5. Darkest Dungeon — anti-stunlock resistance
Useful lesson:
- Stun removes a turn;
- recovering from Stun grants temporary additional Stun resistance;
- Guard and Mark are mechanically distinct states rather than generic defense/damage buffs.

Rookvale use:
- successful hard control should make the same family harder to repeat;
- Guard should be explicit redirection;
- Mark should be a tag consumed by particular skills, not automatically `take more damage`.

References:
- https://darkestdungeon.wiki.gg/wiki/Stun_(Darkest_Dungeon)
- https://darkestdungeon.wiki.gg/wiki/Guard
- https://darkestdungeon.wiki.gg/wiki/Mark

### 6. Monster Hunter — buildup thresholds and escalating status resistance
Useful lesson:
- ailments build toward thresholds;
- buildup can decay;
- after an ailment triggers, the next threshold rises;
- paralysis, poison, and sleep have very different consequences.

Rookvale use:
- boss/elite control can use visible or inspectable buildup/resistance rather than binary immunity;
- repeated successful hard CC becomes progressively more expensive;
- status names should imply genuinely different decisions.

Reference:
- https://www.monsterhunterwiki.org/wiki/Status_Effects_(MHRS)

### 7. Grandia — initiative bar and cancellable preparation
Useful lesson:
- units move on a shared initiative bar;
- after choosing an action there can be a preparation interval;
- attacks during that interval can cancel the prepared move.

Rookvale use:
- `Stun/Interrupt` is most distinct when it interacts with interruptible telegraphs/preparation rather than always creating a stored skipped turn.

Reference:
- https://grandia.fandom.com/wiki/IP_bar

### 8. Child of Light — timeline cast section / interrupt
Useful lesson:
- different actions have different cast times;
- being hit while casting can interrupt and move the actor backward on the timeline;
- Slow and Paralysis visibly alter timeline movement.

Rookvale use:
- action-specific delay and one-shot Delay effects should be first-class concepts;
- not every control state needs to modify the Speed stat itself.

Reference:
- https://childoflight.fandom.com/wiki/Battle

### 9. Honkai: Star Rail — continuous action value
Useful lesson:
- faster units naturally act more often;
- Action Value can be represented as distance-to-next-turn, commonly explained as `10000 / Speed` before other modifiers.

Rookvale use:
- a reciprocal Speed-to-delay formula is transparent and matches the already-locked continuous next-action model;
- Rookvale keeps a much narrower Speed range and stricter timeline-pull caps.

Reference:
- https://www.hoyolab.com/article/19822028

### 10. Epic Seven — combat-readiness manipulation
Useful lesson:
- Speed and direct turn-bar movement are separate concepts;
- combat readiness can move a unit forward/back without permanently changing Speed;
- some bosses resist backward manipulation.

Rookvale use:
- `Haste/Slow` and `Advance/Delay` should be separate vocabulary.

Reference:
- https://epic7x.com/combat-readiness-tutorial/

### 11. Summoners War — target-turn status processing
Useful lesson:
- start-of-turn status effects resolve before the action;
- inability effects can skip the action;
- timed buffs/debuffs count down on the affected unit's turn.

Rookvale use:
- a target-natural-turn clock is readable for effects intended to cover a fixed number of that target's actions;
- skipped natural turns must still have a well-defined start/end boundary so durations do not freeze forever.

Reference:
- https://summonerswar.fandom.com/wiki/Turn_Order

### 12. Crystal Project — explicit per-enemy threat
Useful lesson:
- threat is tracked per enemy;
- damage/healing can affect it;
- threat decays on enemy turns;
- dedicated abilities can directly manipulate it.

Rookvale use:
- per-enemy threat is preferable to one global aggro number;
- front/back formation and AI preferences should modify target score rather than make targeting absolute.

Reference:
- https://crystal-project.fandom.com/wiki/House_of_The_Know-It-All_Ducks

### 13. Persona 5 — ailments as combo states
Useful lesson:
- ailments such as Burn, Shock, Freeze, Sleep, Fear, etc. can enable different Technical follow-ups rather than only dealing damage or skipping a turn.

Rookvale use:
- status identity should include interaction vocabulary and setup/payoff, not just damage color.

Reference:
- https://megamitensei.fandom.com/wiki/Technical

### 14. Pokemon — major statuses are not synonyms
Useful lesson:
- Burn, Poison, Paralysis, Sleep, and Freeze differ in damage, stat pressure, action denial, persistence, and removal rules;
- some statuses interact with elemental attacks or specific counters.

Rookvale use:
- Burn/Bleed/Poison and Stun/Freeze/Sleep must have different tactical answers and timing.

Reference:
- https://bulbapedia.bulbagarden.net/wiki/Status_condition

### 15. Divinity: Original Sin 2 — useful negative example
Useful lesson:
- physical/magic armor can block large families of disabling states until the corresponding armor is removed.

Risk for Rookvale:
- a binary `armor exists -> control does nothing` layer can invalidate control-heavy classes until a separate damage race is won;
- this is especially dangerous for Cryomancer / Oracle / Hunter utility and for solo builds.

Rookvale rejection:
- do not put all CC behind one universal binary armor gate.
- use Break, family resistance, conversion, and diminishing returns instead.

Reference:
- https://divinity.fandom.com/wiki/Physical_and_Magical_Armor_(Original_Sin_2)

### 16. SaGa Scarlet Grace — turn-order manipulation as tactical objective
Useful lesson:
- visible order and manipulation can be a core tactical problem rather than hidden math;
- changing order can create combo opportunities.

Rookvale use:
- timeline information should be visible enough that Delay/Advance/Prediction choices can be planned.

Reference:
- https://www.square-enix-games.com/en_US/news/introduction-to-saga

## Synthesis decisions

### A. Do not use one universal CC system

Rookvale separates:
- **interrupt control** — Stun / explicit interrupt;
- **stored action denial** — Freeze / Sleep, each with different setup and break rules;
- **capability restriction** — Silence / Disarm / Root;
- **timeline pressure** — Slow / Haste / Delay / Advance;
- **posture pressure** — Break;
- **vulnerability** — Exposed;
- **source-owned setup tags** — Mark / Prey.

This keeps class identities separated.

### B. Use four duration clocks, each for a different job

1. **Target Natural Turns** — effects meant to affect a fixed number of the target's own actions.
2. **Until Source Next Natural Turn** — prepared windows such as Guard, Overwatch, Riposte setup, Premonition.
3. **Eligible Event Charges** — barriers, guard hits, rescue triggers, predictive wards.
4. **Timeline Units** — battlefield fields / encounter states that must not become shorter merely because the party has more members.

Bonus actions and Reactions are not natural-turn boundaries.

### C. Boss CC uses conversion + resistance, not immunity-only design

- bosses normally reject raw stored turn-loss from Freeze/Sleep;
- the same control attempt still contributes Break, bounded Delay, vulnerability setup, or telegraph interruption where appropriate;
- repeated use of the same hard-control family becomes less efficient until the boss gets meaningful actions again;
- designated boss windows may temporarily allow stronger control conversion.

### D. Break is a posture system, not another Stun

Break should:
- use a visible gauge;
- be built by many classes at different rates;
- cancel only explicitly breakable prepared actions;
- create a short Exposed window;
- push the next action by a bounded amount;
- recover/strengthen after repeated breaks so permanent control is impossible.

### E. Status application is mostly deterministic in the first prototype

Rookvale should avoid stacking Hit Chance, Status Chance, Status Accuracy, Evasion, and Status Resistance into opaque probability layers during the first prototype.

Initial direction:
- legal direct attacks hit by default;
- soft statuses apply deterministically unless immunity/resistance rules say otherwise;
- hard control uses buildup / conversion / diminishing-return rules;
- explicit Evasive / Obscured / Precise states may exist without a universal Accuracy stat.

## Rejected alternatives

### Every status lasts `N rounds`
Rejected because Rookvale has no simple round reset and Speed can produce unequal natural-turn counts.

### Every status lasts `N caster turns`
Rejected as a global rule because very fast/slow targets can then receive wildly different numbers of actions under the same effect.

### Every status lasts `N target turns`
Useful as the default for action-bound states, but rejected as the only clock because Guard, barriers, predictive effects, and fields are more readable as event charges or timeline windows.

### All hard CC becomes Break on every enemy
Rejected because normal enemies would lose status identity. Normal enemies can still be Frozen, Slept, Silenced, Disarmed, etc.; elites/bosses convert more aggressively.

### Accuracy/Evasion as full baseline attributes
Rejected for the first prototype. Too much miss RNG would obscure whether class rotations and numeric coefficients are actually working.

## Implementation consequence

The concrete Rookvale rules derived from this research are recorded in:
- `docs/01-gameplay/COMBAT_VOCABULARY.md`
- `docs/01-gameplay/PROTOTYPE_NUMBERS.md`
- `docs/01-gameplay/PROTOTYPE_ENEMIES.md`

All values remain prototype-tunable unless the relevant document explicitly marks a rule as locked.
