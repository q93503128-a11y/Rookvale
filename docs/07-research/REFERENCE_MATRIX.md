# Reference Matrix

**Status:** Active

This document tracks what Rookvale studies from external games and, equally importantly, what it does **not** copy from them.

| Design area | Reference candidates | What to study | Current Rookvale direction |
| --- | --- | --- | --- |
| Overworld -> turn-based encounter structure | Hero of Aethric, Broken Ranks | Exploration rhythm, encounter transition, world-content density, how multiplayer presence survives the transition into battle | Hero of Aethric is the primary structural reference; no GPS |
| Multiplayer exploration | Hero of Aethric, Broken Ranks, Loomian Legacy, WAKFU | Seeing other players, party formation, drop-in/out friction, social presence without overcrowding | Multiplayer is foundational, not a post-launch bolt-on |
| Party turn-based combat | WAKFU, DOFUS, Broken Ranks, For The King II | Sequential timing, waiting-time control, AFK/disconnect handling, role interaction | Sequential Speed-based timeline; normal player turn limit starts at 20 seconds; AFK/disconnect cannot stall combat |
| Combat timeline / turn-frequency | Honkai: Star Rail action-value model, Grandia, Child of Light, Epic Seven, SaGa Scarlet Grace | Reciprocal Speed-to-delay models, visible initiative, cast/preparation intervals, one-shot action-bar movement, readable turn manipulation | First prototype uses continuous Timeline Units with `10000 / Speed` standard delay; Haste/Slow change future scheduling while Delay/Advance move the already-scheduled action; no immediate full-turn grants |
| Status-duration clocks | Summoners War, Darkest Dungeon / Darkest Dungeon II, event/charge-based tactical effects | Target-turn ticking, skipped-turn handling, start/end timing, separating full turns from extra actions, charge-based protection | Four explicit clocks: Target Natural Turns; Until Source Next Natural Turn; Eligible Event Charges; Timeline Units; Bonus/Reactions do not advance Natural-Turn clocks by default |
| Combat activity / anti-passivity | Sea of Stars, Octopath Traveler Break, Final Fantasy XIII Stagger, Grandia/Child of Light interrupts | Interrupts, break/stagger, readable future-turn pressure, vulnerability windows, keeping decisions active without reflex spam | Visible Break Gauge creates bounded Delay + Exposed and can cancel only explicitly Breakable actions; no mandatory reflex minigame on every action |
| Tactical positioning | Etrian Odyssey, Darkest Dungeon, DOFUS/WAKFU | Front/back pressure, target rules, formation relevance, class interaction | Two-row front/back formation; front has higher default threat but back is not universally untargetable |
| Threat / target control | Crystal Project, MMO aggro systems, Darkest Dungeon Guard/Mark | Per-enemy aggro, decay, protection, target weighting, explicit exceptions | Threat is per enemy and decays; row/class/Taunt/AI preference modify target score; Guard is proactive redirection and Intercept is a Reaction; scripted/AoE target rules can ignore ordinary Threat |
| Class identity and party roles | Guild Wars 2, Final Fantasy XIV, World of Warcraft, Tree of Savior, DOFUS/WAKFU | Class mechanics, role clarity, hybrid roles, same-class build diversity | Broad roster; each mature class should have a passive/resource/rule-changing identity and remain solo-capable |
| Large class-roster structure | Tree of Savior, Orna / Hero of Aethric, MapleStory | Large fantasy coverage, lineage readability, horizontal expansion, maintenance cost | Maintain an 80-100+ concept design bank but implement gradually; no symmetry requirement across trees |
| Class advancement | Tree of Savior, Guild Wars 2 specializations, MapleStory, Orna | Branch clarity, specialization depth, hidden classes, horizontal vs vertical growth | Deliberately asymmetric trees; branch only when gameplay/fantasy genuinely diverges; linear promotions must still add mechanics |
| Weapon/class relationship | Guild Wars 2, World of Warcraft, Diablo IV, Final Fantasy XIV | Multiple weapons per class, specialization weapon unlocks, loot fragmentation | Origin disciplines use related weapon pools, not one exact weapon; descendants may specialize or unlock additional weapons |
| Skill loadouts | WAKFU, Guild Wars 2, Last Epoch, Darkest Dungeon II, Chained Echoes | Learned pool versus equipped subset, action-bar density, same-class build diversity | Mature target: 8 normal active slots; universal commands separate; learn more than can be equipped |
| Selectable passives | WAKFU, Guild Wars 2, Fell Seal, Horizon's Gate, TROUBLESHOOTER | Passive-slot counts, fixed vs selectable identity, rule-changing traits | 1 innate class mechanic plus 4 selectable class-bound passives; avoid stat-bump-dominated boards |
| Reactions / counters | Fell Seal, TROUBLESHOOTER, tactical RPG counter systems | Dedicated counter layer, trigger rules, anti-loop safeguards | Prototype 1 dedicated Reaction slot; reactions are not full turns and cannot recursively chain by default |
| Signature / ultimate layer | Guild Wars 2 elite skills, Battle Chasers Bursts, class-specific capstones from RPGs | Dedicated high-impact skill presentation, cooldown/resource gating, class fantasy | 1 Signature slot; no shared party ultimate gauge; Signature need not be a damage nuke and normally consumes the ordinary action |
| Skill transformation | Last Epoch, Grim Dawn skill modifiers, Darkest Dungeon II paths, Guild Wars 2 traits | Per-skill transformation, global modifiers, tradeoffs, production burden | Important skills may use 2-3 mutually exclusive Techniques; no giant tree required for every skill |
| Long-tail ability research | TROUBLESHOOTER, Siralim Ultimate, Stolen Realm, Fell Seal, Battle Chasers, Horizon's Gate and other niche/indie RPGs | Unusual passives, triggers, hybrid builds, restrictions, reactions, resource loops | Production research deliberately includes useful smaller/less-famous games instead of repeatedly mining only major franchises |
| Class resources / gauges | Final Fantasy XIV, World of Warcraft, Guild Wars 2, Battle Chasers, Orna | Job gauges, Rage/Mana/Chi-like resources, temporary combat resources, class-specific mechanics | Cooldowns plus optional class-specific resources/stacks/marks; not every class uses universal MP or even a visible bar |
| Passives / traits | Guild Wars 2, TROUBLESHOOTER, Siralim Ultimate, Fell Seal, Orna | Rule-changing traits, innate passives, build choices, mastery combinations | Major passives should change behavior more often than provide generic small stat bumps |
| Status-effect identity | Pokemon, Persona 5 Technicals, Monster Hunter ailments, Etrian Odyssey ailments/binds, Darkest Dungeon | Different tactical consequences for DoTs/control, setup/payoff interactions, category restrictions, status removal | Burn/Bleed/Poison differ in tick/setup behavior; Stun/Freeze/Sleep/Petrify are not synonyms; Silence/Disarm/Root restrict capabilities instead of necessarily deleting a turn |
| Repeated CC / boss resistance | Etrian Odyssey accumulative resistance, Darkest Dungeon post-Stun resistance, Monster Hunter rising ailment thresholds, Star Renegades stagger limits | Diminishing returns, repeat-resistance decay, stagger budgets, keeping control relevant without stun-lock | Hard-control families build temporary repeat resistance; bosses convert hard CC into bounded Break/Delay/setup rather than relying on blanket immunity; repeated boss Break also becomes harder within a phase |
| Break / vulnerability | Octopath Traveler Break, Final Fantasy XIII Stagger, Star Renegades stagger | Visible thresholds, planned vulnerability windows, interrupt versus damage-payoff distinction | Break is posture, not another hard CC: visible gauge -> cancel only Breakable preparation -> bounded Delay -> Exposed -> rebuilt/escalated gauge |
| Mark / designation states | Darkest Dungeon Mark, class-specific mark/prey systems | Tags that skills read/consume, target preference, avoiding universal mandatory vulnerability debuffs | Mark is source-owned and has no automatic global damage bonus; Hunter Prey is a separate class-owned coordination state; Exposed owns universal vulnerability |
| Boss encounters | DOFUS/WAKFU, Broken Ranks, For The King II, Octopath Traveler, FFXIII, Star Renegades, Etrian Odyssey | Telegraphing, phases, role value, coordination checks, Break/CC resistance, failure recovery, repeat-control safeguards | First prototype boss combines Threat-respecting and exception attacks, Breakable windups, support adds, row pressure, status/cleanse interactions and phase patterns; hard CC converts rather than becoming useless or chain-locking |
| Binary control-gate caution | Divinity: Original Sin 2 physical/magic armor | Strengths and failure cases of gating whole CC families behind a separate armor layer | Negative reference: do not make control-heavy classes wait behind one universal binary armor gate before their mechanics matter |
| Party finding | Broken Ranks and modern MMOs | Activity filters, role filtering, requirements, reducing party-formation friction | Treat party finder as core MMO UX, not late polish |
| World / content variety | Hero of Aethric, DOFUS Touch, WAKFU, selected open-world RPGs | Regional identity, density of enemies/NPCs/dungeons/events, reasons to revisit old areas | Large handcrafted world with distinct spaces and broad content variety |
| Cross-platform tactical UI | WAVEN, DOFUS Touch, Broken Ranks mobile | Touch targets, HUD density, action selection, readable status info on small screens | Web-first implementation must stay within a Roblox/mobile-portable UI vocabulary |
| Roblox battle / exploration UX | Loomian Legacy and other suitable current Roblox RPGs | Controller/touch/mouse parity, menu scale, battle readability, Roblox player expectations | Research current Roblox games before final UI implementation |
| Pixel world presentation | Hero of Aethric plus selected high-quality pixel RPGs | Sprite scale, silhouette readability, environment density, animation economy, visual cohesion | No fixed cute/dark style yet; quality and readability take priority |
| Inventory / equipment UX | Modern mobile/PC RPGs selected per task | Information hierarchy, comparison speed, tooltips, touch usability | Open |
| Social / party UX | Broken Ranks and modern MMOs | Invite flow, reconnect behavior, party leader authority, readiness, matchmaking | Open |
| Deep system interaction | Divinity: Original Sin 2 | Systemic party skill interactions and encounter consequences | Depth reference only; do not inherit its slower encounter pacing or binary armor/CC gate by default |

