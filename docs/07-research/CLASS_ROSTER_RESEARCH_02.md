# Class Roster Research 02 — Large-Roster Survey

**Status:** Research basis for `CLASS_ROSTER_MASTER_PLAN.md`

This pass studies games with broad class/job systems to extract reusable design principles for Rookvale. It does not copy their exact class trees.

## Surveyed references

### Tree of Savior

Official current class listing organizes a very large roster under five broad base trees: Swordsman, Wizard, Archer, Cleric, and Scout. The roster includes martial, tank, spear, duelist, elemental, time, summoning, necromancy, alchemy, pet, trap, firearm, priest, druid, oracle, plague, assassin, enchanter, support, and many other fantasies.

Important lessons:

- a small number of broad ancestry/equipment trees can support a very large fantasy roster;
- class identity can be much narrower than the base tree;
- horizontal class choice is healthier than endlessly making later classes strictly stronger;
- the developers have explicitly discussed the maintenance and balance burden of an 80+ class environment;
- class-tree placement should be based on gameplay synergy and build coherence, not only lore naming.

Sources:
- https://treeofsavior.com/page/class/
- https://treeofsavior.com/page/news/view.php?n=1530
- https://treeofsavior.com/page/news/view.php?n=1534
- https://treeofsavior.com/page/news/view.php?n=1970

### Guild Wars 2

Nine professions each have a profession-specific mechanic and broad weapon access. Elite specializations can substantially alter the profession mechanic, add skill types and historically often add weapon proficiency. The current specialization structure shows that a stable base profession can support multiple mechanically distinct later identities.

Important lessons:

- a class needs an intrinsic mechanic, not merely a skill list;
- a specialization can justify itself by changing the profession mechanic, weapon access, skills, and traits together;
- multiple weapons per ancestry are healthy when the class still has a clear identity;
- selectable traits create same-class build diversity without requiring unlimited cross-class skill inheritance.

Sources:
- https://wiki.guildwars2.com/wiki/Profession
- https://wiki.guildwars2.com/wiki/Specialization
- https://www.guildwars2.com/en/news/specializations-part-two-reward-tracks-and-elite-specializations/

### Final Fantasy XIV

Current battle jobs cover tanks, healers, melee DPS, ranged physical DPS, and magical DPS with highly distinct job gauges and weapon identities. One character can train many jobs, but a job itself has a focused action/trait kit.

Important lessons:

- recognizable job fantasy benefits from strong job-specific gauges, actions, traits, and weapons;
- role clarity helps party readability;
- a large roster does not require every job to share the same internal resource model;
- unique weapons are flavorful, but Rookvale should not copy FFXIV's one-job/one-weapon strictness because it would fragment Rookvale's loot economy too heavily.

Sources:
- https://na.finalfantasyxiv.com/jobguide/battle/
- https://guide.ff14.co.kr/Job

### World of Warcraft

Classes such as Warrior, Monk, Druid, Shaman, Rogue, and Paladin demonstrate broad weapon compatibility, distinct resources, and role-changing specializations. Warrior uses Rage with many weapon types; Monk spans tank/heal/damage; Druid uses radically different forms/resources; Shaman uses both weapons and elemental/totem magic.

Important lessons:

- one ancestry can support several roles without losing identity;
- weapon access can be broad while specializations express preferred weapons;
- class resources should match class behavior rather than use one universal MP system;
- hybrids are valuable when their mechanics—not just numbers—change with the role.

Sources:
- https://worldofwarcraft.blizzard.com/en-us/game/classes
- https://worldofwarcraft.blizzard.com/en-us/game/classes/warrior
- https://worldofwarcraft.blizzard.com/en-us/game/classes/monk
- https://worldofwarcraft.blizzard.com/en-us/game/classes/druid
- https://worldofwarcraft.blizzard.com/en-us/game/classes/shaman

### Orna / Hero of Aethric

The official codex currently lists 80+ classes across many tiers and variants. Individual classes combine skill lists, equipment families, passives, resource mechanics, status effects, followers/summons, and later celestial variants.

Important lessons:

- a long-lived single-character RPG benefits from a wide class fantasy bank;
- class passives can carry as much identity as active skills;
- later variants should change mechanics rather than only raise coefficients;
- Rookvale should keep its own class-bound skill rule rather than inheriting Orna's broader cross-class skill collection model.

Sources:
- https://playorna.com/codex/classes/
- https://playorna.com/codex/classes/55/
- https://playorna.com/codex/classes/10/

### MapleStory

Explorer characters choose an early base job such as Warrior, Bowman, Thief, Magician, or Pirate, then remain within class-specific advancement choices rather than freely crossing unrelated job families.

Important lesson:

- a broad first decision followed by lineage-bound advancement keeps identity readable and supports a large long-term roster.

Source:
- https://support-maplestory.nexon.com/hc/en-us/articles/204080379-Can-any-class-advance-to-any-job-in-MapleStory

### Diablo IV

Classes use distinct class mechanics; the Barbarian's Arsenal system is a strong example of one class intentionally using multiple weapons as part of its identity rather than being hard-locked to one item type.

Important lesson:

- weapon plurality can itself be a class mechanic; Rookvale's ancestry should therefore define a compatible weapon pool rather than a mandatory single weapon.

Source:
- https://news.blizzard.com/en-us/article/23189677/diablo-iv-feature-overview

## Rookvale synthesis

The selected direction combines the strongest parts without adopting any one game's full structure:

1. A relatively small set of broad **origin disciplines** anchors equipment ancestry.
2. Each origin supports several related weapon families rather than exactly one weapon.
3. Descendants keep ancestral compatibility but may specialize or unlock additional weapons.
4. Class skills remain lineage-bound; no unrestricted best-of-every-class skill bar.
5. Every mature class should have a recognizable passive/resource/rule-changing mechanic.
6. Trees are asymmetric. Some branch once, some several times, some remain largely linear.
7. Promotions add mechanics, not merely stronger copies of old attacks.
8. CC, buffs, debuffs, threat, formation, cooldown, speed, summons, marks, HP sacrifice, and resource rules are all valid ways to create class identity.
9. The design bank can be extremely large, but production remains staged.
10. First implementation is intentionally small and representative.

## Production warning

A huge roster is only valuable if classes remain mechanically distinct and maintainable. If two proposed classes answer the same combat problems in nearly the same way, one should become a build/passive/loadout path inside the other rather than another permanent class node.
