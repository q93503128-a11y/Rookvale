# First Combat Prototype — Enemy Set

**Status:** Prototype encounter set; mechanics are implementation targets, names/lore and final coefficients remain Draft
**Date:** 2026-10-16

This enemy set exists to test combat systems, not to establish final Rookvale region lore. Working enemy names are intentionally plain. Final factions, art direction, species, lore, rewards, and encounter placement come later.

The set must expose failures in:
- Threat / Taunt;
- Guard / Intercept;
- Front / Back rows;
- Break;
- Burn and anti-heal;
- Chill / Freeze boss conversion;
- Cleanse / Dispel;
- Barrier;
- healing / prevention / rescue;
- prediction and visible intent;
- Marks / Prey;
- companion cadence;
- Reaction triggers;
- Signature windows;
- Speed and timeline manipulation.

Numbers use `PROTOTYPE_NUMBERS.md` and remain tunable.

---

# 1. Common enemy intent language

The base UI should reveal a compact intent before an enemy's committed Natural Action.

Baseline intent categories:
- **Attack** — direct damaging action;
- **Area** — row/party damage;
- **Control** — status / row / timeline pressure;
- **Support** — healing / Barrier / buff / cleanse;
- **Defense** — self/ally protection;
- **Special** — encounter-specific action whose exact behavior may be partially hidden.

Additional icons/flags when globally known:
- **Breakable** — the prepared action can be cancelled by a Break Event / valid interrupt;
- **Redirectable** — Guard/Intercept can redirect it;
- **Unredirectable** — it ignores ordinary Guard/Intercept;
- likely target row when obvious.

Oracle Foresight should reveal deeper information such as exact target preference, secondary status, whether the action is truly Breakable, or which branch a Special intent will become. Base UI remains useful without Oracle.

---

# 2. Normal enemies

## A. Cutthroat — baseline front-line melee

**Purpose:** baseline Threat, direct-hit, Guard/Intercept and Break target.

Prototype stats:
- HP: **310**
- Power: **84**
- Defense: **36**
- Speed: **100**
- Break Max: **52**
- Row: Front

### Slash
- Attack / Direct / Redirectable
- coefficient: **1.00**
- target policy: highest ordinary TargetScore
- Break damage: 5

This is the control sample for normal direct damage.

### Heavy Chop
- Attack / Direct / Breakable / Redirectable
- coefficient: **1.45**
- heavy action delay: **1.15**
- Break damage: 7
- telegraphed one action ahead where the timeline UI allows it

If interrupted/broken during preparation, the attack is cancelled. This gives the first obvious Break tutorial target.

### Press the Weak
- Attack / Direct / Redirectable
- coefficient: **1.10**
- modest AI preference toward targets below 50% HP
- does not ignore Threat; low HP is only one TargetScore factor

**Tests:** Knight threat, Guard, Intercept, Priest rescue, Duelist parry, basic Break readability.

---

## B. Crossbowman — back-row hunter

**Purpose:** prove that the Back row is safer, not immune; test row reach and protection.

Prototype stats:
- HP: **250**
- Power: **92**
- Defense: **28**
- Speed: **103**
- Break Max: **45**
- Row: Back

### Bolt
- Attack / Direct / Redirectable
- coefficient: **1.05**
- can target either row

### Pick Off
- Attack / Direct / Redirectable
- coefficient: **1.30**
- AI preference: **x1.8** target score toward Back-row targets, then low-Barrier targets
- CD 2

High Threat can still overcome the preference; this is not an absolute tank bypass.

### Pinning Bolt
- Attack / Control / Direct / Redirectable
- coefficient: **0.80**
- applies **Root** for 1 Target Natural Turn
- CD 2

**Tests:** Back-row pressure, Knight protection, Marksman/Hunter back-row reach, Root, row rescue, Reaction targeting.

---

## C. Shieldman — defense / protection enemy

**Purpose:** test Defense, Barrier, Guard, Dispel, Break and target switching without becoming a pure HP sponge.

Prototype stats:
- HP: **420**
- Power: **72**
- Defense: **66**
- Speed: **84**
- Break Max: **74**
- Row: Front

### Shield Strike
- Attack / Direct / Redirectable
- coefficient: **0.90**
- Break damage: 12

### Cover Ally
- Defense
- choose one ally
- Guard the next eligible direct single-target hit against that ally
- 1 event charge, safety expiry at Shieldman's next Natural Turn
- CD 2