## Key combat-prototype findings

### Octopath Traveler / Final Fantasy XIII
- Both show the value of building toward a visible threshold that creates a strong vulnerability window.
- Rookvale uses that lesson for `Break -> bounded Delay + Exposed`, but does not copy either game's exact weakness/shield/chain system.

### Etrian Odyssey / Darkest Dungeon / Monster Hunter
- Repeated successful control becoming harder is preferable to a boss being either fully stunnable or globally immune.
- Rookvale therefore tracks temporary same-family hard-control resistance and separately escalates repeated boss Break requirements.

### Star Renegades
- A limited stagger budget and turn-order manipulation demonstrate how control can be strong without becoming unlimited.
- Rookvale takes the bounded-control principle and applies explicit per-target Delay caps rather than copying its exact stagger-count rules.

### Grandia / Child of Light
- Visible initiative plus interruptible preparation makes `interrupt` mechanically different from a stored stun debuff.
- Rookvale's Stun therefore cancels eligible preparation or becomes bounded Delay/Break instead of simply creating another generic one-turn skip.

### Honkai: Star Rail / Epic Seven
- Speed-driven action frequency and direct action-bar manipulation are distinct mechanics.
- Rookvale separates persistent Haste/Slow from one-shot Advance/Delay and uses a reciprocal Speed-to-Timeline-Unit prototype formula.

