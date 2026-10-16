# Hunter

**Status:** Draft for review and prototype; not locked

**Lineage:** Ranger -> Hunter

**Primary role:** Companion coordination / prey control / sustained ranged damage

**Secondary roles:** Soft CC, scouting-style utility, mark support, flexible solo play

## Class fantasy

Hunter fights as a coordinated pair with a bonded beast. The pet is not a second full turn-taking character and not an uncontrollable damage turret. The player sets prey, issues commands, creates openings with traps/marks, and the companion converts those openings into pressure.

## Weapon compatibility

Inherited Ranger pool:
- bows;
- crossbows;
- light spears where allowed;
- selected hunting tools.

Hunter remains ranged-first in the first slice. A future Beastmaster/Survival branch may lean farther into close combat.

## Innate mechanic — Bond + Prey

Hunter has one bonded beast selected outside combat from a small unlocked roster.

The beast:
- acts through automatic lightweight behavior between player turns;
- does **not** own a normal independent initiative slot;
- has one equipped Command action exposed through the Hunter mechanic;
- cannot recursively trigger Hunter Reactions;
- uses capped assist frequency so Speed does not multiply companion actions uncontrollably.

Hunter may mark one enemy as **Prey**.

Prey interactions:
- Hunter and beast gain selected bonuses against that target;
- some skills consume/refresh Prey state;
- changing Prey is allowed but should have opportunity cost so marking is a decision rather than free UI maintenance.

## Innate passive — Hunt Together

When Hunter meaningfully sets up an enemy with Prey, Snare, Exposed, or a compatible control state, the next eligible beast assist gains an enhanced effect.

This is the class loop:
**identify -> prepare -> command/assist -> reposition/repeat**.

# Active skill pool

## 1. Mark Prey
**Type:** Mark / setup

Designate one enemy as Prey. Refreshing the same target is cheap; changing target may use the skill's cooldown or consume Bond-related tempo.

### Technique candidates
- **Weak Spot** — mark also lowers armor/protection slightly.
- **Blood Trail** — damage over time against Prey improves tracking/assist effects.
- **Pack Target** — weaker personal bonus but stronger beast support.

## 2. Hunter's Shot
**Type:** Attack / baseline

Reliable ranged attack. Gains a modest benefit against Prey without requiring the mark to be functional.

## 3. Pinning Arrow
**Type:** Attack / soft CC

Damage plus Slow / row-movement resistance reduction. Normal enemies can be more strongly rooted; bosses receive reduced control and Break contribution.

## 4. Snare Trap
**Type:** Prepared control

Prepare a trap on an enemy row/target state. The next eligible movement/advance/direct assault triggers the trap, inflicting Snare and empowering the beast's next assist.

No grid placement is required.

### Technique candidates
- **Barbed Snare** — adds Bleed/attrition.
- **Heavy Snare** — stronger boss Break, weaker damage.
- **Alarm Line** — weaker control but reveals/penalizes stealth or ambush-like effects.

## 5. Coordinated Strike
**Type:** Attack / companion command

Hunter attacks and immediately commands one bounded beast follow-up. This is still one natural action; the companion follow-up is part of the skill resolution.

**Prototype cooldown:** 2-3 natural turns.

## 6. Beast Command
**Type:** Mechanic interaction

Trigger the currently equipped beast's unique command skill.

Examples of beast command families:
- defensive body block;
- high Break pounce;
- bleed bite;
- back-row harry;
- ally support howl.

The command changes with the bonded beast, giving pet choice real mechanical meaning.

## 7. Recall
**Type:** Defensive companion utility

Pull the beast out of aggressive behavior and gain a short defensive/utility effect. Used to protect Bond momentum or prepare a different command rather than manage pet HP micromanagement.

## 8. Covering Shot
**Type:** Attack / protection

Shoot an enemy and reduce its effectiveness when targeting a chosen ally or the Hunter before the Hunter's next natural turn.

This is ranged peel, not Knight-level guarding.

