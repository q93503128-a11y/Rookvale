# Knight

**Status:** Draft for review and prototype; not locked

**Lineage:** Armsman -> Knight

**Primary role:** Front-line protector / threat control / interception

**Secondary roles:** Break contribution, counter-pressure, row rescue, defensive support

## Class fantasy

Knight wins by deliberately taking ownership of dangerous enemy actions. It is not merely the character with the largest Defense stat.

The Knight:
- draws pressure toward itself when useful;
- rescues allies from dangerous targeting;
- redirects or mitigates selected attacks;
- anchors the front row;
- turns successful defense into Resolve, retaliation, break, or follow-up pressure;
- remains useful in solo play through break, counterplay, and self-defense even when there are no allies to protect.

## Weapon compatibility

Inherited Armsman pool:
- one-handed blades;
- maces / hammers;
- light spears / one-handed polearms;
- shields.

A shield is strongly supported but not treated as the only valid Knight itemization. Some skills carry a `Shield` tag and become unavailable or change when no shield is equipped. Spears and maces should create different Knight loadouts without turning into separate unrelated classes.

Future descendants such as Lancer, Guardian, Paladin, or other branches may narrow or expand this pool.

## Innate mechanic — Resolve

Prototype numbers, tunable:
- Resolve cap: **6**
- Start battle: **2 Resolve**

Gain Resolve:
- +1 the first time a hostile natural action directly targets the Knight;
- +1 additional Resolve when the Knight successfully redirects/intercepts an eligible direct attack from an ally;
- Defend grants +1 Resolve once per Knight natural turn;
- specific skills/passives may generate Resolve;
- one hostile natural action cannot fill Resolve through repeated multi-hits unless an explicit skill says otherwise.

Resolve does **not** automatically regenerate just because the Knight receives another natural turn.

This keeps the resource functional against a single boss while avoiding extra automatic Speed scaling.

## Innate class passive — Oath of the Line

Working rule:
- while in the front row, Knight receives an additional threat weight bonus beyond the global front-row modifier;
- successful protective actions feed Resolve as described above;
- Knight's Defend command is class-relevant rather than a dead fallback because it can feed Resolve and interact with selected passives;
- forced enemy targeting never overrides explicit boss/scripted target rules that are designed to ignore ordinary threat.

Exact threat multipliers are not locked.

# Active skill pool

The mature Knight is expected to learn more than eight of these and equip any eight normal actives.

## 1. Shield Bash
**Type:** Attack / Break / Threat

Deal modest damage and high Break/Stagger pressure. Generates additional threat.

Shield-tagged: stronger Break when a shield is equipped.

**Prototype cooldown:** 2 natural turns.

### Technique candidates
- **Concussive Bash** — lower damage, much higher Break/Stagger contribution.
- **Driving Bash** — reduced Break but can push a valid target from front to back row or disrupt row posture.
- **Disrupting Bash** — weak damage but interferes with a telegraphed charge/cast when the target is vulnerable to interruption.

## 2. Challenge
**Type:** Attack / Threat control

A light weapon attack combined with a direct challenge. Greatly increases the Knight's target score for that enemy's next eligible hostile action.

Does not erase enemy-specific targeting logic, AoE selection, or scripted boss mechanics.

**Prototype cooldown:** 3 natural turns.

### Technique candidates
- **Single Combat** — stronger single-target forcing and small Break; no multi-target utility.
- **Open Challenge** — weaker effect applied to multiple enemies or an enemy row.
- **Punishing Oath** — weaker taunt pressure, but if the target chooses another ally anyway it becomes Exposed / suffers a retaliation setup effect.

## 3. Guard
**Type:** Ally protection

Choose one ally. Until the Knight's next natural turn, the first eligible direct single-target hostile attack against that ally is redirected to the Knight with mitigation.

**Cost:** 1 Resolve.
**Prototype cooldown:** 2 natural turns.

This is a prepared guarantee and therefore differs from the emergency Reaction `Intercept`.

### Technique candidates
- **Bodyguard** — stronger reduction on the redirected hit, but protects only one hit.
- **Shared Burden** — Knight takes only part of the damage and the ally takes the rest; covers more than one eligible hit with strict caps.
- **Escort** — also moves/protects the ally toward the back row while the Knight takes the front position when legal.

## 4. Bulwark
**Type:** Self-defense / anchor

Spend Resolve to brace for a dangerous enemy sequence. Reduce the next limited number of direct hits and gain strong resistance to displacement/control while active.