### Summoners War
- Target-turn start/end processing is useful for effects intended to affect a fixed number of a unit's own actions.
- Rookvale uses Target Natural Turns as one duration clock, not the only clock.

### Crystal Project
- Per-enemy Threat with decay provides a useful model for measurable target pressure.
- Rookvale layers row modifiers, Knight identity, temporary Taunt and enemy-specific preferences on top instead of turning Threat into an absolute lock.

### Darkest Dungeon Mark / Guard
- Mark demonstrates that a tag can have no universal effect until another skill reads it.
- Guard demonstrates explicit redirection rather than vague Defense inflation.
- Rookvale uses source-owned Marks and separates prepared Guard from Reaction-based Intercept.

### Pokemon / Persona 5 / Monster Hunter ailments
- Status names remain interesting when they change timing, action choice, combo payoff, persistence, or removal rules rather than merely changing damage color.
- Rookvale uses this as the standard for adding future statuses.

### Divinity: Original Sin 2
- Physical/magic armor is useful evidence for the clarity of explicit protection layers but also a warning: broad binary CC gating can make controllers ineffective until another resource is removed.
- Rookvale keeps Barrier and Break distinct and does not make one universal armor layer a prerequisite for all CC.

## Key ability-system findings

### WAKFU
- Demonstrates that a single persistent MMORPG character can support a broad learned/equipped spell system, including a large active deck and several passives.
- Rookvale uses a smaller visible loadout because turns, touch UI, Roblox portability, and one-action pacing favor faster reading.

