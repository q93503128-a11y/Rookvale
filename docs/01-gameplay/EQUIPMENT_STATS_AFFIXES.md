# Equipment Stats and Affixes

**Status:** Core stat/affix architecture locked; exact numeric budgets, affix ranges, final pools, and item-by-item tuning remain Draft

## Design goal

Rookvale equipment should be readable at a glance, offer meaningful build choices, and avoid turning item evaluation into a spreadsheet of many narrow conditional percentages.

The equipment model uses three layers:

1. **Base / Implicit** — the item's type identity and baseline stats.
2. **Minor Affixes** — small numeric specialization.
3. **Major Affixes** — bounded rule-changing effects that influence play.

Unique items sit above this ordinary structure and may use hand-authored build-around rules.

## Core equipment stats

The primary stats that ordinary equipment may grant are:

- **Max HP**
- **Power**
- **Defense**

Rookvale does not add redundant intermediary attributes such as STR/INT/VIT/DEX merely to convert them into the actual combat stats.

## Controlled stat: Speed

**Speed is deliberately restricted.**

Because Speed increases Natural-Turn frequency and therefore indirectly affects action frequency, cooldown cycling, resource cadence, status timing, and timeline control, it has a much larger systemic impact than a simple offensive stat.

Rules:

- raw Speed is not part of the general random Minor Affix pool;
- ordinary gear cannot freely stack Speed across many slots;
- Speed may appear through controlled sources such as class profiles, selected fixed item implicits, limited Major Affixes, selected Unique items, passives, and temporary combat effects;
- long-term itemization must preserve the intended class-speed identities and prototype Speed bounds.

## Secondary equipment stats

The first general secondary-stat set is intentionally compact:

- **Critical Chance**
- **Critical Damage**
- **Break Potency**
- **Healing Potency**
- **Barrier Potency**

Exact formulas and caps remain Draft.

The initial equipment system does not introduce universal Accuracy, Evasion, Status Hit, Spell Accuracy, Physical Accuracy, Physical Penetration, Magical Penetration, or similar parallel rating systems unless later combat testing proves a concrete need.

## Base / Implicit identity

Base stats and implicits are determined primarily by the equipment type rather than fully randomized.

Examples:

```text
Tier IV Longsword
Power +34
Implicit: Weapon actions gain a small Break bonus.
```

```text
Tier IV Tower Shield
Defense +28
Max HP +80
Implicit: improves Guard-oriented protection.
```

The purpose is to ensure that a sword still reads as a sword and a defensive shield still reads as a defensive shield before random affixes are considered.

Exact implicits vary by weapon/armor family and remain Draft.

## Minor Affixes

Minor Affixes are simple numeric or narrowly scoped specializations.

Preferred examples include:

- Power;
- Max HP;
- Defense;
- Critical Chance;
- Critical Damage;
- Break Potency;
- Healing Potency;
- Barrier Potency;
- readable system-tag bonuses such as Burn, Bleed, Frost, Summon/Companion, Direct Heal, Weapon action, or Reaction bonuses when broadly reusable.

Avoid excessively narrow conditions such as:

> deal extra critical damage to a Chilled enemy while the player is in the Back row and above a specific HP threshold.

A Minor Affix should usually be understandable without checking several other combat conditions.

## Small random rolls are allowed

Minor Affix values may have a **small random roll range**.

Example:

```text
Tier V Break Potency affix: +8% to +10%
```

The purpose is to create some excitement from a particularly good roll without making decimal optimization the main progression game.

Rules:

- ranges should be narrow enough that the affix family matters more than the exact roll;
- the worst valid roll should still be a legitimate version of the affix rather than vendor trash created by bad RNG;
- Rookvale should not rely on huge overlapping random ranges where a lower-rarity item can become nearly unusable solely because every value rolled badly;
- exact ranges are tuned by Tier and affix family later.

## Major Affixes

Major Affixes create a bounded mechanical hook rather than only a larger percentage.

Examples:

- successful Guard strengthens the next Barrier;
- Breaking an enemy reduces the action delay of the next eligible Weapon skill, with an explicit cadence limit;
- when a Barrier is fully consumed, the next Direct Heal is stronger;
- a Reaction interacting with a Mark may preserve the Mark under a limited condition;
- changing rows may empower the next eligible Break-oriented action.

