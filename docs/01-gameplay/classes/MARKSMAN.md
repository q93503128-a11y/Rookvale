# Marksman

**Status:** Draft for review and prototype; not locked

**Lineage:** Ranger -> Marksman

**Primary role:** Precision ranged burst / priority-target execution

**Secondary roles:** Anti-evasion, suppression, Break contribution, back-row pressure

## Class fantasy

Marksman wins by preparing one or two decisive shots instead of flooding the field with attacks. It is not Hunter without a pet and not a generic high-crit archer.

Core loop:
**observe -> acquire Aim -> create/open a firing window -> commit a shot -> relocate/rebuild**.

## Weapon compatibility

Inherited Ranger pool:
- bows;
- crossbows;
- firearm access may belong to later Musketeer/Gunslinger descendants rather than base Marksman.

Bow and crossbow can bias different Techniques without duplicating the entire skill list.

## Innate mechanic — Aim

Prototype cap: **5 Aim**.

Gain Aim through deliberate setup:
- basic/steady shots;
- remaining in a stable back-row firing position across a natural turn;
- hitting Marked/Exposed targets;
- selected information/setup skills.

Aim is spent on high-commitment shots.

Aim should not fully disappear from one forced reposition; disruption may reduce it instead. Otherwise row-control enemies would hard-disable the class.

## Innate passive — Line of Fire

While in the back row, Marksman gains access to its strongest precision benefits. Front row does not make the class useless, but lowers Aim efficiency and unlocks emergency disengagement tools instead of full burst.

This creates positional identity without a grid.

# Active skill pool

## 1. Steady Shot
**Type:** Attack / Aim generator

Reliable low-cooldown shot. Gain 1 Aim on hit, with an extra condition-based benefit if the user stayed in the same row since the previous natural turn.

### Technique candidates
- **Breath Control** — lower damage, guaranteed Aim generation even on defended targets.
- **Quick Draw** — lower Aim gain, reduced delay/cooldown.
- **Piercing Round** — crossbow-oriented; increased Break/armor pressure.

## 2. Mark Target
**Type:** Setup

Apply a personal Mark that improves Marksman's accuracy/precision interactions and enables selected payoffs. This mark should not become a mandatory party-wide damage multiplier.

## 3. Aimed Shot
**Type:** Aim spender / burst

Spend 2-3 Aim for a high-value single-target shot. Stronger against Marked/Exposed targets.

Longer cooldown than Steady Shot; should feel expensive enough that timing matters.

### Technique candidates
- **Dead Center** — more damage, no utility.
- **Armor Needle** — less damage, ignores/weakens protection and adds Break.
- **Hamstring Shot** — less damage, strong Speed/row-movement suppression.

## 4. Suppressing Fire
**Type:** Attack / debuff

Low-moderate damage plus reduced accuracy/effectiveness on the target's next direct offensive action.

Against multi-action bosses, uses event caps instead of a long blanket debuff.

## 5. Pin the Backline
**Type:** Attack / row control

Target enemy back row reliably. Apply a soft control state that makes forward movement or aggressive reposition less effective.

## 6. Overwatch
**Type:** Preparation

Prepare a firing lane until the Marksman's next natural turn. If an eligible enemy uses a qualifying aggressive movement/charge or exposes itself through a telegraphed action, the equipped Reaction can trigger more strongly.

Does not create multiple free shots by itself.

## 7. Focus Sight
**Type:** Setup / anti-evasion

Reveal stealth/illusion-like defense, reduce evasion, and gain Aim if a hidden/evasive state was actually removed.

## 8. Crippling Bolt
**Type:** Attack / control

Crossbow-friendly heavy shot that reduces Speed and contributes strong Break. Bow variants can trade Break for precision.

## 9. Split Shot
**Type:** Multi-target attack

Strike two legal targets at reduced power. Useful against ordinary encounters without becoming the best single-target option.

## 10. Execution Window
**Type:** Setup / finisher enabling

Apply a short personal state to one enemy. If it becomes Exposed, Broken, heavily debuffed, or crosses a health threshold before the Marksman's next natural turn, the next precision shot gains an enhanced effect.

The class does not need kills to generate Aim.

## 11. Reposition
**Type:** Self utility

Move to back row if legal, clear one limited positional penalty, and preserve part of Aim. No damage.

## 12. Quick Shot
**Type:** Attack / emergency

Low-commitment attack usable from any row. Lower damage but does not spend Aim and helps the class recover after disruption.

## 13. Breakpoint Shot
**Type:** Attack / boss utility

Spend Aim for exceptional Break/Stagger contribution rather than raw burst. Keeps Marksman valuable against bosses where hard control is converted into Break.

## 14. Perfect Release
**Type:** High Aim spender

Spend maximum or near-maximum Aim for a major precision shot. Bonus depends on preparation state, not only crit RNG.

# Reaction candidates

## Countershot
After an eligible enemy ranged/direct attack targets Marksman, return a low-power shot if line conditions are met.

## Overwatch Shot
When a qualifying enemy aggressive movement or exposed telegraph occurs during Overwatch, fire one bounded precision shot. Long Reaction cooldown; cannot trigger from another Reaction.

## Evade and Fire
When directly targeted while in back row, reduce the hit's effectiveness and prepare a small Aim bonus for the next natural turn. No immediate damage.

# Signature candidates

## Deadeye Window
Choose one target and enter a short precision state. Gain enhanced Aim generation and unlock a capped sequence of escalating precision shots against that target. The effect ends on a major miss/target loss or after a fixed number of natural turns.

## Rainline
Mark an enemy row and execute a disciplined multi-shot sequence that pressures several targets, reduces their outgoing accuracy, and sets up follow-up shots. A utility Signature rather than a single nuke.

# Selectable passive candidates

- **Patient Shooter** — staying in the same row through a natural turn grants capped Aim.
- **Hunter's Eye** — Mark Target also reveals one resistance/intent category.
- **No Escape** — shots against slowed/pinned targets gain utility rather than raw crit only.
- **Crossbow Discipline** — heavier Break/armor pressure, slower Aim cycle.
- **Bow Discipline** — faster Aim cycle, lower per-shot Break.
- **Prepared Position** — first forced reposition in a cycle loses less Aim.
- **Suppressor** — Suppressing Fire also reduces enemy crit/secondary effect chance.
- **Kill Zone** — Overwatch Reaction is stronger but has stricter trigger conditions.
- **Economy of Motion** — basic attack can generate Aim once per natural turn when no skill is spent.
- **Perfect Follow-through** — after spending 3+ Aim, next low-cost shot gains a small utility benefit.

# Solo viability

Marksman must be able to set up its own Mark, Slow, Break and Aim. Party debuffs improve its windows but are not mandatory.

# Party identity

Marksman brings:
- high priority-target pressure;
- reliable back-row reach;
- anti-evasion;
- suppression;
- boss Break conversion;
- strong payoff when allies create Exposed/Broken windows.

# Prototype questions

- exact Aim cap and whether passive row stability gain is too passive;
- how much forced reposition should hurt Aim;
- whether Aimed Shot and Perfect Release overlap too much;
- exact reaction trigger rules for Overwatch;
- future boundary between Marksman and Musketeer/Gunner descendants.