### Guild Wars 2
- Separates weapon skills, selectable utilities, elite skills, and profession mechanics.
- Specializations combine fixed identity with selectable traits and can alter profession mechanics.
- Rookvale borrows the layered-build principle rather than its real-time hotbar structure.

### Last Epoch
- Five equipped skills gain substantial depth through per-skill specialization trees.
- Rookvale borrows meaningful skill transformation but reduces the production burden to lightweight Techniques on important skills rather than building a large tree for every skill.

### Grim Dawn
- Distinguishes active skills, passives, and local skill modifiers.
- Useful evidence for separating one-skill transformations from broader class/passive changes.

### Fell Seal: Arbiter's Mark
- Distinct active, passive, and counter layers provide a strong reference for a separate Reaction slot.
- Rookvale keeps reactions class-bound and applies strict non-full-turn / anti-recursion rules.

### Darkest Dungeon II
- Characters unlock more skills than they equip, and paths can alter how existing skills function.
- Useful reference for role-changing variants rather than simple stronger copies.

### TROUBLESHOOTER: Abandoned Children
- A deep mastery board can create enormous build variety through conditional interactions and mastery sets.
- It is also a warning against too many rigid slot categories and filler choices.
- Rookvale takes the rule-changing passive depth but keeps four selectable passives rather than a giant board.

### Battle Chasers: Nightwar
- Basic actions, temporary combat resources, perks, and Burst abilities demonstrate several ways to connect ordinary actions to stronger class moments.
- Rookvale does not use its shared party Burst-meter structure.

### Siralim Ultimate
- Specialization perks show how aggressively different passive rules can support unusual class fantasies.
- Rookvale uses this as a mechanic-idea source only; it is not a model for party or roster structure.

## Key class-roster findings

### Tree of Savior
- Official current listings demonstrate a very large fantasy range under a small set of broad ancestry trees.
- Its Re:Build developer posts are an important warning: later vertical tiers can invalidate earlier choices, while 80+ classes materially increase balance, concept, and maintenance burden.
- Rookvale therefore uses a broad design bank but staged implementation and more horizontal/asymmetric growth.

### Final Fantasy XIV
- Strong role readability, unique job actions/traits/gauges, and distinctive job fantasies are useful references.
- Rookvale does not copy its strict one-job/one-weapon economy because that would fragment loot too heavily for Rookvale's planned roster.

### World of Warcraft
- Warrior, Monk, Druid, Shaman and other classes demonstrate that a class can support several roles and several weapon types while keeping a recognizable mechanic/resource identity.
- Useful for designing broad ancestral weapon pools and hybrid classes.

### Orna / Hero of Aethric
- The current codex contains a very large class set, supporting the premise that long-lived single-character RPGs benefit from broad class fantasies and strong passives.
- Rookvale keeps the broad fantasy goal but rejects unrestricted cross-class skill collection as its default build model.

### MapleStory
- Useful for lineage readability: an early broad job decision limits later advancement to the selected family instead of freely crossing unrelated classes.

### Diablo IV
- Barbarian Arsenal is useful evidence that multiple weapon types can be part of one class identity rather than an exception that breaks the class system.

## Current production rules

See:

- `docs/01-gameplay/COMBAT.md`
- `docs/01-gameplay/COMBAT_VOCABULARY.md`
- `docs/01-gameplay/PROTOTYPE_NUMBERS.md`
- `docs/01-gameplay/PROTOTYPE_ENEMIES.md`
- `docs/01-gameplay/CLASSES_PROGRESSION.md`
- `docs/01-gameplay/CLASS_ROSTER_MASTER_PLAN.md`
- `docs/01-gameplay/ABILITY_LOADOUT_SYSTEM.md`
- `docs/07-research/COMBAT_STATUS_PROTOTYPE_RESEARCH_03.md`
- `docs/07-research/FIRST_COMBAT_PROTOTYPE_CROSSCHECK_02.md`
- `docs/07-research/CLASS_ROSTER_RESEARCH_02.md`
- `docs/07-research/SKILL_LOADOUT_PASSIVE_RESEARCH_02.md`

The long-term design bank is broad, but the first vertical slice implements only a small class subset. Ability production likewise starts narrowly, while the long-term research bank remains broad.

## Research rule

References are collected per system. A strong implementation may inspire a principle or mechanic, but the final design must fit Rookvale's own world, combat, multiplayer, pixel-art presentation, and cross-platform constraints.

For major systems, follow `RESEARCH_POLICY.md` before locking a design.