### Brace
- Defense
- gain **Defense Up** and a Barrier of roughly 80-95 HP
- 1 Target Natural Turn
- CD 3

The Defense Up is Dispellable. The Barrier is not automatically removed by generic Dispel unless a skill explicitly strips Barrier.

### Shield Fault
When Broken, Shieldman loses any active `Cover Ally` and cannot use Brace on its next Natural Turn. This is encounter-specific Break payoff, not a global Break rule.

**Tests:** Duelist anti-buff, Marksman armor/Break shots, Cryomancer Shatter-Break, attack target switching, Dispel versus Barrier distinction.

---

## D. Knife Runner — fast positional enemy

**Purpose:** stress Speed, Slow, Root, traps, Overwatch, reaction caps and duration semantics.

Prototype stats:
- HP: **225**
- Power: **79**
- Defense: **24**
- Speed: **125**
- Break Max: **40**
- Row: Back initially

### Rush In
- Attack / Movement / Direct / Redirectable
- move Back -> Front and strike
- coefficient: **0.95**
- quick action delay: 0.85

Qualifies for Snare/Overwatch-style movement triggers.

### Knife Flurry
- Attack / Direct
- three small hits totaling about coefficient **1.20**
- multi-hit counts as one hostile Natural Action for Resolve/Reaction/event-cap farming unless an effect explicitly says otherwise

### Slip Back
- Movement / Defense
- move Front -> Back
- gain a small one-action defensive state rather than permanent Evasion

### Exploit Opening
- Attack / Direct / Redirectable
- prefers a target that changed rows since Runner's previous Natural Turn
- coefficient: 1.20

**Tests:** high-Speed cooldown/duration behavior, Hunter Snare/Snap Trap, Marksman Overwatch, Cryomancer Slow/Chill, row interactions, anti-multihit resource farming.

---

## E. Hedge Hexer — status pressure

**Purpose:** give Cleanse, prevention, DoT, Healing Reduction and prediction meaningful targets.

Prototype stats:
- HP: **275**
- Power: **84**
- Defense: **30**
- Speed: **94**
- Break Max: **52**
- Row: Back

### Venom Hex
- Control / Direct hostile spell
- apply **Poison** for 3 Target Natural Turns
- no direct damage
- CD 2

### Open Wound
- Attack / Direct / Redirectable
- coefficient: 0.75
- apply 1 **Bleed** stack

### Wither Salve
- Control
- apply **Healing Reduction 35%** for 2 Target Natural Turns
- CD 3

### Murk
- Control / Area
- apply **Disrupted** to the targeted row: the next eligible non-basic secondary effect is reduced
- CD 3

**Tests:** Priest Cleanse/Purity Ward, Pyromancer Cauterize boundary, Oracle prediction, status durations on fast/slow units, anti-heal readability.

---

## F. Field Chirurgeon — healer / support enemy

**Purpose:** test anti-heal, focus fire, Mark/Prey persistence, Dispel, enemy Cleanse and support priority.

Prototype stats:
- HP: **285**
- Power: **80**
- Defense: **32**
- Speed: **90**
- Break Max: **56**
- Row: Back

### Patch Up
- Support / Heal
- heal coefficient: **1.40**
- target the most injured ally by missing-HP percentage
- CD 1

### Fortifying Draught
- Support
- one ally gains a standard Barrier plus **Defense Up** for 1 Target Natural Turn
- CD 2

### Purging Salts
- Support / Cleanse
- remove one eligible ordinary negative status from an ally
- priority: hard/strong control -> Healing Reduction -> high Burn -> Poison/Bleed -> Chill/soft control
- CD 3

It **cannot** remove Hunter `Prey` or source-owned class Marks through ordinary Cleanse.

### Rally Dose
- Support
- grant modest **Damage Up** for 1 Target Natural Turn
- CD 3

**Tests:** Pyromancer anti-heal and Burn maintenance, Duelist/other Dispel, Marksman/Hunter target designation, distinction between Cleanseable debuffs and source-owned Marks.

---

# 3. Elite

## Veteran Enforcer — mixed-pressure elite

**Purpose:** combine direct pressure, row attacks, target exceptions, telegraphs, Break and reaction timing before the boss.

Prototype stats:
- HP: **920**
- Power: **108**
- Defense: **58**
- Speed: **102**
- Break Max: **115**
- Row: Front