## 9. Trailblazer
**Type:** Self utility

Gain short resistance to Slow/row displacement and improve the next reposition or trap skill. In exploration, may later have noncombat utility, but combat function must stand alone.

## 10. Cull the Weak
**Type:** Attack / payoff

Deals increased damage when Prey is controlled, bleeding, exposed, or recently struck by the beast. Does not require low enemy HP.

## 11. Harrier Volley
**Type:** Multi-target pressure

Moderate attack against an enemy row. Each hit has low direct damage but can spread a minor hunting debuff or refresh weak Prey-adjacent setup.

## 12. Emergency Whistle
**Type:** Support / rescue

Command the beast to protect/disrupt around one ally, reducing the next eligible direct hit or applying a brief deterrent to the attacker.

## 13. Tracker's Insight
**Type:** Information / setup

Reveal one enemy's resistance/intent weakness category and make the next Hunter control/mark effect more reliable.

Useful against bosses without being mandatory every fight.

## 14. Relentless Pursuit
**Type:** Resource/payoff

When the current Prey changes row, gains a Speed advantage, cleanses a control state, or attempts to disengage, Hunter gains a limited follow-up benefit on the next natural turn. Can be activated to force a stronger pursuit shot.

# Reaction candidates

## Countershot
After an eligible ranged/direct attack targets Hunter, fire a weak return shot at the attacker.

## Protective Beast
When Hunter or a chosen ally receives an eligible direct hit, the bonded beast reduces a capped portion of damage or applies a deterrent debuff. Internal cooldown.

## Snap Trap
When Prey uses a qualifying movement/charge action, automatically trigger a weaker trap effect once per Reaction cooldown.

# Signature candidates

## Apex Hunt
Mark one enemy as Apex Prey for a limited sequence. Hunter skills and beast commands gain additional interactions against it, and setup effects are harder to cleanse. Does not simply grant a giant damage multiplier.

## Call of the Wild
Empower the bonded beast's command set for several bounded triggers, allowing stronger control/support/assist behavior without giving the beast a full independent turn economy.

# Selectable passive candidates

- **Predator's Patience** — keeping the same Prey for multiple natural turns builds a capped precision bonus.
- **Pack Tactics** — beast assists against controlled Prey gain extra utility.
- **Field Medic** — beast command can provide limited ally recovery/support; lowers offensive command potency.
- **Barbed Craft** — traps also inflict Bleed or anti-heal.
- **Relentless Tracker** — cleansing/removing Prey from an enemy refunds part of the marking cooldown.
- **Companion Discipline** — fewer automatic assists, stronger commanded assists.
- **Loose the Hound** — more frequent assists, weaker individual assists; strict cap remains.
- **Wild Guard** — beast protection effects are stronger when Hunter is in back row.
- **Big Game Hunter** — against elites/bosses, control effects convert more efficiently into Break rather than losing value.
- **Adapted Arsenal** — weapon choice modifies selected Hunter skills: bow precision, crossbow Break, spear close-pressure.

# Beast roster principle

The first slice does not need dozens of pets. Prototype with a small set, for example:
- **Hound** — tracking / bleed / anti-evasion;
- **Boar** — Break / defensive interception;
- **Hawk** — back-row pressure / intent reveal.

The goal is to prove that pet selection changes the build without multiplying content uncontrollably.

# Solo viability

Hunter is naturally solo-capable because the beast provides controlled pressure and utility, but the companion cannot function as a second full player character. Solo efficiency should come from coordination, not doubled action count.

# Party identity

Hunter brings:
- prey focus;
- companion utility;
- traps and soft CC;
- flexible support around a marked target;
- sustained damage that rewards party setup without requiring a fixed composition.

# Prototype questions

- exact automatic assist frequency;
- whether beast can be disabled/banished temporarily by enemies;
- how many pets the first slice needs;
- whether pet commands consume class resource, cooldown only, or Bond charges;
- how Prey target switching is priced;
- boundary between Hunter and future Beastmaster/Falconer-style branches.
