# Platform Architecture

**Status:** Draft

## Platform strategy

The web build is the source implementation for early development and visual iteration. Rookvale should be structured so that Roblox and mobile versions can reproduce the same game rather than requiring a complete redesign.

## Portability principle

Separate portable game definition from platform adapters.

```text
Shared game definitions
  - game rules
  - stats and balance
  - classes and skills
  - enemies
  - items
  - encounters
  - maps / region metadata
  - animations
  - UI layout specifications where practical
  - asset metadata

Platform runtime
  Web
    - renderer
    - input
    - audio
    - networking adapter
    - persistence adapter
  Roblox
    - GUI / sprite renderer
    - Roblox input
    - audio
    - networking / server adapter
    - DataStore / platform services adapter
  Mobile package
    - chosen web-wrapper/native path to be decided later
```

## Rendering constraints

The web renderer should avoid depending on browser-only layout or graphics tricks for core game presentation when no Roblox equivalent or fallback exists. A canvas/game-renderer approach is preferable to building the game as a conventional DOM-heavy website.

## Multiplayer constraint

Networking technology is not locked yet. However, authoritative state boundaries and multiplayer-friendly state separation must influence the code architecture from the first playable build.

## Open technical decisions

- Canvas 2D versus WebGL-based renderer/framework.
- TypeScript/game framework choice.
- Server stack and authoritative model.
- World sharding / room model.
- Persistence model.
- Roblox data conversion pipeline.
- Mobile packaging path.
- Shared-data schema and validation.
