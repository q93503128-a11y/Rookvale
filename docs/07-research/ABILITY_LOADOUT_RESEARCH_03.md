# Ability Loadout Research 03 — Slot Counts, Passives, Reactions, Signatures, Techniques

**Status:** Research note supporting `docs/01-gameplay/ABILITY_LOADOUT_SYSTEM.md`.

This pass intentionally includes both famous and lesser-known / niche RPGs. The goal is not to copy a single game's loadout, but to compare how different games create build identity with limited action slots, passive choices, reactions, class mechanics, and skill transformations.

## Research questions

1. How many active choices can one persistent character reasonably carry without creating a giant hotbar?
2. How many passive choices remain understandable while still creating build diversity?
3. Should innate class identity consume a passive slot?
4. Should reactive/counter abilities occupy their own slot?
5. Should every class have an ultimate?
6. How much per-skill transformation is useful before content production becomes unsustainable?
7. How should these answers change because Rookvale is a single-avatar, sequential-turn, multiplayer-capable RPG rather than a collectible-party game?

## Reference findings

### WAKFU

- A character can equip up to 12 active spells and 6 passive spells.
- This proves a class-heavy tactical MMO can support a large prepared loadout.
- For Rookvale, 12 ordinary active buttons is considered too dense as a default because Rookvale also needs mobile / Roblox readability, universal commands, Reaction, Signature, and a 20-second multiplayer turn safeguard.

Source:
- https://wakfu.wiki.gg/wiki/Spell

### Last Epoch

- The action bar and specialization system center on five equipped skills.
- Each specialized skill has its own skill tree, allowing a small action bar to hide substantial build depth.
- This is a strong reference for meaningful skill transformation, but attaching a large tree to every Rookvale skill would be too expensive across a planned 80-100+ class concept bank.

Source:
- https://support.lastepoch.com/hc/en-us/articles/46363203944859-Skill-Specialization

### Fell Seal: Arbiter's Mark

- Characters have four passive effects total: two from the current class and two selectable learned passives.
- Counter abilities are a separate system, and only one counter is equipped.
- This strongly supports separating always-on class identity, selectable passives, and a dedicated reactive layer.
- Rookvale does not copy Fell Seal's cross-class passive inheritance because Rookvale keeps class/lineage identity much stricter.

Sources:
- https://fellseal.fandom.com/wiki/Abilities
- https://fellseal.fandom.com/wiki/Passives

### Octopath Traveler

- Characters equip up to four support skills.
- Four passive choices are enough to produce meaningful interactions without becoming a giant passive board.
- Rookvale borrows the scale reference, not Octopath's cross-job mixing rule.

Source:
- https://octopathtraveler.fandom.com/wiki/Support_Skills

### Bravely Default

- Support abilities consume a limited slot budget, with stronger abilities sometimes costing multiple slots.
- This creates an interesting build-budget system but adds a second optimization currency to passive selection.
- Rookvale's first implementation keeps four equal passive slots. Weighted passive costs remain a rejected-for-now alternative unless equal-slot balance proves inadequate.

Sources:
- https://bravelydefault.fandom.com/wiki/Bravely_Default_support_abilities
- https://bravelydefault.fandom.com/wiki/Bravely_Default_abilities

### TROUBLESHOOTER: Abandoned Children

- Characters have fixed masteries plus a deep mastery board.
- Certain mastery combinations automatically unlock mastery sets with extra effects.
- The game is valuable evidence that passive combinations themselves can become a major build game.
- It also demonstrates the readability and balance cost of very dense passive composition.
- Rookvale should borrow interaction depth selectively while keeping the visible passive-slot layer much simpler.

Sources:
- https://troubleshooter.fandom.com/wiki/Masteries
- https://troubleshooter.fandom.com/wiki/Mastery_Sets

### Siralim Ultimate

- The game uses many specializations whose perk sets radically alter battle rules.
- Examples include health becoming an offensive stat, benefiting from dead allies, manipulating failed random effects, or provoking and counter-striking.
- It is especially useful as a long-tail mechanic vocabulary source: class identity can be a rule rewrite rather than a list of conventional attacks.
- Rookvale should study these unusual rule changes while adapting them to a single-avatar party RPG.

Sources:
- https://siralimultimate.wiki.gg/wiki/Siralim_Ultimate
- https://siralimultimate.wiki.gg/wiki/Specializations

### Crystal Project

- Classes have innate passives that can strongly alter fundamental rules: threat generation, Cover behavior, cooldown ceilings, AP generation, weapon use, etc.
- This is a useful smaller turn-based reference for keeping class identity in an automatic innate rule rather than spending a selectable passive slot on the class's basic fantasy.
- Its threat, stance, cooldown, and weapon interactions are particularly relevant to Rookvale's own combat vocabulary.

