# Progression Rewards

**Status:** Core reward philosophy and initial Level/Tier structure locked; exact XP curves, Tier names, and numeric power steps remain Draft

## Core rule

Rookvale does **not** grant bonus experience simply because an enemy is above the player's current level.

Later content is naturally more efficient because later monsters, quests, dungeons, bosses, discoveries, and events have larger fixed reward budgets that correspond to later progression bands.

The reward is defined by the content's intended progression tier, not by `enemy level - player level`.

## Three progression axes

Rookvale exposes three distinct player-facing progression axes.

### Character Level

Frequent, granular permanent growth.

- represents ordinary character advancement;
- raises baseline combat capability according to the final stat-growth model;
- does not reset when changing class;
- progresses more frequently than Character Tier;
- uses automatic baseline stat growth rather than a mandatory manual STR/DEX/VIT-style point allocation layer.

### Character Tier

A visible major progression rank, not a hidden anti-boosting variable.

Character Tier communicates that the player has entered a stronger progression band and is now eligible for better content and better progression rewards.

A Tier increase should feel materially important. It may unlock or improve combinations of:

- the next Character Level band;
- higher-tier equipment;
- higher-tier crafting and growth materials;
- regions, dungeons, bosses, raids, or other content;
- new progression systems;
- a modest immediate increase to baseline character power.

Tier should not become one enormous multiplicative stat modifier that makes Character Level, class identity, and equipment irrelevant. It is a major milestone and permission layer with a noticeable power step.

### Initial launch-era Level/Tier structure

The current baseline is:

```text
Tier I      Lv. 1-10
Tier II     Lv.11-20
Tier III    Lv.21-30
Tier IV     Lv.31-40
Tier V      Lv.41-50
Tier VI     Lv.51-60
Tier VII    Lv.61-70
Tier VIII   Lv.71-80
```

This is the **initial progression plan**, not a permanent promise that the game can never expand beyond Lv.80 or Tier VIII.

Future expansions may raise the Character Level cap, add higher Character Tiers, or introduce another justified progression layer when sufficient new content exists. Do not reserve empty Tiers merely for hypothetical future expansion, and do not build the launch curve around endless vertical inflation.

A normal Tier promotion requires:

1. reaching the current Tier's level cap;
2. satisfying the appropriate personal world/progression milestone;
3. completing the Tier's Advancement Quest / Promotion Journey.

See `ADVANCEMENT_CONTENT.md` for the canonical advancement-content rules.

### Class Mastery

Class-specific breadth and mechanical depth.

- stored independently for each unlocked class;
- primarily unlocks skills, passives, Reactions, Signatures, Techniques, and additional build choices;
- does not require unrelated classes to be mastered for universal combat power;
- low Mastery does not erase the Character Level / Tier baseline needed to use a newly unlocked class in current content.

## Character stat-growth direction

Character Level and Tier provide baseline growth, but the player's currently equipped class determines how that baseline is expressed in combat.

The class used while gaining a level does **not** permanently alter future stat growth.

Changing from Knight to Pyromancer, for example, recalculates the level-appropriate baseline using the Pyromancer's class profile rather than preserving a permanently Knight-shaped growth history.

This avoids `I leveled with the wrong class, so my permanent stats are ruined` optimization traps.

The first prototype keeps the baseline stat vocabulary compact. Long-term itemization may later split some stats if testing justifies it.

### Speed caution

Speed is a high-leverage combat stat because it changes Natural-Turn frequency, cooldown cycling, resource cadence, and timeline pressure.

Therefore Character Level/Tier growth should not cause Speed to inflate on the same scale as HP / Power / Defense. Speed remains strongly class-profiled and tightly controlled through equipment, passives, and explicit effects.

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
- Class Trials / Advancement content;
- class-specific quests and challenges.

Class Mastery is not primarily awarded for repetitive button usage. Rookvale does not use rules such as `Guard 20 times` or `cast Heal 50 times` as the default advancement engine.

Party members who meaningfully participate in the same eligible encounter receive the intended baseline Mastery reward without competing over DPS, healing, or tank statistics.

## Character Tier eligibility

Every character has their own **Character Tier**.

This is visible to the player and is both a major growth milestone and the upper band of progression rewards the character has legitimately unlocked.

