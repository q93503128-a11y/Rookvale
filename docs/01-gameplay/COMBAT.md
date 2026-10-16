# Turn-Based Combat

**Status:** Core turn/action/cooldown/formation rules locked; first status, duration, timeline, Break, Threat, formula, and enemy prototype specified; final production balance remains open

## Confirmed requirements

- Combat is turn-based and supports both solo play and multiplayer parties.
- Standard party size is **1 to 4 players**.
- Solo must remain a first-class way to play. A 4-player party may be safer and gain more tactical options, but must not become overwhelmingly more efficient than solo play by default.
- Multiplayer combat is entered by a formed party. Public/world-boss participation may use separate rules later.

## Core turn model

Rookvale uses a **sequential speed-based timeline**.

- Characters and enemies act one at a time.
- Turn order is determined by Speed and the combat timeline.
- Speed affects **how often** a combatant receives turns, not merely who acts first.
- A sufficiently fast combatant can receive two or, in extreme builds, more turns before a much slower combatant acts again.
- There is no manual ally turn-order swapping by default. This avoids added communication requirements and extra decision delay in multiplayer.
- Speed progression must be deliberately compressed compared with damage/HP progression so late-game stat inflation does not create absurd turn-frequency multiplication.

### Prototype implementation model

Use a continuous initiative / next-action timeline rather than a simple round reset.

Conceptually:

1. Every combatant has a next-action point on the timeline.
2. The combatant with the earliest point acts.
3. After acting, its next-action point advances according to effective Speed and any action-specific delay/cost rules.
4. Faster combatants therefore return to the front of the timeline more often.

First implementation formula:

```text
StandardDelayTU = 10000 / EffectiveSpeed
NextActionTime = CurrentTime + StandardDelayTU * ActionDelayMultiplier * TempoModifier
```

At Speed 100, a standard-delay action therefore schedules the next Natural Turn about 100 Timeline Units later.

This exact constant and late-game Speed curve remain tunable. The continuous reciprocal model is the prototype contract.

See `PROTOTYPE_NUMBERS.md` for initial Speed bands, quick/heavy action-delay multipliers, Haste/Slow bounds, and Delay/Advance caps.

## Action economy

- A normal timeline-earned turn is a **Natural Turn** and grants **one standard action**.
- A standard action is normally one skill, basic attack, item use, Defend action, or another full combat command.
- Special mechanics may grant bonus actions, free actions, follow-ups, reactions, counters, or other exceptions.
- These exceptions must be explicitly tagged rather than silently treated as ordinary turns.
- Routine multi-action AP turns are not the default combat model; this keeps multiplayer turns short and readable.

### Bonus-action and Reaction safeguard

A **Natural Turn** processes normal turn-start / turn-end systems.

A **Bonus/Free Action** or **Reaction** does not by default:
- tick ordinary skill cooldowns;
- decrement Target-Natural-Turn durations;
- trigger ordinary DoT/HoT ticks;
- grant natural-turn resource recovery;
- recursively trigger another Reaction.

This prevents action-granting skills from accelerating every temporal mechanic and creating recursive extra-action chains.

## Skill cooldowns

Rookvale uses **owner-Natural-Turn skill cooldowns**.

When a skill with `Cooldown N` is used:
1. set remaining cooldown to N;
2. on each future owner Natural Turn, the skill is unavailable while remaining cooldown is above 0;
3. at the end of that Natural Turn, reduce remaining cooldown by 1;
4. Bonus/Free Actions and Reactions do not reduce the cooldown.

Therefore:
- CD 0 can be used every Natural Turn if other costs allow;
- CD 1 misses one future Natural Turn;
- CD 2 misses two future Natural Turns.

Stronger or more specialized abilities may use longer cooldowns, class resources, conditions, charges, or once-per-battle limits. The interface must show remaining cooldown clearly before selection.

### Speed interaction — important balance constraint

Because Speed grants Natural Turns more often, it legitimately makes owner-turn cooldown skills recycle faster in real timeline time.

This double benefit is intentional in the prototype, but is controlled through:
- compressed Speed ranges;
- Haste/Slow bounds;
- class resources that do not automatically regenerate every Natural Turn by default;
- Delay/Advance caps;
- cooldown floors and anti-loop rules;
- no immediate full-turn grants in the first slice.

The prototype must measure whether this remains healthy before final production Speed curves are locked.

## Status and duration architecture

The canonical first-prototype vocabulary is `COMBAT_VOCABULARY.md`.

Major distinctions include:
- `Stun` = interrupt/bounded shove, not generic stored turn skip;
- `Freeze` = thresholded stored action denial on normal enemies with boss Break/Delay conversion;
- `Break` = posture threshold and vulnerability window, not another Stun icon;
- `Slow/Haste` = future scheduling modifiers;
- `Delay/Advance` = one-shot movement of the already-scheduled next action;
- `Exposed` = universal short vulnerability;
- `Mark` = source-owned setup tag;
- `Prey` = Hunter-specific coordinated designation;
- `Guard` = proactive prepared redirection;
- `Intercept` = out-of-turn Reaction redirection.

