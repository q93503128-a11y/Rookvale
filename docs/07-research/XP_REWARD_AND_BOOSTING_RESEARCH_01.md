# XP Reward and Boosting Research 01

**Status:** Research synthesis for progression reward eligibility and anti-boosting rules

## Question

Rookvale allows multiplayer parties and therefore cannot assume that every player fighting a high-tier enemy reached it at the intended progression point. A low-level player may be escorted or carried by an advanced player. The progression system must preserve cooperative play without allowing an endgame boss or monster to grant dozens of levels, endgame loot, or major unlocks to a character who has not personally reached the relevant progression band.

## Useful external patterns

### Final Fantasy XIV

Instanced duties use personal entry requirements such as character level, item level, and prerequisite unlocks. Being grouped with an eligible player does not replace a character's own eligibility. This is useful for major Rookvale dungeons, bosses, raids, and other progression content.

### Guild Wars 2

Open-world PvE generally scales strong characters downward in lower-level areas, but does not normally scale low-level characters upward simply because they enter a high-level zone. Dynamic events can also deny participation rewards when a character is far below the event's intended level. This demonstrates that cooperative access and reward eligibility can be treated separately.

### Path of Exile

Experience is penalized when the gap between player level and monster level is outside a safe range. Party XP distribution also prevents lower-level party members from simply inheriting the full high-level solo reward. This is a useful anti-boosting reference, although Rookvale should prefer simpler visible progression-tier rules over an opaque continuous formula.

## Rookvale synthesis

### Do not reward relative difficulty directly

Do **not** grant bonus XP merely because an enemy is above the player's current level. Otherwise the optimal leveling method becomes finding the strongest encounter that a high-level friend can carry.

Later content should already grant more raw XP because:

- later character levels require more XP;
- later monsters and activities have higher fixed reward budgets;
- later dungeons, bosses, quests, and discoveries are intended to advance later characters.

The reward budget belongs to the **content tier**, not to the difference between monster level and player level.

### Personal progression eligibility

Every character has a personal progression/reward tier representing how far that character has legitimately opened the world progression ladder. The final player-facing name is open; `Adventure Tier`, `World Tier`, or a more setting-specific term are candidates.

Important properties:

- eligibility is stored per character;
- party leader progression never substitutes for another player's progression;
- teleport, party join, summon, or following another player cannot silently unlock a higher reward tier;
- major first-clear rewards require the character's own unlock state.

### Reward clamp

When a character participates in content above their personally unlocked reward tier, the character does **not** receive the encounter's unrestricted high-tier progression reward.

Conceptually:

`EligibleRewardTier = min(ContentTier, CharacterUnlockedRewardTier)`

The exact formula and number of tiers remain Draft. The structural rule is locked: an over-tier encounter cannot pay a low-progression character as though that character were legitimately at the encounter's tier.

This clamp applies to:

- Character XP;
- Class Mastery XP;
- ordinary equipment tier;
- currency/material reward bands where appropriate;
- first-clear progression rewards;
- endgame currencies and progression tokens.

Unique cosmetics or social/fun rewards may be exceptions when they cannot accelerate combat progression.

### Major-content entry gates

Major progression content should normally require personal eligibility to enter or receive meaningful progression rewards:

- main/major dungeons;
- major bosses;
- raids or raid-like encounters;
- endgame challenge spaces;
- progression-critical world events;
- class or advancement trials where relevant.

A party member cannot bypass this by being invited by an eligible host.

### Open-world regions should not all be invisible walls

Rookvale is an exploration RPG. Do not turn every region border into an arbitrary level gate.

Use a mixed approach:

1. **Physically explorable dangerous regions** may allow an under-tier player to enter if they can reach them. The monsters remain dangerous and their progression rewards are clamped to the player's unlocked tier.
2. **Narratively or mechanically gated regions** may require a ferry route, repaired bridge, key, faction permission, environmental protection, quest milestone, dungeon clear, or other diegetic world unlock.
3. **Extreme endgame spaces** may use explicit hard personal unlocks because bypassing them would undermine both progression and encounter structure.

This preserves curiosity and sequence-breaking where harmless without making boosting optimal.

### High-level helpers in low-level content

The reverse problem also matters: an endgame player should not erase all low-level encounters while carrying a new player.

Prototype a **down-sync / mentor sync** for clearly banded lower-level content:

- core combat stats are reduced toward the area's intended range;
- the veteran may retain a broader toolkit and therefore still feel experienced;
- rewards remain appropriate to each character rather than being copied from the veteran's real level;
- exact stat-sync severity is deferred until equipment progression is designed.

Open-world sync does not need to make every veteran identical to a new character. Its purpose is to prevent trivial one-action clearing and keep cooperative play meaningful.

### Participation remains necessary but is not the main anti-boosting system

Rookvale should require meaningful encounter participation so an AFK character cannot receive full party rewards. However, participation checks alone cannot stop boosting: a low-level character could press one button while a veteran defeats the boss.

Therefore the anti-boosting stack is:

1. personal content eligibility;
2. personal reward-tier clamp;
3. personal first-clear/unlock state;
4. meaningful participation requirement;
5. down-sync for veterans in lower-tier content where appropriate.

### Loot rules

A low-progression character should not receive unrestricted endgame equipment merely because an eligible player carried them.

Prototype rules:

- progression-relevant loot is personal;
- loot tier is capped by personal reward eligibility;
- unique progression-critical boss loot requires personal encounter eligibility;
- trade rules, bind rules, and economy restrictions are deferred to the equipment/economy design phase.

## Rejected directions

- Bonus XP for fighting enemies above the player's level.
- Letting the party leader's unlock state grant full reward eligibility to everyone.
- Pure AFK/participation detection as the only boosting prevention.
- Hard-locking every open-world region solely by character level.
- Letting an under-tier player receive full endgame first-clear rewards and attempting to fix the resulting level jump afterward.

## Still Draft

- final name and number of progression/reward tiers;
- whether an adjacent next tier receives partial or full reward rather than a strict clamp;
- exact mentor-sync formula;
- how gear item level maps onto reward tiers;
- trade restrictions for items acquired through mixed-progression parties;
- exact participation rules;
- exact handling of optional world bosses that are physically reachable early.
