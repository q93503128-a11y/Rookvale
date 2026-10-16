# First Eight Class Kits — Cross-Check 01

**Status:** Draft audit after first broad kit pass

Scope:
- Knight
- Duelist
- Hunter
- Marksman
- Pyromancer
- Cryomancer
- Priest
- Oracle

The purpose is to catch overlap, missing combat axes, solo failures, multiplayer-only kits, and resource loops that break against single bosses before implementation.

## 1. Identity separation

### Knight vs Duelist
**Pass.**
- Knight owns threat, interception, guarding, party protection, Resolve and front-row anchoring.
- Duelist owns intent exploitation, Tempo, parry/riposte precision, anti-buff pressure and selective timeline delay.

Risk:
- both can counter. Keep Knight counter damage secondary and protection-driven; Duelist counter is a primary offensive identity.

### Hunter vs Marksman
**Pass with implementation caution.**
- Hunter owns bonded beast, Prey, traps, companion commands and sustained coordination.
- Marksman owns Aim, precision setup, high-value shots, suppression and back-row firing discipline.

Risk:
- both use marks and ranged control. Hunter's Prey must be a coordination state; Marksman's Mark must be personal precision setup. Do not give both identical `mark -> +damage` loops.

### Pyromancer vs Cryomancer
**Strong pass.**
- Pyromancer owns Burn maintenance/consumption, Ash, anti-heal and combustion decisions.
- Cryomancer owns Frost, Chill, Freeze/Break conversion, barriers and Shatter decisions.

Risk:
- avoid making Shatter simply cold Combust. Cryo Shatter should often convert setup into control/Break/protection, not only damage.

### Priest vs Oracle
**Strong pass.**
- Priest owns direct healing, cleanse, barriers, rescue and Grace.
- Oracle owns information, predictive mitigation, Omens, delayed support and bounded timeline manipulation.

Risk:
- Oracle must not become the best healer plus best support. Its direct recovery stays limited.

## 2. Solo viability

All eight have self-contained loops that do not require party members:
- Knight: enemy targeting -> Resolve -> defense/counter/Break.
- Duelist: intent -> Tempo -> exploit/counter.
- Hunter: Prey + beast commands work alone.
- Marksman: Aim and self-applied Mark/Slow/Break.
- Pyromancer: Burn -> Ash -> Combust without kills/adds.
- Cryomancer: Frost -> Shatter/Break/barrier against one boss.
- Priest: healing/barrier + modest holy offense/control.
- Oracle: predictive debuff/timeline + astral attacks.

No first-slice class currently requires another specific class to function.

## 3. Single-boss compatibility

**Pass by design.**

Explicit anti-failure rules:
- no core resource requires enemy kills;
- hard CC converts to Break/action delay/vulnerability on bosses;
- Hunter pet does not require adds;
- Marksman Aim does not require executions;
- Pyromancer Ash has multiple non-kill sources;
- Priest Grace requires meaningful support, with self-support rules to be tested in solo;
- Oracle Omen comes from prediction/support, not enemy death.

Potential concern:
- Priest Grace in full-health solo states may generate too slowly. Prototype should allow proactive barrier/prevention events to generate Grace when they prevent meaningful damage.

## 4. Party role coverage

Current first-slice sample covers:
- primary tank/protector: Knight;
- precision/counter melee DPS: Duelist;
- companion/control ranged DPS: Hunter;
- precision/burst ranged DPS: Marksman;
- DoT/burst caster DPS: Pyromancer;
- control/barrier caster: Cryomancer;
- primary healer/cleanser: Priest;
- predictive support/timeline utility: Oracle.

This is intentionally broad enough to test role interaction without implementing the long-term roster.

## 5. Status / control coverage

Available axes across the eight:
- threat / taunt / pressure;
- Guard / Intercept / barrier;
- Riposte / parry / reaction;
- Slow / Chill / Frost / Freeze conversion;
- Burn / anti-heal;
- marks / Prey / Exposed;
- accuracy suppression / Whiteout / Suppressing Fire;
- row movement / pinning;
- buff removal / buff weakening;
- cleanse / status prevention;
- action delay / acceleration;
- Break/Stagger;
- delayed healing / delayed attack;
- companion commands.

