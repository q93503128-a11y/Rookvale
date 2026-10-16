# Character Progression Research 01

**Status:** Research synthesis for the locked first character-growth model

## Scope

This pass focuses only on the structure of long-term character growth: persistent character level, class/job-specific mastery, class switching, advancement requirements, and the risk of forcing players to grind unrelated classes.

Rookvale's constraints are unusual:

- one persistent player character rather than a collectible party;
- potentially very large long-term class roster;
- class-bound skills and passives;
- asymmetric class trees;
- solo and multiplayer must both remain viable;
- switching to a newly unlocked class must not make a high-level character temporarily unusable;
- unrelated classes should not become mandatory chores merely because they grant permanent combat bonuses.

## Broad comparison pool

The survey considered the following progression families and related systems:

- Final Fantasy XIV — one character can access multiple combat jobs, but job levels are separate;
- Ragnarok Online — Base Level plus Job Level;
- Xenoblade Chronicles 3 — character level plus per-class Class Rank;
- Guild Wars 2 — persistent character level with specialization unlock tracks and out-of-combat specialization swapping;
- Bravely Default — independent job levels and cross-job support abilities;
- Dragon Quest IX — vocation-specific levels and rewards for raising multiple vocations;
- Final Fantasy V — ABP-based job mastery and cross-job ability inheritance;
- Final Fantasy Tactics — job points, job levels, and cross-job ability building;
- Octopath Traveler / Octopath Traveler II — job-specific JP spending and support-skill unlocks;
- Tactics Ogre: Reborn — persistent unit level retained through class changes, with class identity determining available abilities;
- Fell Seal: Arbiter's Mark — class AP mastery plus active/passive/counter inheritance through class and subclass systems;
- Orna / Hero of Aethric — persistent single-character class changing and long-tail class progression;
- Guild Wars 2 elite specializations — specialization unlocks can reshape profession mechanics and weapons without restarting character level.

The purpose is not to reproduce any one of these systems. The relevant question is how they solve the tension between persistent character growth and class-specific mastery.

## Core lessons

### 1. Full per-class re-leveling creates friction as roster size grows

FFXIV demonstrates that separate job levels make each job feel independently developed, but that same structure creates repeated leveling work whenever a player adopts a new job. That cost can be acceptable with a limited roster and mature catch-up systems, but Rookvale's intended long-term class count makes full re-leveling increasingly hostile to experimentation.

Ragnarok's Base Level + Job Level separates character strength from profession advancement more cleanly, but traditional Job Levels still substantially gate the character's immediate class power.

**Rookvale lesson:** do not reset the player's fundamental combat level when changing class.

### 2. Character level and class mastery solve different problems

Xenoblade Chronicles 3 is a strong structural reference: the character keeps their overall level while Class Rank unlocks and improves class-specific Arts/Skills. This proves that class familiarity can progress independently from raw character level.

Tactics Ogre: Reborn is another useful contrast. A unit retains its character level when changing classes, so trying a new class does not require rebuilding basic numerical power from level 1.

**Rookvale lesson:** persistent numerical progression and class-depth progression should be separate layers.

### 3. Class mastery should unlock depth more than baseline viability

A new class should expose its defining mechanic and enough representative actions immediately. Mastery can then unlock more active choices, passives, Reactions, Signatures, Techniques, and weapon interactions.

This produces a useful progression curve:

`usable immediately -> increasingly expressive -> fully buildable`

rather than:

`numerically crippled -> grind trivial enemies -> finally usable`.

### 4. Cross-class permanent power easily becomes mandatory homework

Final Fantasy V, Bravely Default, Final Fantasy Tactics, Xenoblade Chronicles 3, Octopath and Fell Seal all show variants of carrying abilities, passives, or mastered benefits across jobs/classes. These systems can create excellent buildcraft in games designed around cross-job mixing.

They also create a predictable optimization pressure: players are incentivized to level jobs they may not enjoy because those jobs contain universally valuable passives or abilities.

That directly conflicts with Rookvale's already-locked rule that unrelated class branches do not contribute to one universal best-of-every-class combat build.

**Rookvale lesson:** unrelated class mastery must not grant direct permanent combat power to every other class.

Cosmetics, titles, achievements, codex progress, collection completion, or noncombat prestige rewards are safe alternatives.

### 5. Specialization unlocks can be meaningful without resetting level

Guild Wars 2 elite specializations are useful because specialization investment unlocks a new mechanic, skills, traits, and sometimes weapons while the character remains at the same underlying level. Specializations can also be changed outside combat once unlocked.

Rookvale differs because its class tree is much broader and class-bound, but the lesson is useful: a new combat identity does not require numerical de-leveling.

### 6. Advancement requirements do not need one universal template

Several class systems gate progression through level, job mastery, quests, story milestones, items, exploration, or specialization currency. Rookvale's asymmetric tree benefits from combining these selectively.

A simple early branch can use Character Level + predecessor Mastery + a short class trial. A hidden or prestigious branch may use discoveries, bosses, questlines, rare conditions, or unusual lineage prerequisites.