### Hammer Blow
- Attack / Direct / Redirectable
- coefficient: 1.25
- Break damage: 12

### Sweep the Line
- Area / Front-row attack
- coefficient: 0.85 to each target in Front
- ordinary Guard cannot redirect a row-wide attack
- CD 2

### Call Out the Rear
- Special -> Attack
- telegraph announces a Back-row focus action
- next Natural Turn uses `Vaulting Strike`

### Vaulting Strike
- Attack / Direct / Redirectable
- coefficient: 1.55
- strong AI preference for a Back-row target regardless of normal Front-row pressure
- Threat still matters among legal/priority targets

### Brace Counter
- Defense / Reaction setup
- until Enforcer's next Natural Turn, the first eligible direct melee hit against it causes a small counter
- one charge
- counter cannot trigger another Reaction
- CD 3

### Crushing Windup
- Attack / Breakable / Direct / Redirectable
- coefficient: 1.85
- long visible preparation
- if Broken during preparation, cancel it and apply normal Exposed
- CD 4

### Elite control rule
Hard Freeze against Enforcer may remove one standard action only when Repeat Resistance is low. Subsequent Freeze rapidly loses efficiency; excess control converts into Break/Delay.

**Tests:** Guard limits versus AoE, Back-row hunting, Duelist intent/Parry, Breakable telegraph, Reaction anti-chain, Freeze diminishing resistance.

---

# 4. First boss

## Black Banner Captain — working prototype boss

**Lore/name status:** Working name only; final faction and presentation are not locked.

**Fight purpose:** a single encounter that exercises every first-slice combat axis without becoming an HP sponge.

### Solo baseline stats
- HP: **1,850**
- Power: **120**
- Defense: **65**
- Speed: **100**
- initial Break Max: **180**
- party scaling: use `PROTOTYPE_NUMBERS.md`

### Global boss rules
- Threat applies, but some actions declare target preferences or scripted row patterns.
- Ordinary Taunt strongly modifies direct-action targeting but does not override Area/Unredirectable actions.
- Freeze does not repeatedly erase boss Natural Turns; it converts to Break + bounded Delay + Cryomancer setup.
- Stun cancels only actions flagged Interruptible/Breakable as appropriate; otherwise it converts to Break + bounded Delay.
- Prey and class-owned Marks remain valid setup tags unless a specific boss mechanic says otherwise.
- Burn, Poison, Bleed, Chill, Healing Reduction and Defense Down are allowed with tier-appropriate resistance; the boss is not generically immune to damage/control classes.
- repeated boss Break increases the next Break maximum as defined in the numeric skeleton.

## Phase 1 — Establish the rules (100% -> 70%)

### Officer's Cut
- Attack / Direct / Redirectable
- coefficient: 1.15
- uses ordinary Threat target selection

### Execution Mark
- Special / source-owned Mark
- choose one target using a mix of Threat and a visible preference rule
- the base UI shows the marked target
- Oracle Foresight may additionally reveal whether the follow-up will include Bleed, row movement, or anti-Barrier pressure

This Captain-owned Mark does not interact with Marksman or Hunter mechanics because Marks are source-owned.

### Execution Order
- Attack / Direct / Redirectable / Breakable
- normally follows `Execution Mark`
- coefficient: 1.80
- heavy action delay: 1.15
- large Break window during preparation
- Guard/Intercept can redirect it unless a later phase variant explicitly says otherwise

This is the core Knight/Duelist/Oracle/Break tutorial mechanic.

### Sweeping Cut
- Area / Front-row
- coefficient: 0.85 per Front target
- CD 2
- not redirectable by ordinary Guard

This prevents `put Knight in Front and solve every attack`.

### Hooked Slash
- Attack / Direct / Redirectable
- coefficient: 0.95
- apply 1 Bleed
- creates a modest Cleanse/heal-prevention burden without dominating the fight

## Phase 2 — Support and formation pressure (70% -> 35%)

At phase start, the Captain calls support.

Prototype party-size rule:
- 1-2 players: summon one reduced-HP `Field Chirurgeon`;
- 3-4 players: summon one Field Chirurgeon plus one reduced-HP `Shieldman` or an additional pressure enemy selected by encounter tuning.

This adds decisions instead of only multiplying boss HP.

### Rally the Line
- Support / Heal / Breakable
- heal the Captain and surviving support enemy for a bounded amount, target about 7-8% of boss Max HP before Healing Reduction
- also grants short Damage Up to the Captain
- CD 4

