# First Vertical Slice

**Status:** Core slice scope mostly defined; exact content count remains iterative

The first slice should prove Rookvale's identity, not merely prove that individual technical features work.

## Slice ingredients

- one small but polished starting settlement;
- one connected outdoor exploration area;
- one smaller special/dungeon area;
- controllable player movement and interaction;
- several visually and mechanically distinct enemies;
- full transition from overworld to turn-based battle and back;
- equipment and rewards sufficient to show progression;
- minimal NPC/quest content;
- one stronger encounter or boss;
- UI representative of intended final quality rather than temporary browser forms;
- architecture prepared for multiplayer, with actual networking introduced early enough to validate assumptions.

## First class implementation — intentionally small

Rookvale's long-term class design is broad, but the first slice implements only a representative sample.

### Initial origin disciplines

1. **Armsman**
   - Knight
   - Duelist
2. **Ranger**
   - Hunter
   - Marksman
3. **Arcanist**
   - Pyromancer
   - Cryomancer
4. **Acolyte**
   - Priest
   - Oracle

This is not the final roster and does not imply that every future origin has exactly two branches.

The subset exists to test:

- front-row tanking, threat, interception, and guarding;
- precision/counter melee;
- ranged target marking and a limited companion/pet pattern;
- elemental damage-over-time and control;
- healing, prevention, cleansing, buffs, and debuffs;
- turn-intent / timeline support;
- distinct class resources/passives;
- skill-loadout variation between two players of the same lineage;
- solo viability versus 2-4 player role synergy;
- ancestral weapon pools and descendant specialization.

Do not expand into the full class bank until these systems prove fun and readable.

## First combat implementation milestone

Before the full overworld slice depends on combat balance, build one deterministic combat harness from the current canonical combat documents:

- `../01-gameplay/COMBAT.md`;
- `../01-gameplay/COMBAT_VOCABULARY.md`;
- `../01-gameplay/PROTOTYPE_NUMBERS.md`;
- `../01-gameplay/PROTOTYPE_ENEMIES.md`;
- the eight class documents under `../01-gameplay/classes/`.

### Minimal class content

Do **not** implement every planned learned skill immediately.

Start with roughly 4-6 representative normal actives per class, one innate mechanic, one Reaction candidate, one Signature candidate, and a small passive/Technique sample. The exact representative set is recorded in the first-eight class cross-check.

### Enemy test ladder

The first combat harness should progress through:

1. **Front and Back** — baseline melee + Back-row attacker;
2. **Protection and Sustain** — Guard/Barrier defender + healer/support;
3. **Speed and Status** — fast movement enemy + status user;
4. **Elite** — mixed pressure, Back-row targeting, Reaction and Breakable windup;
5. **Boss** — multi-phase test of Threat, formation, Break, status conversion, support adds, prediction, protection and burst windows.

Enemy/faction names are placeholders until world production gives them a proper regional identity.

### Required combat telemetry

Record at minimum:
- elapsed Timeline Units;
- Natural Turns per combatant;
- actions used and cooldown availability;
- damage dealt/taken;
- healing and effective overheal;
- Barrier created/absorbed/wasted;
- Threat per enemy and final target selections;
- Guard/Intercept triggers;
- Break damage, Break Events, repeat-Break escalation;
- hard-control conversions and repeat resistance;
- status uptime/ticks/cleanses;
- class-resource gain/spend/overcap;
- companion assists/commands;
- Reaction triggers;
- Signature uses;
- TTK and boss Natural Turns by party size.

This telemetry is part of the prototype requirement. Without it, balance changes would be guesswork.

### Combat milestone exit criteria

The deterministic combat milestone is ready to feed the polished web slice when:
- all eight class core loops function without a required second player;
- no class core resource requires kills or adds;
- Bonus/Reaction actions cannot recurse or accelerate ordinary temporal systems incorrectly;
- a fast unit, slow unit, DoT/HoT, and cooldown can coexist without duration contradictions;
- Knight meaningfully changes target pressure but cannot monopolize every boss action;
- Back row is safer but demonstrably targetable;
- Break is achievable solo but cannot chain-lock Elite/Boss actions;
- Cryomancer control retains boss value without raw Freeze-lock;
- Pyromancer resource flow works against one boss;
- Priest has meaningful prevention/utility turns rather than mandatory heal spam;
- Oracle information is valuable without making baseline telegraphs useless;
- Hunter companion does not behave like a second full player;
- 2-4 players add tactical flexibility without reducing the boss to a simple HP multiplier exercise.

Numerical tuning can remain rough when these structural conditions pass.

## Slice success criteria

The slice is successful only if it demonstrates:

1. Exploring the world feels worth doing.
2. Entering combat is not disruptive or tedious.
3. Turn-based combat has a recognizable tactical identity.
4. Different roles matter.
5. Two builds of the same ancestry can feel meaningfully different.
6. Solo progression remains credible while parties gain tactical flexibility rather than overwhelming efficiency.
7. The game looks intentionally designed.
8. The structure can plausibly support online parties and future platform ports.

## Not a content-volume milestone

The slice does not need a huge map, the planned long-term class roster, many hours of quests, or an endgame. Depth and production quality in a small area are more valuable at this stage.
