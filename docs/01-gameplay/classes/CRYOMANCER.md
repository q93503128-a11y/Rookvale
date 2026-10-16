# Cryomancer

**Status:** Draft for review and prototype; not locked

**Lineage:** Arcanist -> Cryomancer

**Primary role:** Control / protection / setup burst

**Secondary roles:** Speed suppression, barriers, row control, Break contribution

## Class fantasy

Cryomancer does not mirror Pyromancer with blue damage. It controls tempo through Chill, builds Frost states, creates protection with ice, and decides when to shatter accumulated control into burst or Break.

The central tension is:
**keep enemies chilled/frozen for control value vs. shatter Frost for immediate damage, Break or barrier value**.

## Weapon compatibility

Inherited Arcanist pool:
- staves;
- wands;
- orbs/foci;
- spellbooks.

## Innate mechanic — Frost

Enemies can accumulate **Frost** stacks/status through Cryomancer skills.

Frost is distinct from hard Freeze:
- Frost is a setup state that can lower Speed, improve Chill reliability, increase Break conversion, or enable Shatter;
- normal enemies may reach a Freeze threshold under specific skills;
- elites/bosses normally convert that threshold into heavy Break, action delay, or a temporary Vulnerable-Frozen state rather than repeated full turn loss.

This preserves control value without stun-locking bosses.

## Innate passive — Cold Front

Applying Chill/Frost for the first time in a bounded event window builds **Cold Front** value. At threshold, Cryomancer's next ice control/protection skill receives a stronger effect.

Cold Front should not be a passive per-turn resource that scales automatically with Speed.

# Active skill pool

## 1. Frost Bolt
**Type:** Attack / Frost generator

Reliable single-target ice attack. Applies Frost/Chill.

### Technique candidates
- **Needle Ice** — lower control, higher precision/direct damage.
- **Deep Chill** — stronger Speed suppression, lower direct damage.
- **Cracking Bolt** — adds Break against already-frosted targets.

## 2. Ice Lance
**Type:** Attack / setup payoff

Deals increased damage and/or Break against heavily Frosted targets. Does not consume all Frost by default.

## 3. Shatter
**Type:** Frost consumer

Consume Frost from one target to trigger one of several payoffs: damage, Break, or nearby pressure.

### Technique candidates
- **Fracture** — high single-target Break.
- **Crystal Burst** — row splash damage.
- **Preserve Core** — consumes fewer stacks and creates barrier instead of maximum damage.

## 4. Frozen Bind
**Type:** Hard/soft control

Against normal enemies, sufficient Frost can convert this into a temporary Freeze/turn-loss state. Against bosses/elites, instead apply major Break/action-delay contribution and a vulnerability window.

Long cooldown and strong resistance rules.

## 5. Ice Wall
**Type:** Party protection

Create a limited protection effect for one row or chosen ally. It absorbs a set amount/number of eligible direct hits rather than lasting indefinitely.

## 6. Glacial Armor
**Type:** Ally/self barrier

Grant a barrier that becomes stronger on targets already affected by Cryomancer protection or in the front row. Barrier can interact with selectable passives rather than only scale with defense.

## 7. Whiteout
**Type:** Enemy row debuff

Apply accuracy reduction / target-obscuring effect and modest Frost. This is control through information/precision, not hard stun.

## 8. Cold Snap
**Type:** Instant control conversion

Apply a small Frost burst and immediately evaluate Frost threshold for a weaker Freeze/Break effect. Useful for emergency control but less efficient than long setup.

## 9. Permafrost Mark
**Type:** Mark / setup

Mark one target so Frost decays more slowly or selected skills gain stronger interaction against it. Intended for bosses/long fights.

## 10. Sliding Current
**Type:** Row manipulation

Push/pull a legal target between rows or alter row pressure using ice. Against immovable bosses, convert the displacement value into Speed suppression/Break.

## 11. Winter's Gift
**Type:** Support

Grant one ally a bounded defensive boon: resistance to Burn/Heat, control, or incoming direct damage depending on Technique.

Cryomancer is not a full support class; this is situational protection.

## 12. Rime Field
**Type:** Persistent field/state

Apply a row-wide cold field for a limited number of action events. Enemies acting from that row accumulate Frost or suffer reduced Speed; strict event cap prevents abuse by very fast units.

## 13. Crystal Spear
**Type:** Direct burst

Strong direct spell that gains extra effect if target is Frozen/Break-vulnerable. Gives Cryomancer a clean damage option without consuming the entire class loop.

## 14. Absolute Zero
**Type:** High setup spender

Consume Cold Front/Frost setup for a major control/Burst event. Against bosses, designed primarily as Break + vulnerability, not guaranteed lost turn.

# Reaction candidates

## Frostguard
When an eligible direct hit targets Cryomancer, gain a small barrier and apply Frost to attacker. Internal cooldown.

## Snap Freeze
When an enemy with high Frost begins an eligible telegraphed attack, consume some Frost to reduce that action's effectiveness or add Break. Does not cancel scripted boss attacks outright.

## Ice Mirror
When targeted by a debuff/control spell, reduce/reflect a limited portion of its secondary effect. No recursive reaction chain.

# Signature candidates

## Winter Dominion
Create a battlefield winter state for a bounded number of action events. Enemy Speed/control resistance is pressured, ally barriers improve, and Frost application becomes easier. Does not continuously steal enemy turns.

## Crystal Prison
Focus on one dangerous enemy. Rapidly build a temporary frozen shell state. Normal enemies can be hard-frozen; bosses instead enter a high-Break / vulnerability window after the shell is shattered.

# Selectable passive candidates

- **Brittle Ice** — Shatter produces more Break, less raw damage.
- **Deep Winter** — Chill/Speed suppression lasts through more action events, but direct burst is lower.
- **Protective Rime** — consuming Frost creates small barriers for allies.
- **Cold Blooded** — Cryomancer gains control resistance while Cold Front is ready.
- **Permafrost** — marked targets retain Frost more efficiently.
- **Glass Glacier** — barriers are smaller but shattering them offensively generates Frost/Break.
- **Snowblind** — Whiteout/accuracy control stronger; Freeze threshold harder to reach.
- **Avalanche** — row/displacement skills gain damage/Break when movement is resisted.
- **Controlled Fracture** — Shatter consumes only a capped number of stacks and leaves residual Frost.
- **Stillness** — if Cryomancer does not change rows between natural turns, next control spell gains reliability; no direct Speed gain.

# Solo viability

Cryomancer can control a single boss through Frost -> Break conversion, maintain barriers, and use Crystal Spear/Shatter for damage. It does not need multiple enemies for Rime/Freeze economy.

# Party identity

Cryomancer brings:
- Speed/timeline suppression;
- barriers;
- controlled hard CC on normal enemies;
- boss-safe Break conversion;
- row control;
- vulnerability windows for allies.

It should feel radically different from Pyromancer's attrition/combustion cycle.

# Prototype questions

- exact Frost stack/threshold model;
- how Freeze interacts with enemy Speed and natural-turn queue;
- boss conversion ratio from Freeze to Break;
- whether barriers scale from magic power, max HP, or class-specific coefficients;
- whether Rime Field uses action-event count or owner natural turns;
- whether Cryomancer should have any direct cleanse of Burn/Heat in first slice.