**Cost:** 2 Resolve.
**Prototype cooldown:** 3 natural turns.

Use hit/event caps rather than a long duration that can be exploited through timeline manipulation.

### Technique candidates
- **Fortress** — maximum self-mitigation; no offensive benefit.
- **Counterwall** — weaker mitigation but primes the Knight's next retaliation/counter effect.
- **Aegis** — some of the mitigation is converted into a small protective effect for a chosen ally or rear row.

## 5. Shield Wall
**Type:** Party protection

Spend Resolve to grant the party limited protection charges against upcoming direct attacks. This does not make the back row untargetable and does not redirect every hit to the Knight.

**Cost:** 3 Resolve.
**Prototype cooldown:** 4 natural turns.

Designed as a party-wide answer to a telegraphed danger window rather than a permanent aura.

## 6. Line Exchange
**Type:** Row rescue / utility

Swap rows with an ally when legal, placing the Knight closer to danger and moving the ally away from it. The rescued ally receives brief protection against immediate retargeting.

No damage.

**Prototype cooldown:** 2 natural turns.

This skill gives the tank something tactically valuable beyond raw mitigation.

## 7. Guarded Advance
**Type:** Attack / reposition

Move the Knight to the front row if needed and strike an enemy. Gains additional threat and modest protection against the next eligible direct attack.

**Prototype cooldown:** 2 natural turns.

### Technique candidates
- **Shield Charge** — shield required; higher Break and anti-displacement value.
- **Spearpoint Advance** — spear required; can reach a legal back-row target but has less self-protection.
- **Rescue Advance** — lower damage; also shifts an endangered ally toward the back when legal.

## 8. Breaker Blow
**Type:** Attack / boss-control contribution

A committed strike focused on Break/Stagger rather than raw damage. Consumes Resolve for significantly higher Break against elites/bosses without hard-stunning them outright.

**Cost:** 1-2 Resolve depending on final tuning.
**Prototype cooldown:** 3 natural turns.

This keeps Knight useful when the enemy already wants to hit them.

## 9. Retaliatory Strike
**Type:** Attack / defensive conversion

Deal increased damage if, since the Knight's previous natural turn, the Knight blocked, intercepted, guarded, or was directly targeted by a meaningful hostile action.

The condition is earned through tanking rather than enemy kills.

**Prototype cooldown:** 2 natural turns.

## 10. Pinning Strike
**Type:** Attack / control

Deal modest damage and apply a soft control effect such as Speed reduction, movement/row resistance reduction, or target-pressure suppression depending on weapon/Technique.

This is not a full turn-loss CC.

**Prototype cooldown:** 2-3 natural turns.

## 11. Stand Ground
**Type:** Defensive utility

Remove or resist selected displacement / destabilization effects on the Knight and strengthen front-row anchoring for a short event-based window.

If used while already stable, may convert part of the value into Resolve or Break resistance so it is not completely dead against bosses without row movement.

## 12. Steadying Call
**Type:** Support

Help one ally recover from a limited class of control/fear-like effects or grant temporary resistance to disruption.

Knight is not a full cleanser; Priest and other support classes remain much better at broad status removal.

**Prototype cooldown:** long enough that this is an emergency tool, not routine cleansing.

## 13. Pressure Strike
**Type:** Attack / threat debuff interaction

Strike a target and reduce its effectiveness when attacking anyone other than the Knight for its next eligible action. This is softer than Challenge and can coexist with enemies that partially ignore normal threat.

Useful in solo because it remains a normal attack; in party play it becomes a protection tool.

## 14. Oathkeeper's Blow
**Type:** Resolve spender / offense

Spend Resolve for a strong but not burst-DPS-class-level attack. Gains an additional effect based on the Knight's recent protective behavior, such as Break, barrier, or threat.

Purpose: prevent full Resolve from becoming wasted when protection is currently unnecessary.

# Reaction candidates

The Knight equips at most one Reaction.

## Intercept
When an ally is targeted by an eligible direct single-target attack, spend 1 Resolve to redirect a capped portion of that damage to the Knight.

- emergency automatic protection;
- weaker than prepared `Guard`;
- limited to once per hostile action / reaction cooldown rules;
- cannot recursively trigger another Reaction.

## Riposte
After the Knight receives an eligible direct melee hit while properly positioned, counter with a modest weapon strike.

- no extra natural turn;
- does not tick cooldowns or natural-turn effects;
- strict per-hostile-action / reaction cooldown cap.

