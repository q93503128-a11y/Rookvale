# Class Tree Research 01

**Status:** Research note — recommendation, not final lock.

## Rookvale constraints

- One persistent player character per human player; not a collectible-party game.
- Broad class fantasy and play-style variety is desirable.
- Skills are class-bound rather than globally inherited across unrelated jobs.
- Same-class players should still diverge through skill loadouts, equipment, stats, resources, and specialization choices.
- The class system must remain maintainable across Web, mobile, and Roblox versions.

## External lessons

### Tree of Savior

Tree of Savior historically pushed multi-stage class advancement very far. The developers later documented problems with the old vertical-rank structure: lower-rank classes fell behind later classes, apparently broad choice narrowed into a much smaller set of valid builds, and the system became convoluted enough to justify a major Re:Build restructuring.

The post-Re:Build design reduced progression to one base class plus three chosen classes and emphasized clearer class identities, horizontal choice, class-change recovery, and party synergy.

Useful lesson for Rookvale: class breadth is valuable, but endlessly extending a vertical advancement ladder creates balance, regret, and maintenance problems. Future variety is safer when added horizontally as sibling options rather than by making every existing class advance another tier forever.

Official sources:
- https://treeofsavior.com/page/news/view.php?n=1530
- https://treeofsavior.com/page/news/view.php?n=1534
- https://treeofsavior.com/page/guide/view.php?n=11

### World of Warcraft

World of Warcraft separates broad class identity from specialization identity. Blizzard has repeatedly discussed preserving recognizable class-defining mechanics while allowing specializations and later Hero Talent trees to deepen the fantasy without replacing the core class.

Its Hero Talent approach also illustrates a useful finite-depth principle: a specialization gains a limited extra layer of identity rather than an endlessly recursive chain of new jobs.

Useful lesson for Rookvale: first establish what makes a base class recognizable, then use a small number of specialization layers to sharpen fantasy and gameplay. Avoid making each successive tier invalidate the identity and skills players already liked.

Official sources:
- https://worldofwarcraft.blizzard.com/en-us/news/23187293
- https://worldofwarcraft.blizzard.com/en-us/news/24025828
- https://worldofwarcraft.blizzard.com/en-us/news/23797209

## Recommended Rookvale topology

Use a **finite specialization tree with two meaningful branching moments after the base class** as the default.

```text
Base Class
  -> Specialization (major fantasy + core mechanic)
       -> Advanced Specialization (deeper play-style identity)
```

Example only:

```text
Mage
  -> Pyromancer
       -> Infernalist       (burst / self-risk / large Mana spending)
       -> Ashcaller         (burn / attrition / debuff spread)
  -> Cryomancer
       -> Frostwarden       (barriers / control / party defense)
       -> Glaciomancer      (freeze setup / burst shatter)
  -> Storm Mage
       -> Tempestcaller     (speed / chaining / repeated actions)
       -> Thunder Sage      (charged strikes / delayed burst / control)
```

Element alone is not sufficient identity. Each branch should change resource flow, target logic, cooldown use, formation interaction, timing, or party role.

## Why not only one branch?

A single branch is simple but leaves less long-term identity progression for a game where the player owns one persistent avatar. Rookvale benefits from a later specialization milestone that gives players another meaningful personal choice after they already understand their class.

## Why not endless branching?

Branch count grows geometrically.

If 8 base classes each have 3 first branches and every branch then has 2 advanced branches:

- 8 base classes
- 24 first specializations
- 48 advanced specializations

That is already **80 named class states** before future expansion.

Adding another 2-way mandatory branch would produce 96 additional end branches, while every branch needs skills, balance, VFX, UI, enemies/content compatibility, solo viability, party value, documentation, and cross-platform testing.

The maintenance cost grows much faster than the player-facing value.

## Expansion strategy

After the initial two branching stages, major updates should normally add one of:

1. a new sibling first specialization to a base class;
2. a new advanced specialization under an existing branch;
3. an entirely new base class family;
4. a horizontal mastery/talent system that changes builds without renaming the class;
5. rare hidden/quest classes, if later research supports them.

Do not automatically add a new vertical job tier to every class whenever level caps rise.

## Decision still needed

- Exact base-class count.
- Exact first-branch count per base class; symmetry is not mandatory.
- Whether advanced branches always split 2 ways or vary by class.
- Whether sibling specializations can be switched after unlocking, and under what restrictions.
- Whether the base-class skill pool remains available to descendants in the same lineage.