### Duration clocks

Timed effects explicitly choose one clock instead of forcing every mechanic into one ambiguous `turn` definition:

1. **Target Natural Turns** — ordinary DoT/HoT, Silence/Disarm, many buffs/debuffs.
2. **Until Source Next Natural Turn** — Guard, Overwatch, Riposte preparation, Premonition and similar prepared windows.
3. **Eligible Event Charges** — barriers, protection hits, predictive wards, rescue triggers.
4. **Timeline Units** — battlefield fields, encounter windows and global timers that must not expire faster merely because a party has more actors.

Bonus/Free Actions and Reactions do not advance Natural-Turn durations by default.

## Break / boss-control model

Rookvale uses a visible **Break Gauge** in the first prototype.

Break pressure can come from dedicated Break attacks, interruption/control conversions, weapon/class mechanics, and encounter interactions.

When Break reaches zero:
- an in-progress action is cancelled only if it is explicitly **Breakable**;
- the target receives a bounded one-shot Delay;
- the target becomes **Exposed** for a short payoff window;
- its Break Gauge rebuilds.

Elites/bosses become harder to Break repeatedly during the same phase. Hard-control families also build temporary repeat resistance.

This means bosses do not rely on blanket CC immunity:
- Stun can interrupt eligible windups, otherwise it can convert into limited Break/Delay;
- Freeze converts into Break/Delay/cold setup rather than repeatedly deleting boss turns;
- movement control against immovable bosses only gains fallback value when the skill explicitly defines such a conversion.

Exact first-test values live in `PROTOTYPE_NUMBERS.md`.

## Front / back formation

Combat uses a simple **front row / back row** formation for both tactical readability and class-role value.

### Core rules

- Party members occupy either the front row or back row.
- Front-row characters have a **higher default enemy target weight**.
- Back-row characters are safer by probability, not absolutely protected.
- Enemies may still target the back row when their AI, skill, role, or tactical condition calls for it.
- Taunt/provoke and other threat-control effects heavily modify normal target weighting without becoming universal mind control.
- Formation should make tanks meaningful without reducing tank gameplay to raw Defense alone.

### Threat model

Threat is stored **per enemy, per player character**.

Prototype direction:
- damage, effective healing/barriers, protection actions, and explicit tank skills can generate Threat;
- each enemy's Threat values decay on its own turns;
- targeting uses Threat together with row modifiers, class modifiers, temporary Taunt/Challenge modifiers, and enemy-specific AI preferences;
- scripted Area, Unredirectable, phase, backline-hunter, low-HP-hunter, or other declared actions may ignore or outweigh ordinary Threat.

The first numeric coefficients are intentionally Draft and live in `PROTOTYPE_NUMBERS.md`.

### Design intent

The front row creates protection through **risk concentration**, not an invulnerability wall.

Examples supported by the system:
- tank skills that raise personal Threat or Intercept attacks;
- enemies that deliberately hunt healers or low-HP targets;
- ranged attacks that favor Back-row targets;
- cleaves that hit one row;
- Guard effects that redirect a specific ally's incoming attack;
- displacement effects that move a unit between rows;
- class skills whose power or target access changes by row.

Not every normal attack is restricted to the opposing Front row. Hard target locks are skill-specific where useful rather than universal.

## Damage / healing / barrier prototype

The first implementation deliberately uses a compact numerical skeleton rather than final itemization complexity.

Prototype direct-damage form:

```text
RawDamage = Power * SkillCoefficient
DefenseMultiplier = 100 / (100 + EffectiveDefense)
FinalDamage = floor(RawDamage * DefenseMultiplier * FinalDamageModifiers * CritModifier)
```

Prototype healing:

```text
RawHeal = Power * HealCoefficient
FinalHeal = floor(RawHeal * HealingDoneModifier * HealingReceivedModifier)
```

Important first-slice simplifications:
- one `Power` scale can drive damage/healing/barriers through different coefficients;
- one `Defense` stat handles first-prototype mitigation;
- no random damage variance;
- no universal Accuracy/Evasion or Status-Hit/Status-Resistance stat contest;
- legal attacks hit by default unless an explicit state/mechanic changes the result;
- barriers absorb post-mitigation incoming damage and use global stacking caps;
- soft-status resistance is a visible potency/duration tier rather than an opaque hit-chance duel.

These are prototype simplifications, not promises about final equipment stats.

## First prototype enemy test harness

`PROTOTYPE_ENEMIES.md` defines the first encounter set:
- baseline melee;
- Back-row attacker;
- defensive Guard/Barrier enemy;
- very fast movement enemy;
- status user;
- healer/support;
- mixed-pressure Elite;
- three-phase Boss.

The set is explicitly designed to test all first-eight class loops, including single-boss resource compatibility, Threat exceptions, Guard/Intercept, Break, Burn, Chill/Freeze conversion, Cleanse/Dispel, Barrier/healing, intent prediction, Mark/Prey, companion frequency, Reactions and Signatures.