If Broken during preparation, both heal and buff are cancelled.

This gives Pyromancer anti-heal, Break builds, focus fire, and Dispel distinct answers.

### Raise Banner
- Defense / Support
- gain Barrier approximately 12-15% boss Max HP and Defense Up for 1 Target Natural Turn
- Defense Up is Dispellable
- Barrier follows normal Barrier rules and is not automatically deleted by ordinary Dispel
- CD 3

### Driving Advance
- Attack / Movement pressure / Front-row
- coefficient: 1.00 to one target
- attempts to Push the target Front -> Back or destabilize row position
- if target is already Back, applies a mild Slow/Disrupted effect instead
- CD 2

This tests Knight anchoring, Marksman Aim disruption, Cryomancer/row recovery and movement rules.

### Poisoned Standard
- Control / Area
- target one row; apply a weaker 2-turn Poison or Healing Reduction state
- visible Control intent
- CD 3

Priest can Cleanse/ward it, Oracle can prepare for it, and offensive parties can choose to race it.

## Phase 3 — Last Stand (35% -> 0%)

The phase should become more predictable but more dangerous, rewarding mastery rather than adding random chaos.

### Last Stand
One-time phase transition:
- remove the Captain's own remaining ordinary Barrier;
- gain a modest outgoing Damage Up;
- the next action receives a small Haste/Advance-style benefit within global caps;
- Defense decreases slightly while attacking aggressively.

The boss becomes easier to hurt, not simply a larger HP sponge.

### Bannerfall Combo
A deterministic three-step loop begins:
1. `Execution Mark` / direct-threat decision;
2. `Bannerfall Sweep` — row attack;
3. `Final Order` — Breakable high-commitment direct strike.

The exact target and secondary effect can vary from readable state, but the broad loop stays learnable.

### Bannerfall Sweep
- Area
- chooses Front or Back based on a visible banner stance
- coefficient: 0.95 per legal target
- changes stance after use

### Final Order
- Attack / Direct / Breakable / Redirectable
- coefficient: 2.00
- longer preparation than normal attacks
- gains extra damage if the preceding Bannerfall Sweep hit its intended row cleanly
- if Broken, cancelled and boss enters normal Exposed window

This creates a late-fight Signature/Break/Guard/Prediction decision window instead of a passive damage race.

---

# 5. Boss intent and Oracle information test

The boss deliberately uses **layered telegraph depth**.

All players can see:
- broad intent category;
- obvious Mark target;
- obvious row-wide danger;
- clearly Breakable major windups once learned/taught.

Oracle can reveal additional information, depending on skill:
- precise target preference before a Mark is committed;
- whether a Special action will become Attack, Control or Support;
- exact secondary status;
- whether an apparent windup can be interrupted or only delayed;
- whether the next phase support call is Chirurgeon/Shieldman when the encounter has alternatives.

Oracle therefore gains useful information value without making non-Oracle parties blind.

---

# 6. Encounter sequence for first playable test

Do not throw all enemy mechanics into the first room.

## Encounter 1 — Front and Back
- 1 Cutthroat
- 1 Crossbowman

Tests:
- Front/Back targeting;
- basic Threat;
- Back-row pressure;
- direct Guard/Intercept;
- back-row reach.

## Encounter 2 — Protection and sustain
- 1 Shieldman
- 1 Field Chirurgeon
- optionally 1 Cutthroat for larger parties

Tests:
- Guard;
- Barrier vs buff distinction;
- Break;
- Dispel;
- anti-heal;
- focus target selection;
- Mark/Prey not being generic debuffs.

## Encounter 3 — Speed and status
- 1 Knife Runner
- 1 Hedge Hexer
- optionally 1 Cutthroat

Tests:
- Speed turn frequency;
- Slow/Chill;
- Root/trap/Overwatch;
- Bleed/Poison/Healing Reduction;
- Cleanse/prevention;
- duration clocks.

## Encounter 4 — Elite
- Veteran Enforcer
- Crossbowman or Hexer depending which mechanic needs more pressure

Tests:
- telegraphed Break;
- Back-row focus;
- Reaction limits;
- Freeze repeat resistance;
- intent-reading value.

## Encounter 5 — Boss
- Black Banner Captain
- phase support as specified above

Tests the complete first-slice interaction set.

---

# 7. Four-player pressure additions

Do not scale normal prototype encounters by giving every enemy four times HP.

