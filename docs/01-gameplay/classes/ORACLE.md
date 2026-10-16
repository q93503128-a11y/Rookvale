# Oracle

**Status:** Draft for review and prototype; not locked

**Lineage:** Acolyte -> Oracle

**Primary role:** Prediction / timeline support / buffs and debuffs

**Secondary roles:** Intent revelation, delayed protection, action-delay control, limited healing

## Class fantasy

Oracle wins by knowing what is about to happen and making that knowledge matter. It is not Priest with cards and not Chronomancer-lite.

The class should let the player:
- reveal or clarify future enemy intent;
- prepare allies for specific incoming action types;
- accelerate or delay bounded future actions;
- place delayed omens that pay off if predictions come true;
- alter buffs/debuffs and elemental/role states through fate manipulation.

Oracle must never generate infinite turns, cooldown loops, or mandatory manual turn-order negotiation for the party.

## Weapon compatibility

Inherited Acolyte pool:
- staves;
- holy/astral foci;
- tomes;
- selected light maces if desired for shared ancestry.

A visual star-globe/card focus may exist as a subtype without creating a separate loot economy unless later justified.

## Innate mechanic — Omens

Oracle maintains a small set of **Omen** charges/cards/states. Prototype cap: **3 Omens**.

Gain Omens through:
- correctly predicting or revealing an enemy action category;
- an Omen skill resolving as predicted;
- selected support actions;
- controlled natural-turn generation only if the final economy proves too inconsistent.

Spend Omens on timeline interventions, stronger predictive buffs, and Signature effects.

Omens are not random loot-box-style cards. If random presentation is used, the player must have enough control to avoid bad-draw frustration.

## Innate passive — Foresight

At the start of Oracle's natural turn, reveal additional information about one or more upcoming enemy actions beyond the game's normal telegraph layer.

Possible information:
- likely target row/category;
- attack/support/control classification;
- approximate damage severity;
- whether the action can be interrupted/cleaned/redirected;
- one resistance/weakness clue.

Bosses may intentionally obscure exact details while still exposing useful categories.

# Active skill pool

## 1. Foretell
**Type:** Prediction / Omen generation

Choose an enemy and predict a broad category for its next eligible natural action: Attack, Control, Support, Defense, or Special/Other.

If correct, gain Omen and apply a small benefit; if wrong, no catastrophic punishment.

### Technique candidates
- **Narrow Reading** — fewer categories, stronger reward, longer cooldown.
- **Open Reading** — more flexible prediction, smaller reward.
- **Shared Prophecy** — lower personal Omen gain, grants ally preparation benefit.

## 2. Premonition
**Type:** Ally protection

Choose one ally and one incoming action category. If that ally is affected by that category before Oracle's next natural turn, reduce the effect or grant barrier/resistance.

## 3. Delay Fate
**Type:** Timeline control

Spend 1 Omen to push one enemy's next-action point later by a bounded amount. Bosses receive reduced delay plus Break/telegraph benefit.

Cannot target the same boss repeatedly without diminishing/cooldown rules.

## 4. Favorable Hour
**Type:** Ally timeline support

Spend Omen to pull one ally's next-action point modestly earlier. This does **not** grant an immediate bonus turn and cannot move an ally ahead of hard encounter locks.

Strong internal cooldown and per-target limits.

## 5. Auspicious Sign
**Type:** Buff

Grant an ally a chosen omen effect from a small deterministic set, such as:
- next direct attack gains precision;
- next heal/barrier gains efficiency;
- next control application gains reliability;
- next incoming hit is partially reduced.

The player chooses; no mandatory random card fishing.

## 6. Ill Omen
**Type:** Debuff

Apply a predictive debuff to an enemy. When it next performs a specified action type, trigger a penalty such as reduced damage, Speed loss, exposed state, or Break.

## 7. Read the Thread
**Type:** Information / utility

Reveal deeper information on one enemy: resistance category, cooldown/intent clue, or whether its next telegraph is interruptible. Gain a small Omen if the revealed information is acted upon successfully.

## 8. Reversal
**Type:** Buff/debuff manipulation

Convert or invert one limited eligible combat state:
- weaken a buff into neutral state;
- cleanse a mild debuff and replace it with a smaller cost;
- convert an enemy haste-like state into normal timing;
- convert ally slow into brief stability.

Cannot flip unique boss mechanics or every status type.

## 9. Horoscope
**Type:** Delayed support