Enemy names/lore and final coefficients are not production locks.

## Turn time limit

- Standard player turn limit: **20 seconds** for the initial implementation.
- The limit is a gameplay safeguard, not a target turn duration; normal turns should usually resolve much faster.
- The limit may later vary for special encounters or accessibility options if testing justifies it.

## Idle / AFK handling

- First consecutive timeout: automatically **Defend** and end the turn.
- Second consecutive timeout: mark the player as AFK and enable temporary AI control.
- While AFK, the AI makes conservative legal actions so one inactive player cannot indefinitely stall or completely sabotage the party.
- When the player provides input again, direct control resumes from the player's next eligible turn.
- AFK AI must not be intentionally stronger than competent human play.

## Disconnect handling

- A disconnected player is not immediately removed from an active combat.
- Temporary AI control takes over while the player is disconnected.
- The combat session keeps a reconnect window and allows the player to reclaim the character after reconnecting.
- Server-authoritative combat state is required so one client's disconnect, stale state, or delayed packet cannot freeze the battle.
- Exact reconnect timeout and behavior after an extended absence remain to be decided.

## Solo versus party balance

Party play should provide cooperation and role synergy without making solo progression obsolete.

Design rules:
- encounter scaling must consider party size;
- do not rely only on HP multiplication; scale enemy composition, action pressure, target coverage, mechanics, or boss responses where appropriate;
- a four-player party should gain tactical flexibility and safety, not approximately four times the progression efficiency;
- normal rewards should be designed around comparable time-to-reward across viable party sizes;
- loot/reward ownership should avoid social friction such as one player consuming another player's progression reward; exact reward rules remain open;
- some explicitly labeled group content may require or strongly favor parties, while ordinary exploration and main progression must remain solo-capable;
- every class path must retain a viable solo progression route even if its optimal multiplayer role is tanking, healing, support, or control.

The first boss test uses sublinear HP multipliers plus additional composition/mechanic pressure for larger parties. Exact values are Draft and must be replaced by telemetry after simulation/playtest.

## Design goals

- Faster and more readable than a menu-heavy traditional JRPG battle.
- Deep enough that class roles and party composition matter.
- Support healing and support as genuinely useful play styles.
- Reward tactical decisions rather than pure stat checks.
- Make enemies mechanically distinct, not just differently sized health bars.
- Remain understandable on desktop, mobile, and Roblox UI layouts.
- Leave room for strong animation, impact, and boss presentation despite being turn-based.

## Still open after the first prototype specification

External research and testing are still needed before final production locks for:
- final long-term Speed progression, soft caps and equipment scaling;
- final damage/healing/Defense/stat split for itemization;
- weakness / resistance / elemental-damage architecture beyond first status interactions;
- basic-attack purpose across every class/weapon family;
- visible future timeline depth and exact intent UI;
- whether voluntary row movement consumes a standard action globally or is only skill/context driven;
- death, downed, revival, escape and wipe rules;
- final party-size encounter/reward scaling;
- final Threat coefficients and detailed enemy utility scoring;
- final Break recovery/escalation coefficients;
- PvP-specific status/CC policy if PvP is ever added;
- exact reconnect timeout and extended-disconnect behavior.

## External-reference notes

The detailed research record is `docs/07-research/COMBAT_STATUS_PROTOTYPE_RESEARCH_03.md`.

Key principles currently retained:
- **Etrian Odyssey / Darkest Dungeon / Monster Hunter:** repeated hard control should become harder rather than support effortless permanent lockdown.
- **Octopath Traveler / Final Fantasy XIII:** building toward a visible Break/Stagger threshold can create a planned vulnerability window.
- **Grandia / Child of Light / Star Renegades:** visible timeline movement, interruptible preparation and bounded stagger/delay create control without needing every control effect to be a turn skip.
- **Crystal Project:** per-enemy Threat can make protection/target manipulation explicit and measurable.
- **Divinity: Original Sin 2:** useful negative example; do not put all control behind a binary universal armor gate that makes control classes irrelevant until another resource is stripped.
- **Darkest Dungeon II:** useful reference for separating extra/free actions from full turns so extra actions do not automatically process every start/end-of-turn effect or cooldown system.

## Avoid by default

- simultaneous action selection as the standard combat model;
- manual ally turn-order negotiation as a routine action;
- AP-heavy routine turns where every player chains many ordinary actions;
- basic attack spam as the optimal default;
- healer gameplay that is only repeated HP restoration;
- tanks that work only through inflated Defense numbers;
- a universal rule that makes Back-row units impossible to target while any Front-row unit lives;
- enemies differentiated only by elemental color;
- excessive animation time that makes ordinary encounters tedious;
- party scaling that merely turns enemies into HP sponges;
- blanket boss CC immunity that deletes control-class identity;
- differently named status icons whose only real effect is `lose one turn`;
- unrestricted Delay/Advance/Haste loops that create effective infinite turns.
