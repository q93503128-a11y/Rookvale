# Multiplayer Loot, Gifting, and Endgame Trade

**Status:** Core loot ownership, gifting, endgame trade, binding, and keyed-entry rules locked; exact trade UI, fees, and endgame unlock threshold remain Draft

## Core philosophy

Rookvale uses multiplayer loot rules that support cooperation without turning veteran wealth into a way to skip the progression ladder.

The intended hierarchy is:

- normal multiplayer rewards are personal;
- party members can help each other with loot earned together;
- early/mid progression cannot be bypassed by veterans mailing high-Tier equipment to new characters;
- mature endgame characters may trade eligible equipment with other equally qualified endgame characters;
- trading exists primarily to reduce duplicate/RNG frustration, not to replace boss, dungeon, quest, or exploration progression.

The guiding rule is:

> **Trade may reduce bad luck after progression has been earned; trade may not substitute for earning progression eligibility.**

## Personal loot

Equipment and major combat rewards use personal loot by default.

A boss defeated by several party members does not create one shared item that the party rolls Need/Greed on. Each eligible player receives their own reward roll.

Personal rewards can include:

- equipment;
- Character XP;
- Class Mastery XP;
- Gold;
- ordinary materials;
- eligible boss/dungeon materials;
- personal first-clear rewards.

Rewards are not divided by party size and are not ranked by DPS, healing, tanking, or another role-performance score.

Meaningful participation and personal progression eligibility still apply.

## Party gifting

An item obtained while playing together may be gifted to another eligible member of that same participating group.

The recipient must satisfy all relevant requirements, including where applicable:

- participation in the encounter / eligible reward event;
- required Character Tier;
- required personal content unlock;
- required source-clearance condition for source-locked pinnacle equipment.

This supports natural cooperation such as a Knight giving a newly dropped bow to a Hunter who fought the same boss.

Party gifting does not allow a veteran to farm unrelated late-game content alone and later send its progression equipment to an ineligible low-Tier character.

## Endgame direct trade

High-end equipment trading is unlocked only in the mature endgame progression band. The current progression draft suggests the Tier VIII era, but the exact final unlock threshold remains Draft until the full endgame structure is designed.

Endgame direct trade exists for characters who are already legitimately established at that progression level.

Examples of intended use:

- two endgame players exchange duplicate build pieces;
- a player with repeated sword drops trades for another player's repeated bow;
- an eligible player buys or exchanges an ordinary endgame Rare/Epic from another eligible endgame player;
- a player who has already cleared a boss can acquire that boss's Unique from another qualified player instead of relying indefinitely on RNG.

The system is not intended to let a character buy their way through untouched progression content.

## Source Clearance

Important source-identity equipment may require a **Source Clearance** before it can be received through trade.

Example:

```text
Abyss King's Greatsword
Tier VIII Unique

Trade receive requirements:
- Character Tier VIII
- Abyss King clear recorded
- Abyss King reward eligibility unlocked
```

The exact label is Draft, but the rule is locked.

Source Clearance is appropriate for equipment whose identity depends strongly on its originating content, such as:

- pinnacle boss Uniques;
- raid-like encounter Uniques;
- secret-dungeon pinnacle drops;
- progression-significant crafted pinnacle equipment whose recipe/material chain proves equivalent progression.

Ordinary endgame Rare/Epic equipment does not need source-specific clearance unless the item is intentionally progression-sensitive.

This ensures that trading mitigates RNG for players who have already proven eligibility instead of replacing the underlying content.

## Trade transfer limit and binding

Eligible equipment may move between players at most once through normal endgame trade.

After a trade completes, the item becomes bound to the receiving character/account according to the final binding implementation and cannot be traded onward through the normal market loop.

This prevents chains such as:

```text
A -> B -> C -> D -> resale speculation
```

The intended market is based on actual use and duplicate exchange rather than unrestricted item-flipping.

### Modification binding

The following normally bind an item before it can be traded:

- equipping / using the item where binding is defined;
- Refinement;
- Reforge;
- Calibration;
- other irreversible item personalization.

Thus a player chooses whether to preserve a fresh valuable drop for gifting/trading or invest in it for personal use.

