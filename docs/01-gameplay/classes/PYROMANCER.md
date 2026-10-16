# Pyromancer

**Status:** Draft for review and prototype; not locked

**Lineage:** Arcanist -> Pyromancer

**Primary role:** Damage-over-time pressure / combustion burst / resource conversion

**Secondary roles:** Area pressure, anti-heal, self-buffing, limited support through Haste/cleansing heat effects where justified

## Class fantasy

Pyromancer is not `red Mage with higher fire numbers`. It creates heat, applies Burn, converts Burn into burst or Ash, and chooses whether to let fire keep ticking or consume it now.

The key tension is:
**spread/maintain fire for long value vs. detonate/consume it for immediate payoff**.

## Weapon compatibility

Inherited Arcanist pool:
- staves;
- wands;
- orbs/foci;
- spellbooks.

Weapon subtype may affect Technique access or scaling behavior later, but does not create duplicate skill lists.

## Innate mechanic — Ash

Prototype cap: **6 Ash**.

Gain Ash through several non-kill sources:
- first application of Burn to a target within a limited event window;
- consuming/detonating Burn with selected skills;
- selected direct fire skills;
- bonus Ash when a burning enemy dies.

Enemy death is explicitly a bonus accelerator, never the core engine.

Ash is spent to:
- intensify Burn;
- change direct spells into combustion effects;
- shorten/reshape selected cooldowns;
- create defensive heat/barrier options;
- empower Signature effects.

## Innate passive — Living Flame

Burn applied by Pyromancer has two tactical values:
1. damage over time;
2. a stored state that certain skills can consume, transfer, extend, or transform.

A Pyromancer who only stacks Burn forever should be viable but not always optimal; a Pyromancer who consumes every Burn immediately should also lose long-term pressure.

# Active skill pool

## 1. Ember Bolt
**Type:** Attack / resource generator

Reliable single-target fire attack. Applies a light Burn or grants Ash when striking an already-burning target, using event caps to prevent multi-hit farming.

### Technique candidates
- **Kindling Bolt** — weaker direct hit, stronger Burn setup.
- **Cinder Bolt** — no new Burn; gain extra Ash against burning target.
- **Piercing Ember** — can reach/pressure a second target or back row at reduced damage.

## 2. Flame Lash
**Type:** Attack / spread

Strike a burning target and spread part of its Burn state to one legal secondary enemy without copying the full stack count.

## 3. Combust
**Type:** Burn consumer / burst

Consume some or all Burn from one target to deal immediate damage based on remaining Burn value and gain Ash.

This is the defining conversion tool.

### Technique candidates
- **Controlled Burn** — consumes only part of Burn, lower burst, better sustained pressure.
- **Flashover** — consumes all Burn for larger burst and stronger cooldown.
- **Ash Harvest** — lower damage; converts more consumed Burn into Ash.

## 4. Fireball
**Type:** Direct area attack

Moderate burst to one target plus splash/row pressure. Applies a small Burn but is not automatically the best Burn generator.

## 5. Scorching Brand
**Type:** Mark / anti-heal

Apply Brand. Healing received by the enemy is reduced or partially converted into additional Burn/Ash interaction, with boss-safe limits.

## 6. Heat Wave
**Type:** Row pressure / soft control

Damage an enemy row and apply Heat: reduced resistance to Burn or slight Speed suppression depending on final tuning.

Heat is not a full stun.

## 7. Backdraft
**Type:** Setup / delayed effect

Place a delayed fire state on one target. If Burn is added/consumed before the target's next natural turn, trigger an additional effect.

Encourages planning without needing real-time timing.

## 8. Flame Ward
**Type:** Defensive utility

Spend Ash to create a temporary heat barrier. When struck by eligible direct attacks, attacker receives a small Burn or the ward converts damage into Ash once per event cap.

Pyromancer gains survival without becoming a tank.

## 9. Searing Haste
**Type:** Self/ally support

Spend Ash to grant a bounded timeline/Speed benefit that improves one upcoming action rather than a long multiplicative Speed buff.

Exact form should avoid double/triple-dipping with the Speed system.

## 10. Cauterize
**Type:** Utility / risky cleanse

Remove one Bleed/organic wound-type status from self or ally and replace it with a small temporary Burn/Heat cost or reduced healing state.

Not a general Priest cleanse.

## 11. Smolder
**Type:** Burn maintenance

Extend/refresh Burn on one target and gain a small setup benefit. Useful in boss fights where enemies are not dying.

## 12. Firebreak
**Type:** Defensive/utility

Consume Burn from an enemy to reduce its next outgoing damage or create a temporary barrier on the Pyromancer/ally. Converts offense into emergency survival at a cost.

## 13. Ashen Spear
**Type:** Ash spender / precision

Spend 2-3 Ash for a strong direct attack. Gains a different bonus depending on whether the target is burning heavily, lightly, or not at all.

## 14. Wildfire
**Type:** Multi-target attrition

Spread moderate Burn across several targets/row. Expensive cooldown or Ash cost so it does not dominate single-target boss combat.

# Reaction candidates

## Flame Reprisal
When directly struck, apply a small Burn to attacker and gain limited Ash once per Reaction cooldown.

## Emergency Flare
When targeted by an eligible control/debuff action, consume Ash to reduce its effectiveness and apply Heat to the attacker.

## Cinderstep
On receiving a heavy direct hit, shift row position if legal and leave a small Burn/pressure effect. No extra natural turn.

# Signature candidates

## Furnace Heart
Enter a temporary altered resource state: Ash cap/flow changes, Burn application becomes easier, and Combust-style skills gain new tradeoffs. The Pyromancer becomes more dangerous but takes a self-risk such as reduced healing received or accumulating Heat on self.

## Conflagration
Choose an enemy row or primary target. Existing Burns are not simply erased; instead they are temporarily synchronized into a large pressure event that can either detonate partially or spread depending on current setup.

# Selectable passive candidates

- **Everlasting Ember** — first Burn refresh each cycle also grants Ash.
- **Ashen Economy** — consuming Burn returns more Ash but direct burst is reduced.
- **Flashpoint** — high Burn stacks improve Break/interrupt contribution.
- **Cauterist** — Cauterize becomes safer and gains small barrier utility.
- **Heat Sink** — spending Ash reduces one bounded self-risk or defensive cooldown.
- **Wildfire Doctrine** — spreading Burn is stronger; single-target Combust is weaker.
- **Furnace Doctrine** — direct Ash spenders stronger; passive Burn spread weaker.
- **Fuel the Flame** — Burn on bosses generates periodic Ash through action events, ensuring long fights remain functional.
- **Searing Rhythm** — alternating direct fire and Burn-consumer skills grants a capped temporary benefit.
- **Backdraft Savant** — delayed fire states gain stronger payoff but longer setup.

# Solo viability

Solo Pyromancer can generate Ash through Burn application, Smolder, Ember Bolt and Combust without adds. Defensive Ash spenders prevent the class from becoming a glass cannon that requires a healer.

# Party identity

Pyromancer contributes:
- sustained damage;
- planned burst from existing DoT;
- anti-heal;
- area pressure;
- limited timeline/support options;
- synergy with allies that extend/expose status windows without requiring them.

# Prototype questions

- exact Burn stacking model;
- whether Ash comes from first Burn application per target, per action, or per cycle;
- how much Burn Combust consumes baseline;
- whether Searing Haste should target allies in first slice;
- exact difference between Heat and Burn;
- how much anti-heal is acceptable in PvE/PvP if PvP arrives later.
