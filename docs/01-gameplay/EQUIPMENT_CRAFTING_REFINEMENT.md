# Equipment Crafting, Refinement, and Pinnacle Acquisition

**Status:** Core philosophy locked; exact costs, refinement counts, recipes, drop rates, and pity thresholds remain Draft

## Core item journey

Rookvale treats the original item acquisition as meaningful and uses crafting primarily to secure baseline gear, refine strong finds, and reduce extreme bad luck.

The intended loop is:

```text
Acquire a useful item or crafting basis
-> optionally Refine it within its intended Tier budget
-> optionally Reforge one eligible Minor Affix slot
-> optionally Calibrate small numeric rolls
-> use it until a genuinely better or later-Tier replacement appears
-> sell / salvage / preserve its appearance when retired
```

Crafting should not turn every mediocre item into a perfect best-in-slot item, and Refinement should never promote an early-Tier item into the power generation of much later-Tier equipment.

## Refinement

Refinement is deterministic.

Rookvale does not use:

- upgrade failure;
- downgrade on failure;
- equipment destruction;
- durability loss as a routine equipment tax.

Refinement consumes Gold and appropriate materials and improves the item's existing base/implicit stat budget by a bounded amount.

Affix identity is not replaced by Refinement.

### Variable Refinement Caps

Different equipment categories and individual item templates may have different visible Refinement Caps.

Examples of the intended pattern:

- primary weapons may have relatively more Refinement steps;
- large armor pieces may have a moderate number;
- small accessories may have fewer;
- Relics and mechanically dense Unique items may have very few.

The exact cap numbers remain Draft.

The cap is always shown on the item, e.g. `Refinement 2 / 4`.

A larger number of steps does **not** automatically mean a larger total power budget. Step size and final bonus are balanced by slot/template so a five-step weapon does not gain disproportionate power merely because it has more clicks than a two-step ring.

The purpose of different caps is pacing, item identity, and material investment texture rather than creating a hidden rarity multiplier.

### Tier boundary rule

A fully refined lower-Tier item may remain comfortable during the opening portion of the next progression band, but Refinement does not allow it to leap several Equipment Tiers.

A Tier II Unique does not become a Tier IV-equivalent Unique because it was fully refined.

## Refinement is optional for ordinary progression

Unrefined current-Tier baseline equipment must remain sufficient for ordinary progression.

Refinement is primarily for:

- extending the life of an item the player likes;
- preparing for harder optional content;
- optimizing within the current Tier;
- investing in a strong Rare/Epic/Unique that the player expects to keep for a while.

If every usable item is assumed to be maximum Refinement, the system has failed and the maximum value has simply become the real baseline.

## Baseline crafting

Crafting provides deterministic access to serviceable current-Tier equipment.

Typical recipes use combinations of:

- regional materials;
- monster parts;
- profession / smithing materials;
- Gold;
- occasional recipe or blueprint unlocks.

A player who has legitimately reached a Character Tier should be able to obtain a functional weapon and core armor for that Tier without depending entirely on random drops.

Baseline crafting is not intended to print perfect optimized Epic items on demand.

## Drop identity versus crafting

Rookvale uses a **hybrid pinnacle-acquisition model** rather than declaring all best equipment either drop-only or craft-only.

The core rule is:

> **High-end content should provide the rare identity, ingredients, or item basis; crafting may finish, specialize, or deterministically assemble some pinnacle rewards.**

This preserves the excitement and world identity of boss/dungeon/exploration rewards while giving crafting and material collection a legitimate endgame purpose.

### 1. Pinnacle Unique drops

Some iconic build-defining Unique items are direct targetable drops from specific bosses, dungeons, world events, rare enemies, or exploration discoveries.

These are not generally reproducible from a universal crafting menu.

Reasons:

- bosses need memorable loot identities;
- discovering a named item should create an actual reward moment;
- later regions need exclusive reasons to be visited;
- a universal recipe catalogue would reduce many bosses to material vending machines.

Drop-only does not mean unbounded RNG. Duplicate protection, target farming, and deterministic bad-luck mitigation may still exist.

### 2. Forged pinnacle items

Some high-end items may instead be intentionally crafted from rare recipes plus materials obtained from demanding content.

Examples:

- a named weapon forged from parts of several endgame bosses;
- a high-Tier defensive item requiring a rare blueprint and dungeon material;
- a special Relic assembled after a quest or exploration chain.

These are bespoke crafted rewards, not generic recipes that can reproduce every direct-drop Unique.