Exact account-bound versus character-bound details remain Draft.

## No global equipment auction house by default

Rookvale does not initially plan a universal searchable equipment auction house / trading post.

Endgame trading is initially conceived as direct player-to-player exchange.

Reasons:

- a universal catalogue could turn boss/dungeon exploration into a Gold-shopping problem;
- direct trade keeps the system social and bounded;
- the project can later add trade boards or broader market infrastructure if real play demonstrates a need.

General commodity/material market design remains a separate economy question.

## Item-category trade rules

### Generally tradeable / low-risk candidates

Depending on the later economy design:

- common monster materials;
- ore, wood, herbs, and ordinary crafting materials;
- food ingredients;
- ordinary consumables;
- vendor/trade goods.

### Party-gift / endgame-trade candidates

- Rare equipment;
- Epic equipment;
- most eligible Unique equipment;
- certain crafted pinnacle items after all recipient requirements are met.

### Non-tradeable progression items

Progression itself is not a commodity.

Normally non-tradeable:

- Character Tier promotion items;
- class-advancement quest items;
- personal progression keys/tokens;
- first-clear progression rewards;
- progression-critical endgame currencies;
- quest keys and world-state unlock objects.

## Keyed endgame content

For repeatable high-end content that uses an entry key, seal, invitation, token, or equivalent access material, **every participating player must possess their own valid entry item**.

Example:

```text
4-player Abyss King party

Player A: key yes
Player B: key yes
Player C: key yes
Player D: key no

=> party cannot begin the keyed encounter
```

One player's key never funds reward access for the rest of the party.

This prevents party size from multiplying the reward value of a single entry cost and prevents free riding into keyed pinnacle farming.

### Key validation and consumption

The preferred rule is:

1. validate and reserve every participant's key when the encounter begins;
2. do not permanently consume it merely because the group entered or wiped during a legitimate attempt;
3. consume one key from every reward-eligible participant when the encounter is successfully cleared / its completion reward is committed.

This allows learning attempts without making each wipe consume another expensive access item while preserving the intended per-player cost of successful farming.

Disconnect/abandon edge cases will be defined later so this rule cannot be exploited.

## Key transferability

A progression-critical entry key cannot be traded if doing so would allow another character to bypass the personal unlock path that the key is meant to represent.

Purely farm-oriented endgame access materials may later be commodity-tradeable only if the surrounding economy and progression gates remain safe. Even in that case, every party member still needs their own key and their own progression eligibility.

## Smart Loot interaction

Rookvale uses soft rather than absolute Smart Loot.

The currently equipped class / compatible lineage may receive higher ordinary-drop weighting, but unrelated gear can still appear.

This supports:

- future class changes;
- party gifting;
- endgame trade;
- salvage choices.

Boss-specific Unique identity should not disappear merely because the current class cannot use the item.

## Duplicate Unique interaction

Duplicate Uniques have several possible values:

- gift to an eligible party member who participated in the source encounter;
- trade to a qualified endgame character if the item is trade-eligible;
- salvage into Unique-grade material;
- contribute to deterministic duplicate/bad-luck protection.

This keeps duplicate drops meaningful without making unrestricted resale mandatory.

## Anti-boosting invariants

The following rules remain fixed:

- Character Tier requirements cannot be bypassed through gifting or trading;
- required personal progression cannot be replaced by the seller's progression;
- source-locked pinnacle items require the recipient's own Source Clearance;
- progression-critical items remain non-tradeable;
- a low-Tier character cannot receive late-game equipment simply because a veteran owns duplicates;
- keyed pinnacle content requires every participant's personal access cost and eligibility.

## Open questions

- final endgame Tier at which unrestricted eligible equipment trade first unlocks;
- direct-trade UI and confirmation flow;
- Gold/item barter versus both;
- transaction fee / tax, if any;
- character-bound versus account-bound final semantics;
- whether an untouched traded item may be gifted back in a short mistake-recovery window;
- commodity-market scope for ordinary materials;
- exact Source Clearance labels and UI;
- disconnect, kick, and abandon handling for reserved keys;
- whether certain pinnacle crafted items are never tradeable despite equivalent clearance.
