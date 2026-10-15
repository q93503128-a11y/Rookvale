# Reference Matrix

**Status:** Active

This document tracks what Rookvale studies from external games and, equally importantly, what it does **not** copy from them.

| Design area | Reference candidates | What to study | Current Rookvale direction |
| --- | --- | --- | --- |
| Overworld -> turn-based encounter structure | Hero of Aethric, Broken Ranks | Exploration rhythm, encounter transition, world-content density, how multiplayer presence survives the transition into battle | Hero of Aethric is the primary structural reference; no GPS |
| Multiplayer exploration | Hero of Aethric, Broken Ranks, Loomian Legacy, WAKFU | Seeing other players, party formation, drop-in/out friction, social presence without overcrowding | Multiplayer is foundational, not a post-launch bolt-on |
| Party turn-based combat | WAKFU, DOFUS, Broken Ranks, For The King II | Sequential timing, waiting-time control, AFK/disconnect handling, role interaction | Sequential Speed-based timeline; normal player turn limit starts at 20 seconds; AFK/disconnect cannot stall combat |
| Combat activity / anti-passivity | Sea of Stars, Octopath-style break systems, Final Fantasy X-style timeline systems | Interrupts, break/stagger, readable future-turn pressure, keeping decisions active without reflex spam | Use selectively; no mandatory reflex minigame on every action |
| Tactical positioning | Etrian Odyssey, Darkest Dungeon, DOFUS/WAKFU | Front/back pressure, target rules, formation relevance, class interaction | Two-row front/back formation; front has higher default threat but back is not universally untargetable |
| Class identity and party roles | Guild Wars 2, Final Fantasy XIV, World of Warcraft, Tree of Savior, DOFUS/WAKFU | Class mechanics, role clarity, hybrid roles, same-class build diversity | Broad roster; each mature class should have a passive/resource/rule-changing identity and remain solo-capable |
| Large class-roster structure | Tree of Savior, Orna / Hero of Aethric, MapleStory | Large fantasy coverage, lineage readability, horizontal expansion, maintenance cost | Maintain an 80-100+ concept design bank but implement gradually; no symmetry requirement across trees |
| Class advancement | Tree of Savior, Guild Wars 2 specializations, MapleStory, Orna | Branch clarity, specialization depth, hidden classes, horizontal vs vertical growth | Deliberately asymmetric trees; branch only when gameplay/fantasy genuinely diverges; linear promotions must still add mechanics |
| Weapon/class relationship | Guild Wars 2, World of Warcraft, Diablo IV, Final Fantasy XIV | Multiple weapons per class, specialization weapon unlocks, loot fragmentation | Origin disciplines use related weapon pools, not one exact weapon; descendants may specialize or unlock additional weapons |
| Skill loadouts | Hero of Aethric / Orna, Guild Wars 2 | Learned pool versus equipped subset, readable hotbars, same-class build diversity | Class-bound skills; learn more than can be equipped; no random card draw and no unrestricted cross-class best-of hotbar |
| Class resources / gauges | Final Fantasy XIV, World of Warcraft, Guild Wars 2, Orna | Job gauges, Rage/Mana/Chi-like resources, class-specific mechanics | Cooldowns plus optional class-specific resources/stacks/marks; not every class uses universal MP or even a visible bar |
| Passives / traits | Guild Wars 2, Orna, MMORPG specialization systems | Rule-changing traits, innate passives, build choices | Major passives should change behavior more often than provide generic small stat bumps |
| Status effects / CC | Guild Wars 2, Darkest Dungeon, tactical RPGs | Hard/soft CC distinction, buffs/debuffs, boss resistance/break systems | Broad functional variety; avoid multiple differently named effects that all just mean “lose one turn” |
| Party finding | Broken Ranks and modern MMOs | Activity filters, role filtering, requirements, reducing party-formation friction | Treat party finder as core MMO UX, not late polish |
| Boss encounters | DOFUS/WAKFU, Broken Ranks, For The King II, selected JRPGs | Telegraphing, phases, role value, coordination checks, CC resistance, failure recovery | Open; boss-control system should preserve value for CC classes without allowing stun-locks |
| World / content variety | Hero of Aethric, DOFUS Touch, WAKFU, selected open-world RPGs | Regional identity, density of enemies/NPCs/dungeons/events, reasons to revisit old areas | Large handcrafted world with distinct spaces and broad content variety |
| Cross-platform tactical UI | WAVEN, DOFUS Touch, Broken Ranks mobile | Touch targets, HUD density, action selection, readable status info on small screens | Web-first implementation must stay within a Roblox/mobile-portable UI vocabulary |
| Roblox battle / exploration UX | Loomian Legacy and other suitable current Roblox RPGs | Controller/touch/mouse parity, menu scale, battle readability, Roblox player expectations | Research current Roblox games before final UI implementation |
| Pixel world presentation | Hero of Aethric plus selected high-quality pixel RPGs | Sprite scale, silhouette readability, environment density, animation economy, visual cohesion | No fixed cute/dark style yet; quality and readability take priority |
| Inventory / equipment UX | Modern mobile/PC RPGs selected per task | Information hierarchy, comparison speed, tooltips, touch usability | Open |
| Social / party UX | Broken Ranks and modern MMOs | Invite flow, reconnect behavior, party leader authority, readiness, matchmaking | Open |
| Deep system interaction | Divinity: Original Sin 2 | Systemic party skill interactions and encounter consequences | Depth reference only; do not inherit its slower encounter pacing by default |

## Key class-roster findings

### Tree of Savior
- Official current listings demonstrate a very large fantasy range under a small set of broad ancestry trees.
- Its Re:Build developer posts are an important warning: later vertical tiers can invalidate earlier choices, while 80+ classes materially increase balance, concept, and maintenance burden.
- Rookvale therefore uses a broad design bank but staged implementation and more horizontal/asymmetric growth.

### Guild Wars 2
- A profession combines weapon access, a profession mechanic, skills, and traits.
- Elite specializations demonstrate that a descendant can meaningfully change a core mechanic and historically often add weapon access.
- Rookvale borrows the principle that a specialization should change rules, not merely coefficients.

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

## Current class production rule

See:

- `docs/01-gameplay/CLASSES_PROGRESSION.md`
- `docs/01-gameplay/CLASS_ROSTER_MASTER_PLAN.md`
- `docs/07-research/CLASS_ROSTER_RESEARCH_02.md`

The long-term design bank is broad, but the first vertical slice implements only four origins and eight immediate advanced classes. Expansion happens only after those systems prove fun, readable, solo-viable, party-useful, and maintainable.

## Research rule

References are collected per system. A strong implementation may inspire a principle or mechanic, but the final design must fit Rookvale's own world, combat, multiplayer, pixel-art presentation, and cross-platform constraints.

For major systems, follow `RESEARCH_POLICY.md` before locking a design.