This gives crafting its own prestigious endgame identity and supports long-form deterministic goals.

### 3. Optimized ordinary/Epic equipment

For non-Unique optimized gear, the desired pattern is often:

```text
strong item basis obtained from content
+
limited Reforge / Refinement / Calibration
=
near-perfect or best-in-slot ordinary/Epic item for a particular build
```

Thus the player still cares about finding a strong original item while crafting has real value in finishing it.

## No single-source best-in-slot doctrine

Rookvale should not make every build's final equipment come from one activity.

A mature endgame loadout may plausibly contain a mixture of:

- boss-drop Unique;
- dungeon Epic;
- crafted pinnacle item;
- quest/exploration reward;
- optimized random Rare/Epic;
- specialized Relic.

The exact mix differs by build.

This prevents the entire endgame from collapsing into either repetitive boss farming or menu crafting.

## Reforge

Ordinary eligible equipment may designate at most one Minor Affix slot as its Reforge slot.

Once an Affix slot is chosen for modification, the other Affix slots remain part of the original item identity.

Reforge presents a small set of valid replacement candidates from that item's slot/type pool rather than rolling blindly across an enormous global pool.

The player chooses one candidate or pays the appropriate cost to generate another set later.

The resulting Minor Affix value may use the same small random roll range as naturally dropped items.

### Major and Unique restrictions

By default:

- Minor Affix: one eligible slot may be reforged;
- Major Affix: effect identity cannot be freely replaced;
- Unique rule/effect: cannot be replaced by Reforge.

This keeps strong Major and Unique drops meaningful.

## Calibration

Calibration may reroll an Affix's numeric value **within the same existing Affix family and its small roll range**.

Example:

```text
Break Potency +8%  -> Calibration ->  +9%
```

Calibration does not change `Break Potency` into another Affix.

Because ordinary roll ranges are intentionally narrow, Calibration is optimization rather than mandatory progression.

## Unique item handling

Unique items keep their authored mechanical identity.

They may have:

- fixed Unique effects;
- fixed or narrowly rolled support stats;
- bounded Refinement appropriate to the individual item;
- limited numeric Calibration where explicitly allowed.

They do not use ordinary Reforge to become another Unique or replace their defining rule.

A lower-Tier Unique remains bounded to its intended equipment generation even after maximum investment.

## Duplicate Unique value

Duplicate Unique drops should retain value.

A duplicate may be salvaged into a special Unique-grade material used for combinations of:

- Unique numeric Calibration;
- high-Tier special crafting;
- deterministic bad-luck protection;
- acquisition of an uncollected item from a relevant target pool after sufficient investment;
- cosmetic or collection rewards.

Exact exchange rates and pity thresholds remain Draft.

The system should reduce extreme duplicate frustration without making the first drop meaningless.

## Salvage and selling

Unwanted equipment can be either sold or salvaged.

Salvage returns crafting/refinement materials based on item Tier, rarity, and category.

This ensures that an otherwise unusable equipment drop is not a total dead reward.

## Sockets and durability

The default equipment system does not add a universal gem/socket layer at this stage.

Rookvale already has Class skills, Passives, Techniques, Minor/Major Affixes, Unique effects, and Relics. A universal socket system would add another optimization layer before a demonstrated need exists.

Specific future items may use socket-like mechanics as a bespoke effect without establishing a universal system.

Routine equipment durability/repair is also excluded. Gold/material sinks are supplied by crafting, Refinement, Reforge, Calibration, and other progression systems instead.

## External design lessons retained

- Monster Hunter demonstrates deterministic forging/upgrading from monster materials and allows different equipment pieces to have different upgrade caps.
- Last Epoch preserves the value of powerful drops while letting players use crafting and Legendary conversion to improve/complete strong item bases.
- Diablo IV separates important dropped item identity from endgame customization systems such as Tempering and Masterworking.

Rookvale uses these as structural references only; exact currencies, numbers, and mechanics are original to Rookvale.

## Open questions

- exact Refinement Caps by slot/template;
- total maximum Refinement budget by Equipment Tier and slot;
- exact Refinement materials and Gold curve;
- crafting profession structure, if any;
- blueprint acquisition rules;
- exact candidate count and costs for Reforge;
- Calibration cost and whether some Affixes are non-calibratable;
- duplicate Unique salvage values and deterministic thresholds;
- exact distribution of pinnacle items across drop/craft/quest/exploration sources;
- trade/binding interaction with crafted and modified equipment.
