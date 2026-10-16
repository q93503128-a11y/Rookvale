# Death, Revival, and Dungeon Failure Research 01

**Date:** 2026-10-16

## Research question

How should Rookvale handle 0 HP, resurrection, wipes, dungeon failure, retry limits, and retreat without erasing long-term progression or making every party carry one mandatory class?

## External references reviewed

### Final Fantasy XIV

Official White Mage and Scholar job guides show resurrection as a class/job capability rather than a universal player action. This supports Rookvale's choice to make in-combat death response part of party preparation and class identity.

- https://na.finalfantasyxiv.com/jobguide/whitemage/
- https://na.finalfantasyxiv.com/jobguide/scholar/

Criterion/variant-style content demonstrates that resurrection rules can change by content: some duties apply resurrection restrictions while supplying limited duty-specific raise actions. This supports content-specific failure contracts rather than one universal resurrection rule.

- https://na.finalfantasyxiv.com/lodestone/topics/detail/46ff678d764ec5b14996fcd2fae85a7170f385f0/

Deep Dungeon content demonstrates a stronger separation between ordinary progression and optional high-stakes challenge runs. In Palace of the Dead / Heaven-on-High / Eureka Orthos, full-party KO can end the run or invalidate challenge progression on deeper challenge floors.

- https://na.finalfantasyxiv.com/lodestone/playguide/contentsguide/deepdungeon/
- https://na.finalfantasyxiv.com/lodestone/playguide/contentsguide/deepdungeon2/
- https://na.finalfantasyxiv.com/lodestone/playguide/contentsguide/deepdungeon3/

Lesson retained:

> Required/ordinary content and optional prestige-run content do not need identical failure severity.

### Monster Hunter

Official Monster Hunter manuals define quest-specific failure conditions, including faint/reward conditions and time limits, rather than treating every mission as an unlimited checkpoint crawl.

- https://game.capcom.com/manual/MH_Gen/en-UK/page-42.html
- https://game.capcom.com/manual/MH_Gen/en-UK/page-41.html

Lesson retained:

> A mission may advertise a finite failure budget or special failure conditions before entry, and reaching the condition can legitimately fail the whole run.

Rookvale does not copy Monster Hunter's exact faint-count/reward-money implementation. It uses the structural lesson to justify shared Retry Stock and other visible content-specific failure contracts.

### World of Warcraft Mythic+

Blizzard has used explicit death/time penalties in high-end repeatable dungeon modes, demonstrating that death cost can be concentrated inside a run rather than deleting persistent progression.

- https://worldofwarcraft.blizzard.com/en-us/news/24148555/hotfixes-december-9-2024

Lesson retained:

> Endgame challenge modes may make mistakes matter strongly within the attempt while leaving permanent character ownership intact.

## Rookvale synthesis

### Rejected

- universal generic `Revive Ally` action for every class;
- permanent XP/level loss on death;
- dropped equipped items;
- routine Gold confiscation;
- equipment durability damage as death tax;
- random percentage-based flee chance;
- forcing every standard story dungeon to restart from the beginning after one wipe;
- forcing complex raid-learning encounters to consume rare entry keys on every failed attempt.

### Retained

- `Fallen` as a combat-state abstraction at 0 HP;
- in-combat resurrection/death response as class/build identity;
- multiple future death-response archetypes so one exact class does not monopolize the role;
- encounter-only anti-infinite-revival limitation;
- automatic post-combat recovery for Fallen allies after victory;
- no loss of secured persistent progression on ordinary death;
- standard dungeons using checkpoints and encounter reset;
- selected expedition/challenge content using finite shared Retry Stock;
- rare no-retry/deep-run challenge formats that fail/reset the run on wipe;
- ordinary raids/pinnacle bosses remaining retryable for learning;
- deterministic, easy Retreat in ordinary eligible encounters;
- content-specific failure conditions disclosed before commitment.

## Necromancer/corpse manipulation note

A future Necromancer-like design may use a Fallen ally as the basis for an undead proxy, corpse-puppet, revenant, or similar temporary substitute. This is deliberately not locked yet. It is retained as an example of how death mechanics can create class identity beyond standard resurrection.

If explored later, preserving control for the Fallen player is preferred over turning the player into a passive spectator.

## Canonical destination

Gameplay rules are recorded in:

- `docs/01-gameplay/DEATH_FAILURE_RETREAT.md`
