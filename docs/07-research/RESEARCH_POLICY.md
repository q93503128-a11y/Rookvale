# Rookvale External Research Policy

**Status:** Active
**Priority:** Highest before major design lock-in

Rookvale uses external game research as the first step for major systems. We do not finalize a major mechanic, UX flow, content structure, class system, combat rule, economy loop, or platform presentation solely from intuition when strong comparable games exist.

## Required workflow

1. **Research first**
   - Identify the closest structural analogue.
   - Identify at least one best-in-class reference for the specific system.
   - Identify at least one platform-specific reference when the system touches Web, mobile, or Roblox UX.
2. **Extract principles, not surface copies**
   - What problem does the reference solve?
   - Why does the implementation work?
   - What friction or failure cases does it create?
   - Which parts fit Rookvale and which do not?
3. **Prototype the Rookvale version**
   - Adapt the useful principle to Rookvale's multiplayer, pixel-art, web-first, cross-platform constraints.
4. **Inspect the actual result**
   - For Web builds, visually inspect the rendered game and UI.
   - Check common desktop and mobile aspect ratios.
   - Rework weak presentation or UX instead of assuming the first implementation is acceptable.
5. **Record the decision**
   - Update the relevant design document and `REFERENCE_MATRIX.md`.
   - Record rejected alternatives when the reason matters for later work.

## Minimum evidence per major system

A major system should normally have at least **three meaningful references** before it is locked:

- **Closest analogue** — a game solving nearly the same problem.
- **Best specialist** — a game especially strong at that particular mechanic or UX problem.
- **Platform reference** — a game proving the interaction works well on the target device/platform.

More references are expected when the design space is contested or the first examples disagree.

## Research categories

Research is not limited to mechanics. It includes:

- overworld exploration and content density
- turn-based battle structure and pacing
- multiplayer / party interaction
- tank, healer, damage, control and support roles
- class and advancement trees
- encounter and boss design
- progression, equipment and economy
- quests, dungeons, raids and world events
- social systems and party finder UX
- inventory and character-sheet UX
- pixel-art readability and animation
- HUD and combat UI
- mobile touch UX
- Roblox conventions and cross-device readability
- onboarding and early-game pacing
- retention loops and repeatable content

## Anti-copy boundary

Rookvale may study and adapt design principles, pacing structures, information hierarchy, interaction patterns, and broadly established genre mechanics. It should not reproduce another game's distinctive art, exact screen composition, text, names, lore, maps, characters, or unusually specific content expression.

## Current baseline references

- **Hero of Aethric** — overworld exploration into turn-based encounters; pixel RPG presentation; solo/party dungeon structure.
- **DOFUS / WAKFU** — long-running tactical turn-based MMORPG design, class identity and party interaction.
- **Broken Ranks** — open-world MMORPG plus party turn-based combat; simultaneous planning and defined party roles.
- **WAVEN** — compact tactical combat, cross-platform PC/mobile presentation, multiplayer and readable battle UI.
- **For The King II** — four-player cooperative turn-based party structure and role combinations.
- **Sea of Stars** — active feedback inside turn-based combat, especially timed input and interruption-style mechanics.
- **Divinity: Original Sin 2** — action-point economy, environmental combinations and deep party synergy; useful as a depth reference, not a pacing target.
- **Loomian Legacy** — Roblox-native exploration/battle UX and cross-device interface expectations; not a class-system reference.

## Rule for Rookvale

**If a major feature has strong external precedents, research them before designing the Rookvale version.**
