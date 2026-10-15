# Multiplayer and Parties

**Status:** Draft

## Core assumption

Rookvale is designed as multiplayer-first even though solo play should remain viable.

## Desired social presence

Players should be able to encounter and travel with other players in the world. Party play should extend naturally from exploration into turn-based combat.

## Party design principles

- Party roles must create cooperation, not merely combined DPS.
- Joining friends should be straightforward.
- Standard exploration should not require a perfectly composed party.
- Harder content may deliberately reward specialization and coordination.
- Solo players should retain a credible progression path.

## Architecture consequences

Even before online networking is fully implemented, game state should be separated conceptually into:

- player state;
- party state;
- world state;
- encounter/combat state;
- persistent progression state.

This prevents a single-player prototype from becoming structurally incompatible with multiplayer later.

## Open questions

- Standard and maximum party size.
- Shared overworld population model.
- Instanced versus shared combat spaces.
- Loot ownership and reward rules.
- Level-gap handling.
- Revive/downed mechanics.
- Matchmaking versus friend/invite emphasis.
- Drop-in/drop-out behavior during exploration and combat.
- Guilds, trading, PvP, and other social systems are not yet committed.
