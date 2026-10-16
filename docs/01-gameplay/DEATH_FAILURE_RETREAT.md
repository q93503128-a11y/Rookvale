# Death, Revival, Dungeon Failure, and Retreat

**Status:** Core philosophy locked; exact revival limits, retry counts, checkpoint spacing, and class-specific death-response kits remain Draft

## Core philosophy

Rookvale makes defeat matter primarily **inside the encounter and the current run**, not by deleting long-term progression or confiscating important possessions.

The game does not use routine death penalties such as:

- lost Character XP or levels;
- lost Class Mastery;
- dropped equipped gear;
- permanent equipment damage;
- large Gold loss;
- deletion of already-secured exploration discoveries or completed progression.

Failure should cost encounter progress, run progress where appropriate, time, and resources actually spent during the attempt. It should not make players afraid to explore because one mistake can erase hours of persistent progress.

## 0 HP and Fallen state

When a character reaches 0 HP in combat, the character enters **Fallen** state and is removed from ordinary action flow.

A Fallen character:

- does not take ordinary Natural Turns;
- cannot use ordinary actions;
- remains part of the encounter state;
- may be restored only by an effect explicitly capable of responding to Fallen characters;
- automatically recovers after the encounter if the party wins, unless a specific content rule states otherwise.

Fallen is a mechanical combat state and does not require every 0-HP event to be interpreted as literal canonical death. Individual classes may express their death-response fantasy differently.

## No universal in-combat revive action

Rookvale does **not** give every character a generic `Revive Ally` action.

Bringing death-response capability is a party-building and preparation choice. If a party enters dangerous content with no way to recover a Fallen member, that is a legitimate risk the party accepted.

However, death response should not be monopolized by one mandatory class forever. Multiple classes/lineages may eventually provide different forms of response, for example:

- true resurrection;
- emergency resuscitation;
- death prevention / cheat-death effects;
- delayed restoration;
- limited self-recovery;
- temporary substitute bodies or death-state manipulation.

The exact class roster and skill implementations are not locked here.

Ordinary consumables do not provide a cheap universal in-combat resurrection that makes class preparation irrelevant. Rare bespoke items or encounter-specific tools may exist only when a specific content design calls for them.

## Revival Strain / repeated resurrection

True in-combat restoration from Fallen state is bounded.

Repeated restoration in the same encounter should accumulate an encounter-only **Revival Strain** or equivalent limitation so a resurrection-capable party cannot create an infinite death/revive loop.

Possible effects include:

- reduced HP restored;
- temporary maximum-HP reduction;
- reduced recovery effectiveness;
- eventual inability to receive another ordinary resurrection in that encounter.

Exact numbers and the maximum number of restorations remain Draft.

Revival Strain clears when the encounter ends. It is not a persistent injury system.

## Future corpse / undead manipulation design space

A future Necromancer-like class may explore mechanics such as temporarily turning a Fallen ally into an undead proxy, corpse-puppet, revenant, or similar substitute rather than performing a normal resurrection.

This is **not yet a locked class mechanic**. It is retained as a promising example of how death-response systems can support strong class identity instead of every class sharing one generic revive button.

If implemented later, the mechanic should preserve player agency where possible—for example by letting the Fallen player control the temporary proxy rather than forcing them to watch passively.

## Solo defeat

In solo play, reaching Fallen with no self-recovery or other valid death-response effect available causes encounter defeat.

Self-resurrection, death prevention, or substitute-life mechanics may exist on specific classes/items, but the game does not give every solo character a free universal extra life by default.

## Victory while a party member is Fallen

If the remaining party wins the encounter, Fallen members recover after combat.

A player who met Meaningful Participation requirements before becoming Fallen receives normal eligible rewards:

- Character XP;
- Class Mastery XP;
- personal loot;
- clear credit;
- progression credit where otherwise eligible.

Dying shortly before the boss falls is not itself a reason to strip the player of rewards.

## Field defeat

A full party defeat in ordinary overworld combat returns the party/players to an appropriate discovered recovery point such as a town, camp, shrine, waystone, or other world-system equivalent.

The exact fiction and checkpoint network are defined with world design later.

Field defeat does not remove secured long-term progression or owned equipment/currency.

The player loses:

- progress in the unfinished encounter;
- unearned/unsecured rewards from that encounter;
- consumables or one-use resources actually spent during the attempt;
- some travel/time through returning from a recovery point.

## Content-specific dungeon failure contracts

Rookvale deliberately does **not** use one universal wipe rule for every dungeon.

The failure contract must be visible before or at entry so players know what kind of commitment they are making.

### A. Standard progression dungeon

Purpose: story, ordinary progression, exploration, standard multiplayer.

Default rules:

- no finite run-life counter;
- full-party wipe resets the current encounter;
- party returns to the latest meaningful dungeon checkpoint;
- bosses reset fully;
- already-secured major dungeon progress before the checkpoint remains secured;
- one wipe does not force a complete dungeon restart.

This keeps ordinary progression from becoming a runback tax.

### B. Limited-retry expedition / challenge dungeon

