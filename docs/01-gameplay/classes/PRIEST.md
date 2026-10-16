# Priest

**Status:** Draft for review and prototype; not locked

**Lineage:** Acolyte -> Priest

**Primary role:** Healing / prevention / cleanse

**Secondary roles:** Rescue, regeneration, limited holy damage, defensive support

## Class fantasy

Priest is not a character who spends every turn pressing the largest heal. Good Priest play alternates between preventing damage, repairing damage, cleansing, preparing recovery, and contributing modest pressure when the party is stable.

The key tension is:
**heal now vs. prevent the next hit vs. prepare delayed recovery vs. cleanse/control the danger source**.

## Weapon compatibility

Inherited Acolyte pool:
- staves;
- maces;
- holy foci/books;
- shields where the build supports a defensive Priest.

## Innate mechanic — Grace

Prototype cap: **5 Grace**.

Gain Grace from useful support events:
- healing an ally who was meaningfully injured;
- preventing meaningful damage with a barrier/ward;
- cleansing a harmful status;
- selected proactive support skills.

Overhealing a full-health target does **not** freely generate Grace.

Grace is spent on emergency rescue, stronger prevention, revival-related effects, or Signature setup.

## Innate passive — Mercy with Purpose

Healing that would significantly overheal converts a capped portion into **Sanctuary**, a small temporary barrier, only if the target was actually injured before the heal.

This prevents waste without encouraging spam-healing healthy allies.

# Active skill pool

## 1. Mend
**Type:** Direct heal

Reliable single-target healing with low cooldown/resource burden.

### Technique candidates
- **Focused Mend** — stronger single-target heal, longer cooldown.
- **Gentle Mend** — lower immediate heal, adds Regeneration.
- **Purifying Mend** — lower heal, removes one minor negative status.

## 2. Prayer of Renewal
**Type:** Heal-over-time

Apply Regeneration for a bounded number of target natural turns or action events. Exact clock must be consistent with global duration rules.

## 3. Sanctuary
**Type:** Barrier / prevention

Spend Grace to create a significant barrier on one ally. Better before telegraphed damage than after it.

## 4. Group Prayer
**Type:** Party heal

Moderate healing across the party. Strong total output, weaker emergency single-target rescue.

Longer cooldown prevents it from dominating every turn.

## 5. Cleanse
**Type:** Status removal

Remove one or more eligible harmful effects. Stronger Techniques may specialize in DoT, control, curse, or disease families rather than cleanse everything at once.

## 6. Blessing
**Type:** Buff

Grant a temporary defensive/support boon such as control resistance, healing received, or protection against the next harmful secondary effect.

Does not become a generic all-stats buff.

## 7. Smite
**Type:** Attack / utility

Modest holy damage. Against marked/cursed/undead-like targets later, can gain class-specific utility, but first-slice version must remain generally useful.

## 8. Dazzling Prayer
**Type:** Control / prevention

Deal low holy damage and apply a soft accuracy/intent disruption or modest Break. Preventing damage is sometimes better than healing it afterward.

## 9. Guardian Hymn
**Type:** Prepared rescue

Choose one ally. If that ally takes a heavy eligible hit before Priest's next natural turn, restore a bounded amount afterward or grant an emergency barrier.

This is delayed insurance, not an automatic full heal.

## 10. Spirit of Restoration
**Type:** Persistent support

Summon/establish a temporary restorative spirit/effect that heals the party at bounded intervals. Only one major restorative spirit/state may be active at a time in first prototype to avoid stacking passive automation.

## 11. Purity Ward
**Type:** Prevention

Place a ward that blocks or reduces the next eligible control/debuff application on one ally.

## 12. Shared Burden
**Type:** Utility

Redistribute a small portion of damage/healing burden between two allies or convert part of an ally's incoming damage into delayed recoverable damage. Exact implementation should remain readable and not duplicate Knight Guard.

## 13. Emergency Grace
**Type:** Grace spender / rescue

Spend Grace for an immediate high-priority heal/barrier on a critically injured ally. Long cooldown and/or high Grace cost.

## 14. Benediction
**Type:** Support payoff

Spend Grace to grant a short party support window: improved healing received, control resistance, or limited barrier generation depending on Technique.

# Reaction candidates

## Saving Grace
When an ally would fall below a critical-health threshold from an eligible direct hit, spend Grace automatically to grant a small emergency barrier/heal. Long Reaction cooldown.

## Purifying Reflex
When an ally receives an eligible severe status, consume Grace to reduce its duration/severity. Does not automatically erase boss mechanics.

## Protective Prayer
When Priest is directly targeted, create a small self-barrier and gain limited Grace if meaningful damage was prevented.

# Signature candidates

## Miracle
A major party rescue: heal injured allies, stabilize critical allies, and apply a short prevention effect. Cannot fully erase failure or resurrect the entire party for free.

## Covenant of Life
Create a bounded support state in which healing, barriers and cleanse actions build toward one powerful rescue/revival effect. Rewards planned support rather than instant panic button only.

# Selectable passive candidates

- **Overflowing Mercy** — controlled overheal converts more efficiently into Sanctuary barrier.
- **Preventive Faith** — barriers/wards generate more Grace; direct heals generate slightly less.
- **Hands of Renewal** — Regeneration is stronger but direct burst healing lower.
- **Pure Heart** — cleansing grants a small heal or barrier.
- **Battle Chaplain** — Smite/Dazzling Prayer contribute modest Grace when they prevent/disable meaningful enemy pressure.
- **Last Rites** — emergency rescue tools stronger on critical allies, weaker above threshold.
- **Steady Hands** — heals are less affected by accuracy/disruption-like penalties.
- **Sheltering Hymn** — Guardian Hymn can protect a second nearby/row ally at reduced strength.
- **Graceful Economy** — high Grace cap and cheaper support spenders, but slower generation.
- **Radiant Reprieve** — after spending large Grace, Priest's next attack/support utility gains a small bonus so resource spend is not pure downtime.

# Revival policy

Priest may eventually have revival tools, but first prototype should be conservative:
- revival is expensive;
- does not erase wipe conditions;
- may require Signature/long cooldown/Grace;
- repeated revival loops are explicitly disallowed.

# Solo viability

Solo Priest must not be miserable. Smite, Dazzling Prayer, barriers, regeneration and self-healing create a slow but credible solo loop. Pure damage remains below dedicated DPS classes.

# Party identity

Priest brings:
- reliable direct recovery;
- proactive barriers;
- cleanse;
- delayed rescue;
- emergency stabilization;
- modest prevention/control.

It should be broader than a pure healbot while still remaining the first-slice benchmark healer.

# Prototype questions

- exact Grace gain rules and anti-overheal farming threshold;
- whether Group Prayer is too strong in 4-player parties;
- exact cleanse taxonomy;
- whether Spirit of Restoration uses target turns, Priest turns, or event ticks;
- first-slice revival availability;
- boundary between Priest and later Saint/Hierophant/Scholar branches.