No need to add more status names merely for count. Future statuses should add new decisions.

## 6. Reaction audit

Each class has a different Reaction identity:
- Knight: intercept/protect/counter.
- Duelist: parry/riposte/evasion.
- Hunter: beast protection/countershot/trap trigger.
- Marksman: overwatch/countershot/defensive reposition.
- Pyromancer: retaliatory Burn/defensive flare.
- Cryomancer: frostguard/predictive freeze defense.
- Priest: emergency rescue/purify.
- Oracle: predicted mitigation/fate intervention.

Shared `Countershot` concept between Hunter and Marksman is acceptable only if final implementations differ strongly. Hunter version should be simple companion/ranger retaliation; Marksman version should tie to Aim/Overwatch or be replaced if redundant.

## 7. Signature audit

Current Signatures are not all damage nukes:
- Knight: Fortress Oath / Duel of Oaths.
- Duelist: Grand Riposte / Checkmate.
- Hunter: Apex Hunt / Call of the Wild.
- Marksman: Deadeye Window / Rainline.
- Pyromancer: Furnace Heart / Conflagration.
- Cryomancer: Winter Dominion / Crystal Prison.
- Priest: Miracle / Covenant of Life.
- Oracle: Written in the Stars / Rewrite Fate.

**Pass.** Signature slot is producing class fantasy instead of a universal ultimate meter.

## 8. Speed-system risk audit

High-risk mechanics:
- Duelist Tempo + action delay;
- Cryomancer Chill/Freeze;
- Oracle Favorable Hour / Delay Fate / Borrowed Moment;
- Pyromancer Searing Haste;
- Marksman stable-row Aim if Speed gives too many natural turns.

Rules to preserve:
- bonus/reaction actions never count as natural turns;
- no effect grants a full immediate natural turn in the first prototype;
- cooldown reduction has a floor and per-skill/per-target caps;
- Speed-altering buffs should often adjust next-action delay rather than multiply long-term Speed stat;
- repeated boss delay uses diminishing/cooldown rules.

## 9. Resource risk audit

Resources/mechanics:
- Knight: Resolve.
- Duelist: Tempo.
- Hunter: Prey + Bond/companion command cadence.
- Marksman: Aim.
- Pyromancer: Ash + Burn.
- Cryomancer: Frost + Cold Front.
- Priest: Grace.
- Oracle: Omens.

This is intentionally varied, but avoid turning every UI into another identical six-pip meter. Hunter Prey, Cryomancer Frost, and Oracle predictive states can be represented differently.

## 10. First implementation recommendation

Do not implement all learned skills immediately.

For the first playable combat prototype, implement **4-6 representative normal actives per class**, one innate mechanic, one Reaction candidate, one Signature candidate, and a small passive/Technique sample.

Recommended first mechanic coverage:

### Knight
- Shield Bash, Challenge, Guard, Bulwark, Retaliatory Strike.

### Duelist
- Testing Thrust, Feint, Lunge, Opening Cut, Tempo Break.

### Hunter
- Mark Prey, Hunter's Shot, Snare Trap, Coordinated Strike, Beast Command.

### Marksman
- Steady Shot, Mark Target, Aimed Shot, Suppressing Fire, Reposition.

### Pyromancer
- Ember Bolt, Combust, Fireball, Smolder, Flame Ward.

### Cryomancer
- Frost Bolt, Shatter, Frozen Bind, Ice Wall, Crystal Spear.

### Priest
- Mend, Sanctuary, Cleanse, Dazzling Prayer, Guardian Hymn.

### Oracle
- Foretell, Premonition, Delay Fate, Auspicious Sign, Fate's Needle.

This set is large enough to test each class loop while still respecting the project rule: broad planning, narrow first implementation.

## User decisions currently required

None. The next useful user review point is after the first combat prototype exposes:
- whether 8 mature active slots feel excessive or correct;
- whether front/back formation creates enough decisions;
- whether intent/timeline information is readable;
- whether companion automation feels responsive without feeling like a second character;
- whether tank/healer/support actions feel worthwhile in solo play.