Major Affixes should:

- be readable;
- have explicit trigger and cadence rules;
- avoid recursive loops;
- avoid granting unrestricted extra Natural Turns;
- respect the global Break/Delay/Reaction caps;
- remain weaker and narrower than a true Unique build-around effect.

## Rarity structure

Working ordinary-item structure:

| Rarity | Structure |
| --- | --- |
| Common | Base / Implicit only |
| Uncommon | Base + 1 Minor |
| Rare | Base + 2 Minor |
| Epic | Base + 2 Minor + 1 Major |
| Unique | hand-authored Base + Unique rule package |

Exact rarity names/colors remain Draft.

Rarity is not a giant automatic base-stat multiplier. A well-matched Rare may be preferable to a poorly matched Epic.

## Affix pools by slot family

Affix pools should differ by equipment family rather than allowing every stat/effect on every slot.

### Weapons

Emphasize:

- Power;
- Critical;
- Break;
- Weapon-action effects;
- offensive statuses;
- offensive Major Affixes.

### Shields / defensive off-hands

Emphasize:

- Defense;
- Max HP;
- Barrier;
- Guard;
- Intercept;
- Threat/protection interactions.

### Armor

Emphasize:

- Max HP;
- Defense;
- limited Power where appropriate;
- Barrier/Healing support;
- status-response effects;
- row/formation interactions.

### Rings / Amulets

Emphasize specialization rather than large base stats:

- Crit;
- Healing;
- Barrier;
- Break;
- status-system tags;
- class-resource-compatible generic hooks;
- Reaction and utility interactions.

### Relics

Relics use relatively low raw-stat budgets and stronger mechanical identity.

They are intended as an experimentation/build-expression slot and can host stronger Major-style rules, while still remaining below the identity-rewriting scope of the most specialized Unique items unless the Relic itself is Unique.

## Armor weight families

Light / Medium / Heavy are equipment identities rather than complete-set requirements.

Players may mix pieces freely unless a specific item explicitly says otherwise.

Working tendencies:

- **Heavy:** high Defense/HP, protection/threat-oriented affix access.
- **Medium:** balanced offense/defense, Crit/Break/weapon-action affinity.
- **Light:** lower Defense, stronger support/status/resource/utility affinity.

There are no default full-armor-type completion bonuses and no hidden set mechanic for wearing five pieces of one weight.

## Two-handed versus one-handed + off-hand

Two-handed weapons must not be penalized merely because they occupy both hand slots.

Design principle:

> A two-handed setup and a one-handed + off-hand setup should have comparable overall item-budget potential while offering different build expression.

Working identity:

- **Two-handed:** concentrated Power/Break/implicit identity, fewer independent pieces to mix.
- **One-handed + off-hand:** more modular combination of offense/defense/support effects across two items.

Exact affix-count and stat-budget compensation is Draft and must be tested rather than assumed.

## Unique boundary

Unique items may change the rules of a class or system in ways ordinary Major Affixes should not.

Examples include:

- changing how a class resource is created or consumed;
- changing how a Signature/Reaction interacts with a status;
- retaining a normally consumed status under a meaningful tradeoff;
- restructuring a companion cadence;
- substantially changing a Guard/Intercept/Break loop.

Unique items do not simply equal `Epic + larger numbers`.

## Rejected directions

- general random Speed stacking across many slots;
- very large stat dictionaries;
- universal Accuracy/Evasion/Status-Hit itemization without demonstrated need;
- several nested conditional damage percentages per item;
- wide random-roll ranges where the same affix can be excellent or nearly worthless;
- full armor-weight completion bonuses that recreate a set system;
- Epic rarity automatically invalidating every Rare in the same Tier;
- Major Affixes that recursively grant extra Natural Turns or bypass global combat safeguards.

## Open questions

- exact numeric stat budgets by Equipment Tier and slot;
- exact random-roll ranges;
- exact Critical/Break/Healing/Barrier formulas and caps;
- full Minor Affix pool;
- full Major Affix pool;
- exact item-type implicits;
- two-handed versus dual-item budget coefficients;
- crafting, enhancement, rerolling, reforging, and affix-editing rules;
- duplicate Unique handling;
- trading/binding interactions with rolled equipment.