For larger parties, prefer:
- one additional enemy role;
- broader row pressure;
- an extra support unit that must be prioritized;
- mechanics that create two simultaneous problems;
- slightly increased boss outgoing damage and phase pressure per numeric skeleton.

Examples:
- Encounter 1 adds a second Cutthroat, not a 900-HP Crossbowman;
- Encounter 2 can add a Cutthroat so Shieldman protection has a meaningful beneficiary;
- Encounter 3 adds another Runner only if Reaction/event caps remain readable;
- boss Phase 2 adds a second support role rather than quadrupling Captain HP.

---

# 8. Class coverage matrix

| Class | Required prototype proof from this enemy set |
| --- | --- |
| Knight | Cutthroat/Execution Order obey Threat; Crossbowman and Vaulting Strike prove Threat is not absolute; Guard/Intercept protect direct hits; Sweep proves AoE cannot all be redirected; Breaker tools work on windups. |
| Duelist | Enforcer/Captain readable intent enables Feint/Parry/Opening play; Shieldman/Chirurgeon provide removable buffs; bounded Delay remains useful without replacing Oracle; boss Breakable windups reward timing. |
| Hunter | Runner movement triggers Snare/Snap Trap; back-row support gives companion/row pressure targets; Prey survives generic Cleanse; one-assist-per-cycle cap can be observed under high Speed; boss remains valid single-target Prey. |
| Marksman | Crossbowman/Chirurgeon create priority Back targets; Shieldman tests Break/armor-pressure Techniques; Driving Advance disrupts firing position without deleting Aim entirely; boss Exposed windows reward prepared shots. |
| Pyromancer | Chirurgeon healing makes anti-heal useful; Purging Salts pressures Burn maintenance; Captain accepts Burn in a long single-target fight; Combust/Ash loop works without kills; Phase 2 support provides optional multi-target value, not a requirement. |
| Cryomancer | Runner demonstrates Chill/Slow and normal Freeze value; Enforcer demonstrates diminishing hard CC; Captain demonstrates Freeze -> Break/Delay conversion; Ice Wall/barriers answer predictable row pressure; Shatter has non-damage Break value. |
| Priest | Hexer provides Poison/Bleed/Healing Reduction to Cleanse; boss row damage gives Regen/Group Heal value; Execution Order gives Guardian Hymn/rescue value; proactive Barrier can generate useful Grace before damage occurs; solo still has sustained pressure to heal/prevent. |
| Oracle | Enforcer/Captain expose layered intent; Premonition can answer predicted direct/status actions; Delay Fate is bounded by boss caps; support enemy buffs create Reversal/Dispel-style value; phase patterns make prediction useful without being mandatory. |

All eight have at least one ordinary enemy test and one elite/boss interaction. No class's core resource requires adds or kills.

---

# 9. Failure conditions for playtest

The enemy set should be considered **failed**, not merely difficult, if any of the following happens repeatedly:

- Knight can force essentially every boss attack onto itself with no target-rule exceptions.
- Back-row units are either effectively invulnerable or just as exposed as Front with no meaningful difference.
- one hard-control class can indefinitely delay the Captain.
- Break happens so frequently that major enemy windups never resolve, or so rarely that solo control builds cannot trigger it.
- Chirurgeon makes anti-heal mandatory rather than merely useful.
- generic Cleanse removes Prey/Marks and erases Hunter/Marksman setup.
- Shieldman/Barrier requires one specific class to defeat.
- Knife Runner Speed causes DoT/HoT/cooldown rules to visibly contradict each other.
- Hunter companion effectively acts as a second full party member.
- Priest must heal every turn and cannot spend stable turns on prevention/utility/offense.
- Oracle makes ordinary telegraphs redundant by revealing everything for free.
- Marksman becomes nonfunctional after one forced row change.
- Pyromancer's boss Ash economy still depends on Phase 2 adds.
- Cryomancer's Freeze becomes either full boss stun-lock or completely worthless.
- four-player boss fights become mostly inflated HP with no added tactical pressure.

---

# 10. Content deliberately not finalized here

Still Draft:
- enemy/faction names;
- lore and region placement;
- art/sprite silhouettes;
- exact rewards and loot;
- exact AI utility weights;
- exact boss HP/Power after simulation;
- number of adds at each party size;
- final boss ability names and presentation;
- PvP behavior of any status.

The prototype enemy set should be replaced/refined after simulation and actual play rather than promoted directly into production lore content.