## Last Cover
When an ally would be pushed into a critical-health state by an eligible direct attack, consume Resolve to reduce the finishing portion of the hit or grant an immediate emergency barrier.

Longer Reaction cooldown and higher Resolve cost than Intercept.

# Signature candidates

## Fortress Oath
Spend substantial Resolve. For the next limited number of eligible hostile direct attacks against the party:
- Knight intercepts them;
- redirected damage is reduced;
- Knight gains strong displacement/control resistance;
- no more than the intended number of attacks can be absorbed.

This is a protection Signature, not an invulnerability button.

## Duel of Oaths
Choose one dangerous enemy. For its next limited number of natural actions:
- its normal target weighting heavily favors the Knight;
- Knight receives improved defensive conversion against that enemy;
- successfully surviving its pressure unlocks a stronger counter/break follow-up.

Boss scripted mechanics can ignore the targeting component while still interacting with the defensive/counter component where appropriate.

# Selectable passive candidates

The mature build equips four.

## Vanguard Habit
Begin combat with additional Resolve or gain a one-time Resolve burst the first time the Knight becomes the primary target.

## Retaliation Doctrine
After successful Guard / Intercept / meaningful block, the Knight's next damaging active gains a stronger retaliation effect.

## Formation Keeper
While the Knight is in the front row, allies directly protected by the formation gain a small benefit against row pressure / direct targeting. This does not make them untargetable.

## Iron Discipline
At high Resolve, the Knight gains increased resistance to displacement and hard control. Spending below the threshold removes it.

## Shieldcraft
With a shield equipped, selected Guard/Bulwark skills gain better efficiency or extra utility rather than only raw Defense.

## Long Reach
With a spear/polearm equipped, selected Knight attacks gain back-row access or improved row-control behavior while some shield-specific benefits are reduced.

## Measured Defense
Using the universal Defend command can modify one defensive cooldown or improve the next protection skill. Explicit cooldown manipulation is capped and never treated as an extra natural turn.

## Oathkeeper
Increase Resolve cap / improve one category of Resolve spender, creating a resource-heavy build at the cost of another passive slot.

## Calm Under Fire
When the Knight resists or receives a control effect, gain a limited defensive benefit or Resolve. Internal cooldown prevents status-spam farming.

## Measured Strikes
Basic attacks against a Challenged / Pressured enemy can generate a small amount of Resolve once per natural turn, supporting a more offensive solo Knight build.

# Weapon identity inside Knight

The class remains one Knight kit, but compatible weapons can bias the build.

### Blade
- balanced damage / retaliation;
- reliable general-purpose Knight.

### Mace / hammer
- Break/Stagger emphasis;
- better disruption, slightly lower precision/reach.

### Light spear / one-handed polearm
- better row reach and pressure;
- supports Pinning / back-row threat control;
- weaker access to some shield-centric Techniques when configured two-handed in future descendants.

### Shield
- unlocks or strengthens Bash/Bulwark/Guard Techniques;
- should not simply be `+Defense`.

# Solo viability

Solo Knight cannot rely on protecting allies, so a viable solo loadout should be able to omit Guard, Line Exchange, and other ally-only skills.

Solo loop:
1. enemy targeting naturally generates Resolve;
2. Bulwark / Defend creates safe pressure windows;
3. Breaker Blow and Shield Bash contribute control;
4. Retaliatory Strike / Oathkeeper's Blow turn defense into offense;
5. weapon and passive choices determine whether the solo Knight leans counter, Break, or steady damage.

The Knight should be slower at pure damage than a dedicated damage class but not painfully inefficient in ordinary solo progression.

# Party identity

Party Knight should create **safety and permission** for allies rather than only reduce damage numbers.

A good Knight lets:
- fragile allies remain in aggressive loadouts;
- back-row characters survive targeted pressure;
- the party answer a telegraphed boss strike;
- CC/break windows happen without turning Knight into a dedicated controller;
- mistakes be recovered through row rescue / emergency reactions.

# Prototype questions

These remain tunable and should not be treated as locked until playtested:
- Resolve cap/start value and exact gain rate;
- exact threat multipliers;
- whether Guard fully redirects one hit or splits damage baseline;
- exact Shield Wall charge model;
- how much ally-only content is acceptable in one class's learned pool;
- which hard-control types Knight may cleanse/resist;
- final number of Knight actives/passives learned in the first slice;
- whether shieldless Knight is strong enough to be a real build rather than a trap;
- whether Spear Knight should stay inside Knight or eventually graduate into Lancer earlier in the tree.