Structural rules:

- Character Tier belongs to the individual character;
- another party member's Tier cannot replace it;
- party invitations, teleports, summons, and following a veteran do not grant a higher Tier;
- major encounter first-clear eligibility remains personal;
- higher Tiers are opened by legitimate world/content progression rather than by killing a single overleveled monster;
- the UI should make Tier requirements visible before the player commits to difficult content.

## Over-tier reward clamp

A character may sometimes physically reach or participate in content above their Character Tier. This must not produce unrestricted late-game progression rewards.

Conceptually:

```text
EligibleRewardTier = min(ContentTier, CharacterTier)
```

The precise implementation may later include adjacent-tier grace rules, but the invariant is fixed:

> **A low-Tier character cannot receive the full progression value of extreme endgame content merely because another player carried the encounter.**

The clamp can apply to:

- Character XP;
- Class Mastery XP;
- ordinary equipment reward tier;
- progression currencies and materials;
- endgame tokens;
- first-clear progression rewards.

Purely cosmetic/social rewards may be exempt where they cannot accelerate combat progression.

## Tier-gated drops and disclosure

Tier requirements for meaningful drops must be shown **before** the player spends substantial effort pursuing them.

Examples of valid UI surfaces include:

- boss information pages;
- monster drop tables;
- dungeon reward previews;
- map or region information;
- item tooltips;
- encounter-entry warnings.

Example:

```text
Black Crown
Legendary Headgear
Obtainable: Character Tier VIII+
```

If a character below Tier VIII defeats that boss, the item is excluded from that character's eligible progression loot rather than visibly dropping and then becoming impossible to pick up.

If an encounter contains important rewards above the player's Tier, the UI should warn clearly before entry or engagement.

This rule exists to prevent a lower-Tier player from undertaking an extremely difficult fight under the false assumption that every displayed reward is currently obtainable.

## Recommended Tier vs required Tier

Rookvale distinguishes between **Recommended Tier** and **Required Tier**.

### Recommended Tier

A difficulty warning, not an access lock.

A lower-Tier character may enter where world traversal permits it. Enemies remain genuinely dangerous and the character is not scaled upward.

### Required Tier

A genuine progression requirement used only where sequence-breaking would undermine the progression or encounter structure.

Appropriate uses include:

- major progression dungeons;
- raids or raid-like encounters;
- extreme endgame spaces;
- progression-critical bosses;
- certain systems or reward tracks.

The distinction should always be visible in the UI.

## Region access philosophy

Do not solve boosting by placing an arbitrary invisible level wall around every region.

Rookvale uses a mixture of three access patterns.

### 1. Dangerous but physically accessible

Some higher-Tier wilderness can be reached early by a curious player.

- enemies are genuinely dangerous;
- the player is not automatically scaled upward;
- over-Tier rewards remain clamped;
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

These gates should feel like part of the world rather than a generic level wall whenever possible.

### 3. Hard progression gates

Extreme endgame regions and encounters may require explicit personal Character Tier / progression access where sequence-breaking would undermine progression or encounter design.

## Veterans in lower-Tier content

Rookvale does **not** automatically weaken high-level/high-Tier players merely because they enter an older region or lower-Tier encounter.

A veteran should be allowed to feel their accumulated power when returning to early content. This supports:

- visible long-term power growth;
- helping newer friends;
- social displays of strength;
- revisiting old regions for quests, collection, cosmetics, or completion;
- the simple fun of overwhelming enemies that used to be threatening.

Therefore there is no general open-world down-sync system.

Older regions also should not become the optimal source of current-Tier progression rewards. Their ordinary XP, equipment, and progression materials remain appropriate to their original band, so current-Tier content remains the efficient place to advance combat power.

Specific competitive, challenge, or normalized-content modes may define their own scaling rules later, but they are exceptions rather than the default world rule.

## Carrying / boosting philosophy

Rookvale allows social carrying as an activity but prevents it from skipping the progression ladder.

Examples:

- a strong veteran may help a lower-Tier friend clear content the friend is legitimately eligible for;
- the veteran is not automatically weakened and may clear it very quickly;
- a lower-Tier player who reaches extreme late-game content does not receive unrestricted late-game Character XP, Mastery XP, equipment, currencies, or progression drops;
- a veteran's unlock state does not substitute for personal Required-Tier or first-clear requirements.

