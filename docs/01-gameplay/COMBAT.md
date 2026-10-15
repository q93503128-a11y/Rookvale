# Turn-Based Combat

**Status:** Core turn, action, cooldown, formation, AFK, and party-size rules locked; formulas and advanced combat identity still open

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
- The exact mathematical Speed formula is not locked yet. Speed progression must be deliberately compressed compared with damage/HP progression so late-game stat inflation does not create absurd turn-frequency multiplication.

### Preferred implementation model

Use a continuous initiative / next-action timeline rather than a simple round reset.

Conceptually:

1. Every combatant has a next-action point on the timeline.
2. The combatant with the earliest point acts.
3. After acting, its next-action point advances according to effective Speed and any action-specific delay/cost rules.
4. Faster combatants therefore return to the front of the timeline more often.

This allows Speed, slows, haste, interrupts, heavy/quick skills, and boss mechanics to interact with one consistent system.

## Action economy

- A normal turn grants **one standard action**.
- A standard action is normally one skill, basic attack, item use, defend action, or another full combat command.
- Special mechanics may grant bonus actions, free actions, follow-ups, reactions, counters, or other exceptions.
- These exceptions must be explicitly tagged rather than silently treated as ordinary turns.
- Routine multi-action AP turns are not the default combat model; this keeps multiplayer turns short and readable.

### Bonus-action safeguard

Special effects that grant an additional action should be distinguishable from a naturally earned full timeline turn.

Initial design preference:

- a **natural Speed-earned turn** is a full turn and processes normal turn-start / turn-end systems;
- a **bonus/free action** does not automatically count as another full turn for every cooldown, duration, regeneration, or damage-over-time system.

This prevents action-granting skills from accidentally accelerating every other temporal mechanic and creating recursive extra-action chains. Exact exception rules remain to be tested.

## Skill cooldowns

Rookvale uses **turn-based skill cooldowns**.

- Stronger or more specialized abilities may become unavailable for a stated number of turns after use.
- Basic or low-impact skills may have no cooldown.
- Cooldown reduction/increase can become a legitimate class, equipment, status, or boss mechanic.
- The interface must show remaining cooldown clearly before the player selects a skill.

### Speed interaction — important balance constraint

Because Speed can grant more full turns, a cooldown that decreases on the user's own turns also makes Speed accelerate skill recycling. This is potentially desirable, but it makes Speed multiplicative: it improves action frequency **and** access to cooldown skills.

Current preferred rule to prototype:

- cooldowns decrease on the owner's **natural full turns**;
- Speed-earned extra turns therefore legitimately recharge skills faster;
- special bonus/free actions do **not** automatically tick cooldowns unless a skill explicitly says otherwise;
- Speed growth, cooldown lengths, haste effects, cooldown reduction, and extra-action effects must be balanced together rather than independently.

This rule is not a promise that every temporal effect uses the same clock. Buffs, debuffs, damage-over-time, regeneration, and boss timers need separate explicit rules later.

## Front / back formation

Combat uses a simple **front row / back row** formation for both tactical readability and class-role value.

### Core rules

- Party members occupy either the front row or back row.
- Front-row characters have a **higher default enemy target weight**.
- Back-row characters are safer by probability, not absolutely protected.
- Enemies may still target the back row when their AI, skill, role, or tactical condition calls for it.
- Taunt/provoke and other threat-control effects may override or heavily modify normal target weighting.
- Formation should make tanks meaningful without reducing tank gameplay to raw Defense alone.

### Design intent

The front row should create protection through **risk concentration**, not an invulnerability wall.

Examples of future mechanics that fit this model:

- tank skills that raise personal threat or intercept attacks;
- enemies that deliberately hunt healers or low-HP targets;
- ranged attacks that favor back-row targets;
- cleaves that hit one row;
- guard effects that redirect a specific ally's incoming attack;
- displacement effects that move a unit between rows;
- class skills whose power or target access changes by row.

Not every normal attack must be restricted to the opposing front row. Hard target locks should be skill-specific where useful rather than a universal rule.

## Turn time limit

- Standard player turn limit: **20 seconds** for the initial implementation.
- The limit is a gameplay safeguard, not a target turn duration; normal turns should usually resolve much faster.
- The timer may later vary for special encounters or accessibility options if testing justifies it.

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

- Encounter scaling must consider party size.
- Do not rely only on HP multiplication; scale enemy composition, action pressure, target coverage, mechanics, or boss responses where appropriate.
- A four-player party should gain tactical flexibility and safety, not approximately four times the progression efficiency.
- Normal rewards should be designed around comparable time-to-reward across viable party sizes.
- Loot/reward ownership should avoid social friction such as one player consuming another player's progression reward; exact reward rules remain open.
- Some explicitly labeled group content may require or strongly favor parties, while ordinary exploration and main progression must remain solo-capable.
- Every class path must retain a viable solo progression route even if its optimal multiplayer role is tanking, healing, support, or control.

## Design goals

- Faster and more readable than a menu-heavy traditional JRPG battle.
- Deep enough that class roles and party composition matter.
- Support healing and support as genuinely useful play styles.
- Reward tactical decisions rather than pure stat checks.
- Make enemies mechanically distinct, not just differently sized health bars.
- Remain understandable on desktop, mobile, and Roblox UI layouts.
- Leave room for strong animation, impact, and boss presentation despite being turn-based.

## Tactical identity still to decide

External research must continue before locking the systems below:

- MP, mana, stamina, class resources, charges, and resource recovery;
- exact cooldown semantics and typical cooldown lengths;
- basic-attack purpose;
- weakness / break / stagger mechanics;
- status effects and cleanses;
- exact threat/aggro formula and taunt behavior;
- protection, interception, guarding, and tank identity beyond target weight;
- healer gameplay beyond repeated HP restoration;
- reaction / counter / interrupt mechanics;
- visible future timeline depth;
- action delay differences between quick and heavy abilities;
- formation changes and whether moving rows consumes a full action;
- death, revival, escape, and wipe rules;
- boss phase structure;
- exact party-size encounter scaling;
- exact Speed formula, diminishing returns, and soft caps.

## External-reference notes

- **Etrian Odyssey:** useful reference for front-row target pressure and keeping fragile characters safer in the rear. Rookvale should avoid making the back row universally untargetable.
- **Darkest Dungeon:** useful reference for making formation tactically meaningful through skill targeting and position-dependent abilities. Rookvale currently uses a simpler two-row model rather than four exact ranks.
- **Epic Seven and similar turn-based RPGs:** useful reference for readable turn-count cooldowns, cooldown reduction/increase effects, and speed-driven turn frequency.
- **Darkest Dungeon II:** useful reference for separating extra/free actions from full turns so extra actions do not automatically process every start/end-of-turn effect or cooldown system.

## Avoid by default

- simultaneous action selection as the standard combat model;
- manual ally turn-order negotiation as a routine action;
- AP-heavy routine turns where every player chains many ordinary actions;
- basic attack spam as the optimal default;
- healer gameplay that is only repeated HP restoration;
- tanks that work only through inflated defense numbers;
- a universal rule that makes back-row units impossible to target while any front-row unit lives;
- enemies differentiated only by elemental color;
- excessive animation time that makes ordinary encounters tedious;
- party scaling that merely turns enemies into HP sponges.
