# Progression Rewards

**Status:** Core reward philosophy locked; exact XP curves, progression-tier count, and sync numbers remain Draft

## Core rule

Rookvale does **not** grant bonus experience simply because an enemy is above the player's current level.

Later content is naturally more efficient because later monsters, quests, dungeons, bosses, discoveries, and events have larger fixed reward budgets that correspond to the later progression curve.

The reward is defined by the content's intended progression tier, not by `enemy level - player level`.

## Character XP

Character XP represents overall adventure progression.

Primary sources include:

- combat;
- quests;
- exploration and meaningful discoveries;
- dungeons;
- bosses;
- world events;
- major challenges and progression milestones.

Ordinary repeatable monster combat remains a valid steady source but should not automatically dominate exploration, questing, first clears, and other handcrafted content.

Later content gives more raw Character XP than early content. Exact reward tables remain Draft until the world and level curve are defined.

## Class Mastery XP

Class Mastery XP represents experience using the currently equipped class in meaningful combat and challenge content.

Primary sources include:

- completed combat encounters;
- Elite and Boss encounters;
- dungeon progression and clears;
- combat-focused events;
- Class Trials;
- class-specific quests and challenges.

Class Mastery is not primarily awarded for repetitive button usage. Rookvale does not use rules such as `Guard 20 times` or `cast Heal 50 times` as the default advancement engine.

Party members who meaningfully participate in the same eligible encounter receive the intended baseline Mastery reward without competing over DPS, healing, or tank statistics.

## Personal progression / reward tier

Every character has a **personal progression eligibility tier**. The final player-facing name is open.

This tier determines which progression reward band that character has legitimately unlocked.

Structural rules:

- it belongs to the individual character;
- another party member's progression cannot replace it;
- party invitations, teleports, summons, and following a veteran do not grant a higher tier;
- major encounter first-clear eligibility remains personal;
- later tiers are opened by legitimate world/content progression rather than by killing a single overleveled monster.

## Over-tier reward clamp

A character may sometimes physically reach or participate in content above their unlocked progression tier. This must not produce unrestricted late-game progression rewards.

Conceptually:

```text
EligibleRewardTier = min(ContentTier, CharacterUnlockedRewardTier)
```

The precise implementation may later include adjacent-tier grace rules, but the invariant is fixed:

> **A low-progression character cannot receive the full progression value of extreme endgame content merely because another player carried the encounter.**

The clamp can apply to:

- Character XP;
- Class Mastery XP;
- ordinary equipment reward tier;
- progression currencies and materials;
- endgame tokens;
- first-clear progression rewards.

Purely cosmetic/social rewards may be exempt where they cannot accelerate combat progression.

## Major encounter eligibility

Major progression encounters normally require the character's own unlock state.

Examples:

- major dungeons;
- progression bosses;
- raids or raid-like challenges;
- extreme endgame spaces;
- progression-critical world events;
- class advancement trials.

An eligible host cannot simply invite an ineligible character and grant them full entry/rewards.

Exact level, quest, region, equipment, or milestone requirements are content-specific and remain Draft.

## Region access philosophy

Do not solve boosting by placing an arbitrary invisible level wall around every region.

Rookvale uses a mixture of three access patterns.

### 1. Dangerous but physically accessible

Some higher-level wilderness can be reached early by a curious player.

- enemies are genuinely dangerous;
- the player is not automatically scaled upward;
- over-tier rewards remain clamped;
- reaching the location early is allowed to be an exploration achievement rather than a leveling exploit.

### 2. Diegetic world gates

Some areas unlock through world progression such as:

- repairing or opening a route;
- obtaining a ferry/ship route;
- a key or seal;
- faction permission;
- environmental protection;
- clearing a dungeon or boss;
- completing a quest or world-state milestone.

These gates should feel like part of the world rather than a generic `Level 50 required` wall whenever possible.

### 3. Hard endgame gates

Extreme endgame regions and encounters may require explicit personal progression access where sequence-breaking would undermine progression or encounter design.

This is acceptable for content whose identity depends on the player already completing earlier systems.

## High-level players helping lower-level players

Rookvale should support veterans playing with newer friends without making low-level content meaningless.

Prototype a **down-sync / mentor-sync** rule for clearly tiered lower-level content.

Goals:

- reduce veteran core combat stats toward the area's intended band;
- preserve enough skills and build identity that the veteran still feels like their character;
- prevent one-action clearing from becoming the default carry method;
- award each player rewards appropriate to their own progression state.

Exact synced stats, equipment handling, and whether all open-world regions use sync are deferred to the equipment/world design phases.

## Participation

Meaningful participation is required for normal party rewards. AFK presence alone should not qualify.

However, participation checks are **not** the primary anti-boosting mechanism. A carried character could otherwise perform one trivial action and receive an endgame reward.

Therefore boosting prevention uses several layers together:

1. personal unlock eligibility;
2. personal reward-tier clamp;
3. personal first-clear state;
4. participation requirement;
5. veteran down-sync where appropriate.

## Class Mastery pacing

The earlier Class Mastery direction remains:

- early Mastery ranks are fast;
- the class's core combat loop becomes available quickly;
- later Mastery increasingly unlocks build breadth rather than raw stat necessity;
- important milestones may use Class Trials;
- Max Mastery is not a prerequisite for the class to have level-appropriate base combat power;
- mastering unrelated classes must not become a mandatory source of universal combat stats.

## Explicitly rejected

- higher-level enemy = automatic bonus XP;
- endgame carry kills granting unrestricted endgame XP to new characters;
- host progression substituting for every party member's progression;
- role-performance XP competition between tank/healer/DPS;
- repetitive skill-use grinding as the main Class Mastery engine;
- hard character-level walls around every open-world zone.

## Open numbers and implementation questions

- final Character Level cap;
- exact XP curve;
- exact Class Mastery rank count and XP curve;
- progression/reward-tier count and names;
- exact reward budgets by activity;
- whether one adjacent locked tier receives partial grace rewards;
- exact veteran down-sync model;
- exact participation threshold;
- equipment and trading interaction with personal reward eligibility.