**Rookvale lesson:** advancement conditions follow class fantasy and progression role rather than a universal `Lv.20 -> Lv.40 -> Lv.60` ladder.

## Locked Rookvale synthesis

### Persistent Character Level

Rookvale uses one persistent **Character Level**.

- changing class never resets Character Level;
- Character Level represents the overall growth of the persistent avatar;
- it provides the baseline scale for combat stats, equipment/content access, and general progression;
- class choice modifies that baseline through class stat profiles rather than historical level-up stat gains;
- leveling as one class must not permanently damage or optimize the stat growth of another class.

Conceptually:

`final baseline stats = Character Level baseline x current Class Profile + equipment/other modifiers`

Exact formulas remain future balance work.

### Per-class Class Mastery

Every unlocked class stores its own **Class Mastery** progression.

Class Mastery primarily unlocks class depth:

- normal Active choices;
- selectable Passives;
- Reaction candidates;
- Signature candidates;
- Techniques;
- advanced class-mechanic interactions;
- selected weapon/class interactions.

A newly unlocked class receives its defining innate mechanic and enough basic actions to function immediately at the character's current progression tier.

Class Mastery does not exist primarily to rebuild lost HP/Attack/Defense after switching.

### No unrelated-class power tax

Mastering an unrelated class does not grant universal combat-stat bonuses, transferable unrelated skills, or mandatory passives to other classes.

Do not create a long-term optimization rule such as:

- master every tank for permanent HP;
- master every caster for permanent Power;
- collect one best passive from twenty unrelated classes.

Class mastery rewards may include class-local power/depth and noncombat prestige, cosmetics, titles, collections, or achievements.

Ancestral inheritance inside the same explicitly connected lineage remains allowed under the existing class-lineage rules.

### Class switching

Once a class or sibling branch has been legitimately unlocked, the character may return to it later without losing progress.

Switching restores that class's saved Mastery and class-bound build state.

Persistent systems remain unchanged:

- Character Level;
- world/story progression;
- inventory and permanent ownership;
- unlocked classes;
- account/character collections.

Current class-specific systems change to the equipped class:

- innate mechanic;
- eligible skills;
- selectable class passives;
- Reaction;
- Signature;
- Techniques;
- compatible class-specific loadout rules.

The exact location/UX restriction for switching is still to be designed, but it occurs outside active combat and is not intended to require re-unlocking or destructive respec costs.

### Asymmetric advancement conditions

Typical advancement may combine:

- minimum Character Level;
- predecessor Class Mastery;
- class quest/trial;
- story or region access;
- boss/encounter completion;
- discovery;
- special item or NPC relationship;
- unusual lineage conditions for hidden/prestige branches.

Not every class needs every condition, and every lineage does not advance at the same levels or depth.

## Rejected directions

### Full independent level per class

Rejected as the main structure because Rookvale's long-term class count would make experimentation require excessive re-leveling.

### Historical class-based stat growth

Rejected. The class equipped during a Character Level-up should not permanently bias the avatar's future stat potential and create hidden 'wrong leveling' traps.

### Universal permanent bonuses for mastering unrelated classes

Rejected because it converts optional class variety into mandatory completion work.

### Broad cross-class skill inheritance

Rejected by the existing class-bound ability policy. Rookvale is not FFV/Bravely/FFT-style unrestricted job-mixing.

### Completely mastery-free class swapping

Also rejected. Classes need their own progression layer so developing a favorite class still has meaning. The mastery layer unlocks breadth and sophistication without forcing basic numerical re-leveling.

## References retained as most useful

- Final Fantasy XIV — separate job leveling: useful warning about repeated re-leveling friction for a very broad roster.
- Ragnarok Online — Base Level + Job Level separation.
- Xenoblade Chronicles 3 — Character Level + Class Rank, with class-specific Arts/Skills unlocking through rank.
- Guild Wars 2 — specialization training and free out-of-combat specialization/trait swapping once learned.
- Tactics Ogre: Reborn — persistent unit level across class changes; useful reference for immediate viability after switching.
- Bravely Default / Final Fantasy V / Final Fantasy Tactics — powerful cross-job mastery systems, used primarily as a warning for Rookvale's unrelated-class power-tax problem.
- Octopath Traveler — job-specific JP progression and support-skill unlocking.
- Fell Seal: Arbiter's Mark — class mastery and separated Active/Passive/Counter layers; useful but intentionally more cross-class than Rookvale.
- Orna / Hero of Aethric — single persistent avatar with long-tail class progression and class switching.

## Still open after this pass

- Character Level cap and long-term cap policy;
- Character XP curve and catch-up rules;
- exact Class Mastery scale, cap, and rate;
- whether mastery comes only from combat or also quests/exploration/class-specific feats;
- exact minimum kit granted immediately on unlocking a class;
- where class switching is legal and whether presets can include class switches;
- exact advancement conditions for each lineage;
- exact stat profiles and later equipment/stat formulas.
