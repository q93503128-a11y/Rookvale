# Weapon & Resource Structure Research 01

**Status:** Design discussion / not all rules locked

## Resource design correction

Rookvale is a turn-based game that may often feature one boss, one elite, or only a few enemies. Therefore a class resource must not depend primarily on enemy kills unless that class is specifically designed around short-lived adds/minions.

### Rule

A core class resource should have at least one **reliable baseline source** that remains usable in boss fights and low-enemy-count encounters.

Conditional events such as kills, crits, cleanses, intercepts, status detonations, or enemy phase changes may grant **bonus acceleration**, but should not normally be the sole source of the class's main resource.

Example for a fire specialist:

- applying Burn: small Ash/Heat generation;
- consuming or detonating Burn: meaningful generation;
- maintaining Burn across turns: possible generation with safeguards;
- killing a burning enemy: larger bonus generation, not the primary loop;
- certain class skills/passives: alternative generation routes.

This keeps the resource functional against a single boss while making multi-target encounters feel different rather than mandatory.

## Weapon ancestry: do not bind one lineage to exactly one weapon

The earlier idea of weapon-oriented root classes is useful for organizing equipment, but a strict `one root class = one exact weapon forever` rule would be too restrictive.

External references show multiple viable models:

- The Elder Scrolls Online separates class skill lines from weapon skill lines, allowing one class to use several weapon families.
- Guild Wars 2 professions can use several weapons, while elite specializations can add a new weapon proficiency and new mechanics/skills.

Rookvale should use a middle model.

## Proposed Rookvale weapon-proficiency model

### 1. Root class = combat discipline + starting weapon family set

A root class may begin with **more than one compatible weapon type**.

Example only:

```text
Martial root
- one-handed blade
- spear / polearm
- shield compatibility where applicable
```

A descendant class inherits the weapon proficiencies that still fit its identity rather than being forced to one exact weapon.

### 2. Descendants may add a weapon proficiency

A specialization can unlock an additional weapon when that weapon materially changes the class fantasy or combat pattern.

Example:

```text
Martial root
├─ Knight
│  ├─ Guardian Knight: sword + shield emphasis
│  └─ Lancer Knight: gains stronger spear/polearm identity
└─ Duelist
   └─ favors one-handed blades
```

The point is not to lock these exact classes, but to allow the lineage to share an equipment ecosystem while later classes specialize.

### 3. Weapon categories should be broad enough to control item bloat

Do not create a separate loot ecosystem for every visual weapon noun if the mechanical distinction is small.

Possible broad families can later be split by tags/subtypes, for example:

- one-handed blades;
- heavy weapons;
- polearms;
- bows / ranged physical;
- daggers / agile weapons;
- arcane focuses (staff, wand, tome, orb, etc. if appropriate);
- shields / defensive off-hands;
- fist / martial weapons;
- firearms / mechanical weapons;
- special weapons only when the design justifies a new family.

Exact families are not locked.

### 4. Class skills remain class-bound

Weapon flexibility must not undo the class-bound skill rule.

A weapon primarily provides:

- equipment stats and affixes;
- attack profile / baseline attack behavior;
- compatibility with certain class skills;
- possible weapon traits or passive modifiers;
- visual identity.

Rookvale should avoid turning weapon choice into a completely independent second class system unless later testing proves that desirable.

### 5. Weapon-specific differences may matter inside the same class

Example possibilities:

- sword: balanced speed / counter-oriented bonuses;
- spear: better back-row access, armor penetration, or anti-frontline reach;
- mace: stronger stagger / break / heavy-hit utility;
- shield: threat, guard, interception, or defense interactions.

These differences can make two characters of the same class play differently without giving them unrelated class skills.

### 6. Special / signature weapons may exist later

A later advancement may unlock a signature weapon or unusual proficiency if it reinforces identity.

This should be an exception with design purpose, not a reason to create excessive weapon categories.

## Current recommendation

Use **weapon-oriented ancestry without single-weapon imprisonment**:

- root classes define a small compatible weapon pool;
- descendants inherit a sensible subset;
- some descendants may gain or emphasize an additional weapon;
- class skills stay class-bound;
- special/signature weapons are allowed where they meaningfully change the fantasy;
- item families stay broad enough to avoid loot-table fragmentation.

This preserves recognizable class lineages while allowing cases such as a knight descendant that legitimately uses a spear.