Sources:
- https://crystal-project.fandom.com/wiki/Classes
- https://crystal-project.fandom.com/wiki/Classes/summary

### Battle Chasers: Nightwar

- Basic Actions are weaker but generate temporary Overcharge, while stronger Abilities consume resource.
- Perks modify resource generation and ability behavior.
- High-impact Burst abilities sit outside the normal action set and are not all simple damage nukes.
- The shared party Burst Meter is specifically *not* adopted by Rookvale because separate human players should not fight over one party resource.
- The useful lesson is instead that a high-impact ability category can be separate from normal skills and can contain healing, time manipulation, damage, or utility.

Sources:
- https://battlechasersnightwar.fandom.com/wiki/Actions
- https://battlechasersnightwar.fandom.com/wiki/Overcharge
- https://battlechasersnightwar.fandom.com/wiki/Battle_Bursts

## Rookvale synthesis

### 1. Normal active slots: 8 mature, progressively unlocked

Rookvale uses eight normal active slots at mature buildcraft.

Why not 5?
- Rookvale is a single-avatar RPG: one player character must carry enough offense, survival, class resource management, utility, and solo tools.
- Five works well in games where each skill has a giant transformation tree or where multiple controllable characters distribute responsibilities, but risks making Rookvale's one avatar feel artificially narrow.

Why not 12?
- Rookvale also has universal commands, Reaction, Signature, status information, and cross-platform UI requirements.
- Multiplayer turns need fast decisions.

Onboarding target: roughly 4 -> 6 -> 8 normal slots.

### 2. Selectable passives: 4

Four is the prototype target.

- Large enough for combinations.
- Small enough that each slot can remain meaningful.
- Equal-cost slots are simpler than a second weighted-point economy.
- Passive content should be mechanically strong enough that four choices matter.

### 3. Innate class mechanic: always active

The core class fantasy does not consume one of the four selectable passive slots.

An innate mechanic may be a compact package rather than literally one effect: resource rules, threat behavior, summon logic, stance rules, or another linked mechanic.

Advanced classes evolve or redirect the ancestral mechanic rather than stacking dozens of permanent inherited passives.

### 4. Reaction: one dedicated slot

A dedicated Reaction slot preserves out-of-turn identity without mixing reactions into passive clutter.

- One equipped at once.
- Does not count as a natural turn.
- Does not normally tick natural-turn cooldowns/durations.
- No recursive reaction chains by default.
- Classes that do not need reaction gameplay are not forced to invent filler options.

### 5. Signature: one dedicated slot, not a universal ultimate meter

Every mature class should have at least one class-defining Signature candidate, but a Signature can be:

- attack;
- transformation;
- defensive oath;
- rescue;
- summon;
- curse;
- major status manipulation;
- timeline intervention;
- another class-specific high-impact action.

It normally consumes the normal action for the turn. Limitation can be cooldown, resource, condition, charges, or once-per-battle rules.

There is no shared party ultimate meter.

### 6. Techniques: selective per-skill transformations

Rookvale does not use a giant Last-Epoch-style tree on every skill.

Instead:
- important skills may have 2-3 mutually exclusive Techniques;
- Technique does not consume another active slot;
- it changes function, targeting, timing, resource behavior, status interaction, row access, weapon interaction, or risk/reward;
- purely numerical `+10% damage` variants are not sufficient;
- not every skill needs a Technique.

A mature class may target roughly 3-5 important Technique-enabled skills, but this is not a quota.

### 7. Mature content targets

Across ancestry + current specialization, a mature class lineage should roughly aim for:

- 12-16 normal active choices, 8 equipped;
- 7-10 serious selectable passives, 4 equipped;
- 2-4 Reaction candidates if reaction play fits the class;
- 2-3 Signature candidates when mature enough;
- Techniques on around 3-5 important actives.

These are production targets, not symmetry rules. Do not create filler to hit a number.

## Research policy for actual class kits

For every production class kit:

1. Discovery survey: normally inspect roughly 10-20 possible games/classes/mechanics.
2. Synthesis set: retain roughly 6-10 genuinely useful references.
3. Include multiple lesser-known / indie / older / non-obvious sources when useful.
4. Research active, passive, Reaction, Signature-like, class-resource, CC/status, and transformation mechanics separately.
5. Record failure modes as well as good ideas.
6. Build the Rookvale kit around Rookvale's own turn timeline, cooldown rules, front/back formation, threat, multiplayer pacing, and single-avatar constraints.

These numbers are quality targets, not citation quotas. The purpose is to maximize mechanic diversity and avoid repeatedly rediscovering only the most famous RPG conventions.
