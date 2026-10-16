# Multiplayer and Parties

**Status:** Core party size, personal-loot philosophy, and endgame trade direction locked; world population, matchmaking, revive, and networking details remain Draft

## Core assumption

Rookvale is designed around meaningful multiplayer cooperation while remaining fully viable for solo progression.

The standard playable party is **1-4 players**.

Each human controls one persistent growing character. Rookvale is not a collectible-party RPG where one player commands a roster of interchangeable combat units.

## Desired social presence

Players should be able to encounter, travel, explore, and fight with other players in the world. Party play should extend naturally from exploration into turn-based combat.

## Party design principles

- Party roles create cooperation, not merely combined DPS.
- Joining friends should be straightforward.
- Standard exploration does not require a perfectly composed party.
- Harder content may deliberately reward specialization and coordination.
- Solo players retain a credible progression path.
- Four-player play may be somewhat more efficient socially and tactically, but it must not become roughly four times faster progression.
- Rewards do not rank players by DPS, healing, tanking, or other role-performance scores.

## Loot and trade

Detailed rules are defined in `MULTIPLAYER_LOOT_TRADE.md`.

Core locked direction:

- normal equipment and progression rewards use personal loot;
- XP, Class Mastery XP, Gold, and ordinary eligible rewards are not divided by party size;
- items earned together may be gifted to another eligible participant;
- gifting/trading cannot bypass Character Tier or personal progression requirements;
- early/mid-game high-end equipment cannot simply be mailed from veterans to new characters;
- mature endgame characters may directly trade eligible high-end equipment after legitimate progression has been earned;
- important boss/pinnacle Unique items may require the recipient's own clear/source eligibility before trade reception;
- normal endgame equipment can move through trade at most once before binding;
- Refinement/Reforge/Calibration and other personal investment normally bind the item;
- a universal global equipment auction house is not part of the default plan;
- progression-critical items remain non-tradeable.

The trade philosophy is:

> **allow RNG relief between qualified endgame players; do not allow trade to replace progression.**

## Keyed pinnacle encounters

For repeatable high-end encounters using an entry key/token/seal, every participating player must independently meet the progression requirement and possess their own valid access item.

One player's key never pays for the rest of the party.

Preferred consumption flow:

1. all participants' access items are validated/reserved when the attempt begins;
2. ordinary wipes do not permanently consume another access item;
3. one access item per reward-eligible participant is consumed when the clear/reward is successfully committed.

Exact disconnect/abandon handling remains Draft.

## Progression-gap handling

Rookvale does not generally down-scale veterans merely because they return to lower-Tier world content.

Veterans should be allowed to demonstrate accumulated strength and help newer friends in content those friends are legitimately eligible for.

At the same time:

- personal Character Tier controls progression-reward eligibility;
- over-Tier rewards are clamped or excluded;
- host/veteran progression does not substitute for another player's personal unlocks;
- progression-sensitive pinnacle encounters may use explicit personal eligibility gates.

Thus social carrying is allowed while progression skipping is not.

## Architecture consequences

Even before online networking is fully implemented, game state should remain conceptually separated into:

- player state;
- party state;
- world state;
- encounter/combat state;
- persistent progression state;
- personal loot/reward eligibility state;
- trade/gift binding state.

This prevents a single-player prototype from becoming structurally incompatible with multiplayer later.

## Open questions

- shared overworld population model;
- instanced versus shared combat spaces;
- revive/downed mechanics;
- matchmaking versus friend/invite emphasis;
- drop-in/drop-out behavior during exploration and combat;
- guild structure;
- commodity/material-market scope;
- PvP, if any;
- exact direct-trade UI and fees;
- character-bound versus account-bound final implementation;
- keyed-content disconnect/kick handling.
