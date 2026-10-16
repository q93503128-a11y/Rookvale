# Equipment Foundation

**Status:** Core equipment philosophy and stat/affix architecture locked; exact numeric budgets, upgrade/crafting costs, drop rates, and final rarity names remain Draft

## Core philosophy

Rookvale is not a loot-flood ARPG. Equipment should be readable, meaningful, and obtainable at a pace that prevents progression gaps without showering the player in disposable weapons and armor after every encounter.

The design separates three concepts:

- **Equipment Tier** = the progression band / baseline power generation of an item.
- **Rarity** = how unusual, complex, or mechanically distinctive the item is.
- **Unique identity** = hand-authored effects that can enable or reshape builds.

Equipment Tier and Rarity are not the same axis.

Detailed stat and affix rules are defined in `EQUIPMENT_STATS_AFFIXES.md`.

## Equipment slots

Current foundation:

- Main Hand
- Off Hand
- Head
- Chest
- Hands
- Legs
- Feet
- Amulet
- Ring 1
- Ring 2
- Relic

Two-handed weapons occupy Main Hand and Off Hand together.

Weapons follow class / lineage compatibility more strongly than armor. Armor may carry Light / Medium / Heavy-style identities or tags, but these should primarily shape stats and build tendencies rather than act as universal hard class locks.

## Equipment Tier

Equipment Tier tracks the Character Tier progression ladder.

A Tier V item belongs to the Tier V progression band even if its rarity differs from another Tier V item.

Higher Equipment Tiers should have meaningfully larger baseline stat budgets and may expose later affix families, later crafting materials, and later Unique designs.

A low-Tier item should not normally be upgraded until it becomes equivalent to a much later-Tier item.

### Why low-Tier Unique items do not scale forever

A Tier II Unique may be exceptional and memorable during Tier II progression, but it should not normally be transformed into a Tier VIII-equivalent Unique.

Reasons:

- later-Tier Unique items need their own reason to exist;
- new regions and bosses need desirable new rewards;
- permanent scaling of every early Unique would create a growing long-term balance burden;
- keeping old Uniques permanently best-in-slot would weaken the feeling of entering a new equipment generation.

Earlier Uniques may remain useful for special low-Tier content, collection, alternate builds, cosmetics, experimentation, or specific niche effects, but later progression should introduce genuinely stronger and more sophisticated Unique opportunities.

The game may later allow limited refinement within an item's own intended Tier/band, but not unrestricted Tier promotion by default.

## Rarity

Working rarity structure (names/colors are Draft):

- Common
- Uncommon
- Rare
- Epic
- Unique

Rarity does not mean a giant automatic baseline stat multiplier.

Within the same Equipment Tier, higher rarity primarily provides combinations of:

- additional affixes;
- rarer affix families;
- more specialized build hooks;
- hand-authored effects;
- distinctive visuals/lore;
- target-farm identity.

Working ordinary-item structure:

| Rarity | Structure |
| --- | --- |
| Common | Base / Implicit only |
| Uncommon | Base + 1 Minor |
| Rare | Base + 2 Minor |
| Epic | Base + 2 Minor + 1 Major |
| Unique | hand-authored Base + Unique rule package |

A well-matched Rare may therefore be preferable to a poorly matched Epic.

## Core stat direction

Ordinary equipment primarily works with a compact stat set.

Primary stats:

- Max HP;
- Power;
- Defense.

General secondary stats:

- Critical Chance;
- Critical Damage;
- Break Potency;
- Healing Potency;
- Barrier Potency.

Raw Speed is a controlled stat and is **not** part of the general random Minor Affix pool because of its compound impact on Natural-Turn frequency, cooldown cycling, resource cadence, and timeline behavior.

Rookvale does not add STR/INT/VIT/DEX intermediary attributes merely to convert them into these combat stats, and it does not reintroduce universal Accuracy/Evasion/Status-Hit itemization without a demonstrated combat need.

## Minor and Major Affixes

Ordinary equipment may use limited randomized affixes while avoiding long lists of narrow conditional percentages.

- **Minor Affixes** provide readable numeric or system-tag specialization.
- **Major Affixes** provide bounded mechanical hooks that influence play without rewriting an entire class.
- **Unique effects** may go further and create true build-around rule changes.

Minor Affix values may have a **small random roll range**. The affix family should matter more than whether the player rolled the absolute maximum value.