Place Horoscope on one ally. If that ally receives healing/barrier/support before expiry, Horoscope upgrades. Recast/expiry releases a delayed heal/barrier based on upgrade level.

This creates planned support rather than instant healing spam.

## 10. Constellation Ward
**Type:** Party utility

Apply a limited party ward keyed to one selected category: control, debuff, direct attack, or elemental/status family. The first few eligible events receive reduced effect.

## 11. Fate's Needle
**Type:** Attack / setup

Modest astral damage. Deals bonus utility against enemies with active Ill Omen/Foretell states and can generate minor Break or Omen progress.

## 12. Starfall Mark
**Type:** Delayed attack

Mark an enemy for a delayed astral strike after a bounded future action/event. If the enemy performs the predicted category before impact, the strike changes effect.

## 13. Borrowed Moment
**Type:** Cooldown utility

Spend Omen to reduce one **specific eligible skill cooldown** by a small bounded amount. Cannot affect Signature by default and cannot reduce below a minimum. Does not count as another natural turn.

## 14. Misfortune
**Type:** Enemy disruption

Apply a short state causing the next beneficial enemy secondary effect or buff generation to fail/weaken. Against bosses, converts into buff-duration reduction/Break if immunity applies.

# Reaction candidates

## Foreseen Harm
When an ally under Premonition is hit by the predicted category, trigger an additional small barrier or reduction. Once per Reaction cooldown.

## Twist of Fate
When an ally would receive a severe eligible debuff/control, spend Omen to reduce its duration/severity. Does not erase unique boss mechanics.

## Prophetic Reprieve
When Oracle is directly targeted by an action that had been revealed by Foresight, gain a small barrier/Omen refund. Rewards correct information use.

# Signature candidates

## Written in the Stars
For a bounded sequence of upcoming actions, Oracle reveals much deeper timeline/intent information and may perform a limited number of Omen interventions at reduced cost. It does not freeze time or grant extra full turns.

## Rewrite Fate
Select one major upcoming enemy action that is explicitly eligible. Instead of cancelling it, change one parameter: target weighting, severity, secondary effect, or timing. Boss/scripted actions may offer a predefined set of rewrite options rather than full freedom.

# Selectable passive candidates

- **Clear Skies** — first correct Foretell each cycle grants extra Omen.
- **Bad Moon** — Ill Omen penalties stronger; ally buffs weaker.
- **Benefic Aspect** — Auspicious Sign and Horoscope stronger; enemy timeline control weaker.
- **Measured Intervention** — timeline adjustments smaller but cheaper/more frequent.
- **Fixed Point** — fewer interventions, stronger single Delay/Favorable Hour effects.
- **Second Sight** — Foresight reveals an additional secondary clue on elites/bosses.
- **Astrologer's Patience** — delayed effects like Horoscope/Starfall gain stronger payoff if allowed to fully mature.
- **Conjunction** — when two different Oracle predictive effects trigger in one enemy action, gain a capped extra Omen benefit.
- **Unlucky Star** — buff removal/weakening grants small Break.
- **No Paradox** — Borrowed Moment cannot target the same skill consecutively but gains stronger reduction when switching targets; explicit anti-loop passive.

# Randomness policy

Oracle can use cards/stars/omens visually, but core performance should not hinge on drawing a rare good card.

If randomness exists:
- outcomes must all be useful;
- player can hold, choose, cycle, or convert results;
- multiplayer allies should not suffer because Oracle rolled badly;
- high-end planning should come from prediction, not casino variance.

# Solo viability

Oracle can debuff enemy actions, manipulate timeline modestly, use Fate's Needle/Starfall for damage, and protect itself through prediction. It should kill more slowly than DPS classes but not depend on allies to make Omen function.

# Party identity

Oracle brings:
- superior intent information;
- predictive mitigation;
- buffs/debuffs;
- bounded action timing manipulation;
- delayed support;
- cooldown utility;
- boss-mechanic preparation.

It should complement Priest rather than replace it: Priest repairs/prevents HP/status damage directly, Oracle prevents problems through prediction and timing.

# Prototype questions

- how much intent information the base UI already exposes before Oracle bonuses;
- exact Omen cap/generation;
- safe bounds for Delay Fate/Favorable Hour;
- whether Borrowed Moment belongs in first slice or should wait until cooldown balance is stable;
- deterministic versus semi-random Omen presentation;
- how Rewrite Fate interacts with boss scripts;
- whether Oracle has too much system complexity for an early class and needs staged skill unlocks.
