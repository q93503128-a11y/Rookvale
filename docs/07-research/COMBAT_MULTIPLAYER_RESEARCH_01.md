# Combat & Multiplayer Research 01

**Status:** Research note — not final design.

## Confirmed Rookvale preferences

- Party combat is entered by an already-formed party or a player explicitly joining a party activity.
- Combat should feel like a true sequential turn-based RPG.
- Simultaneous action selection/execution is not the preferred default.
- Inactive, AFK, disconnected, or non-responsive party members must not be able to stall the whole fight indefinitely.

## External references

### WAKFU
- Sequential initiative queue.
- Each active character receives 30 seconds to act; timeout advances to the next turn.
- Players can manually end their turn early.
- Team battle supports reconnecting to an ongoing fight while teammates remain alive.
- Nearby group members can be prompted to join when another member starts a fight.

Sources:
- https://wakfu.wiki.gg/wiki/Combat
- https://wakfu.wiki.gg/wiki/Turn

### DOFUS
- Sequential turn-based combat.
- Roughly 30-second turn window; exceeding it skips/ends that character's turn.

Source:
- https://dofuswiki.fandom.com/wiki/Combat

### Broken Ranks
- Relevant because it combines an open-world MMORPG, parties, explicit support/tank/damage class roles, and turn-based combat.
- Its combat uses simultaneous planning with a 10-second action-selection window.
- Rookvale should study its class-role synergy and multiplayer encounter structure, but not adopt simultaneous turns by default.

Sources:
- https://brokenranks.com/en/faq/
- https://brokenranks.com/en/news/combat-system-in-broken-ranks

### Hero of Aethric
- World exploration -> turn-based encounter structure remains a primary broad reference.
- Official 2026 plans/updates emphasize visible players in towns, party formation, and overworld travel together, making its social-world direction worth monitoring.

Sources:
- https://playorna.com/aethric/
- https://blog.ornarpg.com/forge-forward-2026-recap-new-games-and-huge-updates/

### For The King / For The King II
- Uses one-character-at-a-time turns rather than simultaneous movement.
- Public reports and patches show how active-turn disconnect/desync can cause multiplayer softlocks.
- Rookvale should therefore keep turn progression server-authoritative and design disconnect recovery as a first-class rule rather than an afterthought.

Sources:
- https://steamcommunity.com/app/527230/discussions/0/2251181585642580249/
- https://steamcommunity.com/app/1676840/discussions/3/4366878568240628487/

## Strong candidate baseline for Rookvale

This is a proposal for discussion, not an accepted rule set.

1. Initiative-based sequential turns.
2. Visible turn-order timeline.
3. Manual `End Turn` button.
4. Per-turn time limit so one player cannot halt the encounter forever.
5. First timeout: character performs a safe fallback action and the turn ends.
6. Repeated inactivity: temporary auto-control or repeated auto-end until the player returns.
7. Short disconnect grace period with reconnect into the same battle.
8. Party leader cannot grief-kick a member in the middle of combat; party management occurs before/after encounters except for exceptional moderation cases.
9. Server owns the canonical combat state and turn clock.

## Open decisions to make with the project owner

1. Party size: 3 / 4 / 5 / 6?
2. Exact turn timer: fixed or context-sensitive? 15 / 20 / 30 seconds?
3. AFK fallback action: defend, guard, wait, basic attack, or class-specific AI?
4. How many consecutive missed turns before auto-control activates?
5. Disconnect grace duration and what happens after it expires.
6. Whether party members can temporarily control a disconnected player's character.
7. Whether enemies act as individual turns or enemy groups share turns to reduce waiting.
8. Initiative model: fixed by Speed stat, rerolled per battle, or player-adjustable through skills.
9. Whether adjacent allied turns may be freely reordered by the party.
10. Whether ordinary field encounters and boss/raid encounters use the same timing rules.
11. Party entry rules: automatic join for nearby party members, ready check, or explicit accept prompt.
12. Whether solo players can fill empty party slots with companions/mercenaries.

## Current recommendation

Do not finalize classes or the advancement tree until items 1-9 above are settled. Party size, initiative, timing, and AFK/disconnect behavior directly determine how enjoyable tanks, healers, buffers, revivers, and setup-heavy damage classes can be.