Some dungeons, expeditions, hunts, or challenge runs may use a visible **shared Retry Stock** (working term).

Example structure only:

```text
Retry Stock: 3
Party wipe -> Retry Stock -1 -> return to checkpoint
Retry Stock reaches 0 and party wipes again -> Run Failed
```

Exact counts are content-specific and remain Draft.

Important rules:

- the stock is shared by the run, not one stock per character;
- an individual becoming Fallen does not automatically consume a retry;
- a retry is normally consumed by a full-party encounter failure/wipe;
- successful resurrection or winning short-handed can therefore save a retry;
- if the run fails, run-specific progress resets according to that dungeon's contract, commonly to the dungeon start;
- permanent account/character progression already secured before the run is not deleted.

This model makes death-response composition meaningful without making the tank's individual KO directly burn the entire group's limited lives.

### C. No-retry / deep-run challenge content

Rare optional challenge content may use a harsher contract:

- no retry stock, or one effective life;
- full-party wipe ends the run;
- some or all run progress is reset;
- rewards are correspondingly prestigious;
- the rule is prominently disclosed before entry.

This is suitable for optional deep-dungeon, gauntlet, survival, or prestige formats, not ordinary required progression.

### D. Raid / pinnacle boss learning content

Complex raids and pinnacle bosses should **not automatically inherit a whole-run life limit** on their ordinary difficulty.

Default learning-friendly rule:

- party wipe resets the boss encounter;
- party returns to the boss checkpoint;
- repeated attempts are allowed;
- key-entry items follow the separate rule that all eligible participants must own their own required key and the key is consumed only when the successful reward/clear is committed.

A special prestige/challenge variant may add limited attempts, shared retry stock, or other harsher failure rules if its rewards and UI clearly communicate that contract.

### E. Advancement content

Mandatory Character Tier or class-advancement content cannot become an indefinite failure wall.

It follows the existing Advancement Content principles:

- retry is allowed;
- character growth, equipment, build changes, and preparation matter;
- repeated failure may unlock clearer guidance or optional assistance where appropriate;
- clearing with assistance remains legitimate progression.

## Optional alternative failure conditions

Some bespoke quests may fail for reasons other than a total party wipe when the fiction requires it, such as:

- time limit;
- protected NPC/objective destroyed;
- required target escapes;
- forbidden target killed;
- objective condition violated.

These are content-specific exceptions and must be shown clearly. Rookvale does not silently hide arbitrary failure conditions from the player.

## Retreat

Retreat is intentionally a small utility system rather than a major build axis.

### Standard field retreat

Ordinary eligible encounters allow a deterministic Retreat action or party retreat command.

Core rules:

- no percentage-based flee RNG;
- retreat should resolve quickly rather than require a long minigame;
- unfinished encounter rewards are forfeited;
- enemy encounter state resets appropriately;
- resources/consumables actually spent remain spent;
- retreat itself does not impose an additional major death penalty.

Exact turn timing and party-confirmation UX remain Draft.

### Retreat-related abilities

Some classes/items may improve retreat in small ways, such as:

- faster retreat resolution;
- protecting allies during withdrawal;
- avoiding a minor retreat inconvenience;
- enabling retreat from a narrow class of otherwise awkward encounters.

Retreat-related utility should remain a side benefit, not consume a large portion of a class's power budget unless a future specialist class is deliberately designed around exploration/escape.

### No-retreat encounters

Some content may forbid retreat:

- major bosses;
- advancement encounters;
- sealed arenas;
- specific scripted ambushes/incidents;
- pinnacle challenge fights.

Where practical, `Retreat unavailable after engagement` is disclosed before the player commits.

## Failure and key-entry content

For endgame content that requires an entry/key material:

- every participating reward-eligible player must individually possess the required key/material;
- the party cannot enter with one player's key covering everyone;
- keys are reserved/validated at entry;
- keys are consumed when the successful clear/reward is committed;
- ordinary wipe or voluntary failed attempt does not consume the key by default.

This supports learning difficult encounters without allowing one player's entry material to multiply into four players' reward rolls.

## Design invariants

1. Persistent progression is not routinely destroyed by death.
2. In-combat resurrection is a build/party capability, not a universal button.
3. No single specific class must be the only possible source of death response across the full game.
4. Repeated resurrection inside one fight is bounded.
5. Dungeon failure rules are content-specific and disclosed.
6. Standard required progression is forgiving enough to learn.
7. Optional challenge content may legitimately reset a whole run.
8. Retreat is deterministic and relatively simple where allowed.
9. Death does not erase meaningful participation rewards if the party ultimately wins.

## Open questions

- final public terminology for Fallen / Revival Strain / Retry Stock;
- exact Revival Strain behavior and maximum revival count;
- which initial and future classes receive true resurrection, death prevention, or alternative death-response mechanics;
- checkpoint spacing and local enemy-reset policy;
- exact Retry Stock counts by challenge format;
- whether some run formats can earn an extra retry from an in-run objective;
- exact solo self-recovery availability;
- retreat timing and multiplayer vote/confirmation UX;
- future Necromancer corpse-proxy mechanic feasibility and identity.