The target is **allow the social carry; block the progression skip**.

## Advancement content and difficulty

Tier promotion and class advancement use dedicated advancement content rather than one universal menu exam.

Advancement may involve NPC quests, incidents, exploration, puzzles, preparation, combat, bosses, short dungeons, longer questlines, or combinations of these.

Mandatory advancement should require some understanding and execution, but it must not become an indefinite skill wall.

Normal character growth matters:

- current Level/Tier baseline applies;
- equipment and build improvements apply;
- preparation and permitted consumables may apply;
- Class Mastery/loadout improvements may apply.

A player who struggles can therefore become stronger and return rather than being stuck against a fully normalized fixed-stat test forever.

Repeated failure in mandatory instanced content may also unlock optional assistance such as stronger NPC help, clearer hints, temporary attempt-only buffs, or reduced mechanic intensity. Completing with assistance still counts as normal legitimate progression.

Optional prestige challenges may use harder or normalized rules separately.

See `ADVANCEMENT_CONTENT.md` for full rules.

## No hidden level-difference combat penalty

Rookvale does not need a universal hidden rule such as `60 levels under target = -90% damage / -80% hit chance`.

Higher-Tier enemies are difficult because their actual combat stats, mechanics, formations, status tools, and encounter design are stronger.

A lower-Tier player may defeat content above the intended band through exceptional play or preparation where access rules permit it, but the personal reward clamp still prevents this from becoming a progression skip.

## Launch-era level cap and later expansion

The current launch-era target is **Lv.80 / Tier VIII**.

At Lv.80, Rookvale does not default to an infinite Character Power level that permanently widens combat-stat gaps forever.

Long-term progression can instead continue through:

- equipment;
- Class Mastery;
- additional classes and lineages;
- build options;
- high-difficulty content;
- crafting, collection, exploration, and other systems.

Experience earned at the current cap may later feed repeatable non-mandatory rewards rather than infinite direct Character Power.

However, Lv.80 / Tier VIII is an initial cap, not an immutable lifetime maximum. A future expansion may raise it when the world and content genuinely justify a new vertical progression era.

## Participation

Meaningful participation is required for normal party rewards. AFK presence alone should not qualify.

However, participation checks are **not** the primary anti-boosting mechanism. A carried character could otherwise perform one trivial action and receive an endgame reward.

Therefore boosting prevention uses several layers together:

1. personal Character Tier / unlock eligibility;
2. personal reward-tier clamp;
3. personal first-clear state;
4. participation requirement;
5. explicit Required-Tier gates for content that must not be sequence-broken.

## Class Mastery pacing

The earlier Class Mastery direction remains:

- early Mastery ranks are fast;
- the class's core combat loop becomes available quickly;
- later Mastery increasingly unlocks build breadth rather than raw stat necessity;
- important milestones may use Class Advancement content;
- Max Mastery is not a prerequisite for the class to have level-appropriate base combat power;
- mastering unrelated classes must not become a mandatory source of universal combat stats.

## Explicitly rejected

- higher-level enemy = automatic bonus XP;
- endgame carry kills granting unrestricted endgame XP to new characters;
- host progression substituting for every party member's progression;
- hidden Tier restrictions that cause players to defeat difficult content for rewards they could never receive;
- universal veteran down-scaling in ordinary world/content;
- role-performance XP competition between tank/healer/DPS;
- repetitive skill-use grinding as the main Class Mastery engine;
- hard Character-Level walls around every open-world zone;
- manual stat allocation as a required baseline progression layer;
- permanent stat damage from leveling under the `wrong` class;
- universal hidden level-difference damage/hit penalties;
- mandatory fully normalized progression trials that ignore normal character growth;
- launch design built around infinite direct Character Power levels.

## Open numbers and implementation questions

- final player-facing names/themes for Tier I-VIII;
- exact immediate power granted by Tier promotion;
- exact Character XP curve;
- exact Class Mastery rank count and XP curve;
- exact reward budgets by activity;
- whether one adjacent locked Tier receives partial grace rewards;
- exact participation threshold;
- equipment and trading interaction with Character Tier eligibility;
- eventual conditions under which a future expansion should raise Lv.80 / Tier VIII.
