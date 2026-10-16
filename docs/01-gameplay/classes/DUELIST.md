# Duelist

**Status:** Draft for review and prototype; not locked

**Lineage:** Armsman -> Duelist

**Primary role:** Precision melee damage / counterplay / tempo control

**Secondary roles:** Soft control, anti-buff pressure, row manipulation, evasive solo play

## Class fantasy

Duelist wins by reading an opponent, choosing when to commit, and turning enemy intent into openings. It is not a generic fast swordsman and not a tank with lower armor.

The Duelist should feel strongest when the player predicts correctly, but wrong reads must cost tempo rather than make the class unplayable.

## Weapon compatibility

Inherited Armsman pool, narrowed toward finesse:
- one-handed blades;
- rapiers/fencing weapons as visual subtypes of the blade family;
- selected light spears where a future branch justifies them;
- buckler/light off-hand defensive equipment where supported.

Heavy shields and heavy blunt specialization are not part of the core Duelist identity.

## Innate mechanic — Tempo

Prototype cap: **5 Tempo**.

Gain Tempo from meaningful precision events:
- landing a skill on a target whose intent/category was correctly read;
- successful Reaction parry/riposte;
- exploiting an Exposed/Open target;
- selected skills may generate Tempo without needing a perfect read so solo rotation never stalls.

Spend Tempo on stronger counters, feints, action-delay pressure, and precision finishers.

Tempo does not regenerate automatically every natural turn.

## Innate passive — Measure the Opponent

At the start of the Duelist's natural turn, one currently visible enemy intent is highlighted with a broad category such as:
- direct attack;
- support/buff;
- control/debuff;
- defensive action;
- special/uncertain.

The Duelist does not receive perfect script knowledge. Boss mechanics may deliberately remain partially obscured.

Correctly exploiting the revealed category can grant Tempo or strengthen selected skills.

# Active skill pool

## 1. Testing Thrust
**Type:** Attack / setup

Reliable low-cooldown strike. If used against the currently read enemy, gain 1 Tempo.

**Technique candidates**
- **Probe the Guard** — lower damage; weakens enemy protection/block.
- **Quick Measure** — lower damage; improves the next intent read.
- **Needlepoint** — higher single-target precision but loses Tempo generation.

## 2. Feint
**Type:** Setup / debuff

Apply Feinted to one enemy. Its next direct attack has reduced accuracy/effectiveness against the Duelist; if it attacks the Duelist anyway, the Duelist gains Tempo.

Does not consume the enemy's turn by itself.

## 3. Lunge
**Type:** Attack / row movement

Advance toward the front and make a strong attack. Gains bonus effect when moving rows as part of the action.

**Technique candidates**
- **Deep Lunge** — stronger hit, longer cooldown.
- **Passing Lunge** — weaker hit but can target a legal back-row enemy.
- **Guarded Entry** — reduced damage, gain short defensive state.

## 4. Disengage
**Type:** Attack / reposition

Strike and move toward the back row. Sets up ranged-safe or counter-oriented play without granting an extra turn.

## 5. Disarm
**Type:** Attack / soft control

Modest damage plus reduced effectiveness for the target's next weapon-tagged/direct physical action. Against bosses, contributes Break instead of fully disabling major attacks.

## 6. Riposte Stance
**Type:** Preparation

Prepare a stronger Reaction window until the Duelist's next natural turn. The equipped Reaction gains improved potency/condition handling.

This is an active setup, not a second automatic action economy.

## 7. Opening Cut
**Type:** Attack / exploit

Deal bonus damage to Feinted, Exposed, recently interrupted, or buff-stripped targets.

Purpose: convert tactical setup into damage.

## 8. Sever Advantage
**Type:** Attack / anti-buff

Strike and remove or weaken one removable positive combat effect. Against targets with no removable effect, instead apply a small vulnerability so the skill is not dead.

## 9. Tempo Break
**Type:** Resource spender / timeline pressure

Spend 2 Tempo to push the target's next-action point later by a bounded amount. Bosses receive reduced delay plus Break contribution.

Cannot chain-lock enemies and does not erase an already-triggered action.

## 10. Flourish
**Type:** Self-buff / resource conversion

Spend Tempo to gain a short event-based precision buff affecting the next 1-2 suitable attacks rather than a long Speed multiplier.

## 11. Cross Step
**Type:** Utility / row interaction

Swap position with an ally in the same or adjacent row when legal and gain a small defensive/evasive benefit. Useful for fixing disrupted formation without becoming a party tank.

## 12. Punishing Point
**Type:** Attack / counter-conversion

Strong strike whose effect scales from successful parry/riposte events since the Duelist's previous natural turn.

## 13. Duel Mark
**Type:** Mark / pressure

Mark one enemy as the Duelist's chosen opponent. Attacks against that target gain precision utility; attacking other enemies provides less Tempo value while the mark persists.

This is a self-build marker, not a party-wide mandatory damage mark.

## 14. Final Measure
**Type:** Finisher

Spend 3-5 Tempo for a committed strike. Extra effects depend on setup rather than missing-HP execution alone: stripped buff, Feinted, Open, interrupted, or correctly read intent.

# Reaction candidates

## Riposte
After an eligible direct melee attack targets the Duelist, retaliate with a modest strike if the Duelist is not hard-controlled.

## Perfect Parry
Spend 1 Tempo when targeted by an eligible direct attack to sharply reduce that hit and apply Open to the attacker. Longer Reaction cooldown than Riposte.

## Slip Aside
When targeted by a single-target direct attack, reduce its accuracy/effect and shift row position if legal. No damage retaliation.

# Signature candidates

## Grand Riposte
Enter a limited counter state for the next set number of eligible hostile actions. Successful counters build a finishing thrust available on the Duelist's next natural turn.

Strict trigger cap prevents multi-hit/multi-action bosses from multiplying value without bound.

## Checkmate
Choose one enemy. For a short window, correctly exploiting its revealed intents builds Check tokens. Cash them out on the next natural turn for a strong precision finisher plus Break/anti-buff utility.

# Selectable passive candidates

- **Cold Read** — first correct intent exploitation each cycle grants extra Tempo.
- **Second Intention** — Feint also improves the next parry window.
- **No Wasted Motion** — reposition skills slightly improve the next attack rather than granting Speed outright.
- **Discipline of Steel** — anti-buff actions generate Tempo when they remove something.
- **Single Combat** — bonuses while focusing the same marked enemy; loses stacks on target swap.
- **Dancing Line** — row-changing attacks gain modest protection.
- **Counterpoint** — successful Reaction reduces one specific counter-synergy cooldown by a bounded amount.
- **Measured Mercy** — when Tempo would overcap, convert excess into a small barrier or accuracy buff.
- **Fencer's Reach** — selected blade attacks can reach the enemy back row at lower raw damage.
- **Unbroken Rhythm** — resisting displacement/control preserves Tempo that would otherwise decay under selected effects.

# Solo viability

Solo Duelist gets all major value from reading, feinting, parrying and exploiting a single enemy. Party-only value is optional utility rather than core rotation.

# Party identity

In party play, Duelist contributes:
- precision damage;
- buff stripping;
- selective action delay;
- soft control;
- formation repair;
- counter-pressure against enemies that use frequent direct attacks.

It should not replace Knight as protector or Oracle as dedicated timeline support.

# Prototype questions

- exact intent information granularity;
- Tempo cap/gain speed;
- whether wrong reads lose Tempo or only lose opportunity;
- how much boss action delay is healthy;
- whether anti-buff pressure is common enough to justify a full skill slot;
- final boundary between Duelist and later Fencer/Sword Saint descendants.