Example principle:

```text
Tier V Break Potency affix: +8% to +10%
```

Exact ranges remain Draft.

Prefer affixes tied to reusable combat systems and tags such as:

- Break;
- Barrier;
- Guard;
- Mark;
- Burn;
- Bleed;
- Frost;
- direct healing;
- Summon / companion;
- Reaction;
- Weapon actions;
- row / formation interactions.

Avoid bloating the pool with a separate narrow affix for every individual class where a reusable system-tag effect can serve several classes.

## Set items

Traditional multi-piece set equipment is **not part of the default Rookvale equipment plan**.

Rookvale should avoid 4-6 piece sets or other structures that reserve many equipment slots for one predefined package and reduce build mixing.

Armor-weight completion bonuses are also avoided; Light/Medium/Heavy pieces may be mixed freely unless a specific item explicitly says otherwise.

If a future exceptional item pair or narrative equipment combination is ever introduced, it should be treated as a special case rather than establishing a general set-item system.

## Unique equipment

Unique items are hand-authored build opportunities rather than merely ordinary items with much larger numbers.

A good Unique should make the player think:

> "I could build around this."

Unique effects may alter:

- class-resource rules;
- status consumption or retention;
- Guard / Intercept behavior;
- Break interactions;
- Reaction behavior;
- companion cadence;
- targeting / rows;
- cooldown / timeline interactions;
- specific lineage mechanics where a class-specific Unique is justified.

Class- or lineage-specific Unique equipment is allowed where it strengthens identity and the loot source is sufficiently targetable.

Low-Tier Uniques do not normally promote into later-Tier-equivalent Uniques. Later regions and bosses must retain their own desirable equipment identities.

## No equipment starvation

Rookvale distinguishes **baseline gear availability** from **high-value gear rarity**.

A player who has legitimately entered a Character Tier should not routinely be forced to play that Tier while mostly naked or wearing gear several Tiers behind simply because random drops failed.

Therefore each Tier should provide several dependable sources of serviceable current-Tier equipment.

Candidate baseline sources:

- Tier advancement / progression quest rewards;
- ordinary quest rewards;
- town merchants whose stock improves with progression;
- blacksmith / crafting recipes using reasonably available materials;
- common dungeon or chest rewards;
- guaranteed or strongly weighted first-clear equipment rewards;
- ordinary enemy drops.

These baseline items do not need to be optimal. Their purpose is to establish a healthy minimum gear floor.

High-quality Rare/Epic/Unique equipment can remain meaningfully rarer.

## Loot density

Equipment itself should not flood the screen after every battle.

A combat reward can still feel substantial through a mixture of:

- Character XP;
- Class Mastery XP;
- gold / currency;
- crafting materials;
- monster parts;
- consumables;
- trade / vendor items;
- quest items;
- collectibles;
- cosmetics;
- occasional equipment.

Thus fewer weapon/armor drops do not mean empty rewards.

## Targetability

Important equipment should not rely exclusively on a huge global random loot pool.

Rookvale should use multiple acquisition identities:

- specific boss Unique drops;
- specific monster-family materials/items;
- dungeon reward pools;
- exploration chests / secret areas;
- quests;
- merchants;
- crafting;
- world events;
- broad ordinary drops.

A player pursuing a particular build should usually have a plausible idea of where to look rather than only hoping the global random table produces it.

## Progression rule

Current-Tier baseline gear should be accessible enough that the player can function.

Current-Tier strong optimized gear should require more effort.

Current-Tier Unique gear should be exciting and meaningfully targetable but not assumed for ordinary progression balance.

This means encounter tuning must not assume the player already owns a rare Unique unless the content explicitly provides or requires it.

## Open questions

- exact numeric stat budgets by Tier and slot;
- exact Affix pools and exact random-roll ranges;
- exact rarity names/colors;
- final Light/Medium/Heavy base profiles;
- crafting and enhancement systems;
- rerolling/reforging/affix-editing rules;
- repair/durability policy;
- trading and binding policy;
- Unique drop protection / pity / deterministic acquisition;
- whether some Tier advancement quests guarantee a weapon appropriate to the equipped class;
- exact merchant catch-up rules;
- how duplicate Uniques are used;
- cosmetics/transmog relationship to retired low-Tier gear.
