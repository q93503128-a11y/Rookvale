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
