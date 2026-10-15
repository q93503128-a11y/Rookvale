# Turn-Based Combat

**Status:** Core turn rules locked; tactical identity and detailed formulas still open

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
3. After acting, its next-action point advances according to effective Speed and the action's delay/cost.
4. Faster combatants therefore return to the front of the timeline more often.

This allows Speed, slows, haste, heavy skills, quick skills, interrupts, and boss mechanics to interact with one consistent system.

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

- action resources: MP, stamina, AP, cooldowns, charges, or hybrids;
- basic-attack purpose;
- weakness / break / stagger mechanics;
- status effects and cleanses;
- guarding, aggro, protection, interception, and tank identity;
- healer gameplay beyond repeated HP restoration;
- reaction / counter / interrupt mechanics;
- visible future timeline depth;
- action delay differences between quick and heavy abilities;
- death, revival, escape, and wipe rules;
- boss phase structure;
- exact party-size encounter scaling;
- exact Speed formula and soft caps.

## Avoid by default

- simultaneous action selection as the standard combat model;
- manual ally turn-order negotiation as a routine action;
- basic attack spam as the optimal default;
- healer gameplay that is only repeated HP restoration;
- tanks that work only through inflated defense numbers;
- enemies differentiated only by elemental color;
- excessive animation time that makes ordinary encounters tedious;
- party scaling that merely turns enemies into HP sponges.
