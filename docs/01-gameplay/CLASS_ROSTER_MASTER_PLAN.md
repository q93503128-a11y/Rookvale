# Class Roster Master Plan

**Status:** Broad design bank approved; exact final roster remains iterative

Rookvale is a single-avatar RPG, not a character-collection game. Class variety therefore has to carry a large share of long-term identity, replay value, party-role variety, aesthetics, and build expression.

The design strategy is deliberately asymmetric:

- design a very broad class bank first;
- implement only a small representative subset first;
- expand only after the combat, skill-loadout, resource, passive, and advancement systems prove fun;
- do not force every lineage to have the same number of branches or the same depth;
- do not create a branch unless it has a distinct fantasy and a distinct gameplay loop;
- do not make promotions feel like `Fireball -> Bigger Fireball -> Biggest Fireball`;
- class-bound active skills remain the default;
- related descendants may share ancestral weapons, but a descendant may specialize in or unlock additional weapon families.

## Research-derived scale rule

Large class rosters are valuable but expensive to maintain. Tree of Savior has historically demonstrated both sides: a very large roster creates strong fantasy/build breadth, while its developers have also publicly discussed the balancing, concept, and maintenance burden of an 80+ class environment.

Therefore Rookvale should keep a **large design bank** without committing to implement every designed class immediately.

Current planning scale:

- roughly **11 origin disciplines**;
- roughly **80-100+ advanced-class concepts** available as a long-term design bank;
- only a small subset enters the first playable slice;
- classes graduate from design-bank status to production only after their mechanic is distinct enough to justify implementation and maintenance.

## Origin-discipline model

An origin discipline is not a single weapon lock. It is a broad combat tradition with a related weapon pool. Descendants inherit that pool unless their identity narrows it, and some descendants may unlock an additional weapon family.

The origin discipline defines:

- broad equipment compatibility;
- ancestral combat vocabulary;
- early passive/resource identity;
- the part of the class tree that descendants are allowed to inherit skills from;
- a coherent loot family without requiring one unique weapon type per class.

## 1. Armsman

**Core weapons:** one-handed blades, maces, shields, spears/polearms.

**Core fantasy:** disciplined martial combat, protection, precision, formations, commands.

Candidate lineage bank:

- **Knight** — threat control, guarding, interception, Resolve.
  - Guardian — maximum ally protection and damage redirection.
  - Lancer — spear specialization, back-row pressure, anti-large-target attacks.
  - Paladin — defensive holy hybrid; may unlock sacred focus interactions.
- **Duelist** — parry, riposte, precision, tempo.
  - Fencer — speed and counter windows.
  - Sword Saint — fewer but highly committed precision strikes.
- **Dragoon** — polearm reach, armor piercing, large-target hunting.
  - Sky Lancer — timeline leaps and delayed impact attacks.
- **Warlord** — command buffs, marks, formation leadership.
  - Banneret — party buffs and threat redistribution.
- **Gladiator** — counterplay, enemy-reading, risk/reward dueling.
- **Rune Knight** — hidden/advanced martial-magic path; weapon enchantment rather than generic spellcasting.

## 2. Marauder

**Core weapons:** greatswords, greataxes, heavy maces/hammers, heavy polearms.

**Core fantasy:** commitment, stagger, armor breaking, rage, high-risk front-line damage.

Candidate lineage bank:

- **Berserker** — Rage, self-risk, momentum through taking/dealing damage.
  - Bloodrager — HP-risk burst and recovery windows.
  - Ravager — sustained aggression and escalating pressure.
- **Juggernaut** — stagger resistance, heavy guard, unstoppable actions.
  - Colossus — very slow, very high commitment attacks and protection.
- **Reaver** — executions, wounds, anti-healing, fear pressure.
  - Dread Reaver — fear/debuff hybrid.
- **Breaker** — break/stagger specialist, boss-control contribution.
- **Executioner** — target thresholds and finishing attacks.
- **Warmonger** — offensive party aura and enemy pressure rather than pure personal DPS.
- **Doomhammer** — heavy blunt specialization and delayed-impact skills.

## 3. Ranger

**Core weapons:** bows, crossbows, light spears; some descendants may unlock firearms.

**Core fantasy:** target selection, ranged pressure, traps, tracking, pets, precision.

Candidate lineage bank:

- **Ranger** — flexible ranged generalist.
  - Pathfinder — exploration utility, marks, adaptable ammunition/effects.
  - Warden Archer — defensive ranged support and ally covering fire.
- **Marksman** — deliberate high-value shots.
  - Sharpshooter — long setup, high precision, exposed-target exploitation.
- **Hunter** — prey marks and creature knowledge.
  - Beastmaster — persistent animal companion emphasis.
  - Falconer — scouting, assists, target disruption.
- **Trapper** — prepared effects, row control, conditional CC.
  - Sapper — explosive/area denial specialization.
- **Arcane Archer** — advanced branch using enchanted ammunition without becoming a generic Mage.
- **Musketeer** — firearm unlock, slow heavy ranged shots.

## 4. Rogue

**Core weapons:** daggers, rapiers, light swords, thrown weapons.

**Core fantasy:** speed, evasion, marks, poison, stealth-like setup, target manipulation.

Candidate lineage bank:

- **Assassin** — marked-target burst and execution windows.
  - Shadowblade — timeline manipulation and evasive follow-ups.
  - Nightblade — darkness/debuff hybrid.
- **Venomist** — poison stacking, debuff conversion, anti-healing.
- **Swashbuckler** — agile duelist/support, taunts, risky counters.
  - Corsair — opportunistic utility and loot/exploration flavor without combat RNG dependence.
- **Shinobi** — clones/decoys, delayed techniques, evasive setup.
- **Trickster** — misdirection, target manipulation, buff/debuff interference.
- **Gambler** — controlled risk mechanics; avoid uncontrolled party-grief randomness.
- **Acrobat** — very high Speed, turn-frequency tools, evasion.
- **Phantom** — illusionary feints and enemy-intent manipulation.

## 5. Pugilist

**Core weapons:** fist weapons, gauntlets, quarterstaves, selected blunt weapons.

**Core fantasy:** stance, combo rhythm, counters, body control, grappling, Chi.

Candidate lineage bank:

- **Monk** — Chi cycle, disciplined offense/support.
  - Grandmaster — stance mastery and conditional skill transformation.
  - Spirit Fist — Chi projection and support/control.
- **Brawler** — straightforward pressure and reactive counters.
  - Iron Body — defensive bruiser/tank path.
- **Grappler** — displacement, front/back-row manipulation, enemy control.
  - Luchador — spectacle/risk-reward control path.
- **Staff Adept** — reach, sweeping row attacks, defensive parries.
- **Wind Fist** — Speed manipulation and rapid natural turns.

## 6. Arcanist

**Core weapons:** staves, wands, orbs/foci, spellbooks.

**Core fantasy:** formal magic, Mana management, elements, time/space, illusion, constructed summons.

Candidate lineage bank:

- **Pyromancer** — Burn, heat buildup, Ash generation.
  - Infernalist — high-resource burst and self-risk.
  - Ashcaller — DoT spread, detonation, battlefield attrition.
- **Cryomancer** — Slow, freeze setup, protection.
  - Frostwarden — barriers and defensive ice control.
  - Glaciomancer — shatter/burst after freeze setup.
- **Storm Mage** — shock, speed/timeline pressure, chaining effects.
  - Tempest — multi-target/control emphasis.
  - Thunder Sage — single-target overload and timeline disruption.
- **Chronomancer** — delay, haste, cooldown/timeline manipulation.
  - Epoch Weaver — advanced turn-order control with strict anti-loop rules.
- **Illusionist** — decoys, enemy-intent distortion, miss/target manipulation.
- **Conjurer** — elementals/constructs rather than undead or beasts.
- **Battlemage** — may unlock one-handed blades; Mana-to-defense/offense conversion.
- **Gravity Mage** — row displacement, speed suppression, heavy delayed spells.
- **Runecaster** — prepared rune states and conditional spell modification.
- **Sage** — broad high-level arcane control; not merely a stat-upgrade Mage.

## 7. Acolyte

**Core weapons:** maces, staves, shields, holy foci/books.

**Core fantasy:** healing, protection, cleansing, faith, prophecy, anti-curse, battle support.

Candidate lineage bank:

- **Priest** — direct healing, Grace, cleansing.
  - Hierophant — stronger ritual/party support and resource support.
  - Saint — prevention, rescue, revival emphasis.
- **Oracle** — prediction, enemy intent, future-turn manipulation.
  - Astrologer — buffs/debuffs through omen cycles.
- **Crusader** — front-line divine hybrid.
  - Battle Cleric — damage/healing conversion and front-row support.
- **Exorcist** — anti-summon, anti-curse, banishment, purification.
- **Inquisitor** — mark/punish enemy buffs and dangerous casting.
- **Scholar** — barriers, planned healing, tactical support.
  - Ward Sage — prevention-first healer/support.
- **Plague Doctor** — cleansing, disease manipulation, prevention and risky medicine.

## 8. Occultist

**Core weapons:** ritual books, staves, ritual blades/foci; some descendants may unlock scythes or other signature weapons.

**Core fantasy:** forbidden magic, death, blood, curses, spirits, contracts.

Candidate lineage bank:

- **Necromancer** — corpses/death events, undead summons, life force.
  - Bonecaller — skeletal constructs and defensive summons.
  - Grave Lord — persistent undead army/control emphasis.
  - Spirit Binder — fewer summons, more soul manipulation and debuffs.
- **Blood Mage / Hemomancer** — HP sacrifice, lifesteal, blood resource.
  - Crimson Sage — controlled HP conversion and party-support blood magic.
  - Sanguine Knight — optional weapon unlock and front-line blood hybrid.
- **Hexer** — curses, debuff layering, condition amplification.
  - Curseweaver — spread/transfer/transform debuffs.
- **Warlock** — pact resource, dangerous borrowed power.
  - Demonologist — summoned pact entities.
  - Pactbinder — fewer summons, stronger personal contract mechanics.
- **Shadowmancer** — darkness, blindness, target denial and evasive magic.
- **Soul Reaper** — advanced death-resource spender; possible scythe unlock.

## 9. Warden

**Core weapons:** staves, spears, bows, natural/totemic foci.

**Core fantasy:** nature, spirits, beasts, shapeshifting, totems, terrain-like control.

Candidate lineage bank:

- **Druid** — nature magic and flexible support/damage.
  - Shapeshifter — form-based role changes with strict turn readability.
  - Grovekeeper — healing-over-time, roots, protection.
- **Shaman** — spirits/elements/totems.
  - Totemist — persistent support/control objects or effects.
  - Storm Shaman — offensive elemental/spirit hybrid.
- **Beastmaster** — animal companion specialization distinct from Ranger Hunter by emphasizing bond mechanics over ranged prey gameplay.
  - Packlord — multiple weaker companions or rotating beast calls.
- **Spiritwalker** — spirit-state buffs, cleanse, spectral utility.
- **Geomancer** — earth/terrain-like row control, defense, stagger.
- **Wildspeaker** — buffs/debuffs through creature/nature aspects.

## 10. Artificer

**Core weapons:** firearms, hammers, gadget foci; some branches unlock cannons or specialty devices.

**Core fantasy:** technology, alchemy, constructs, ammunition, devices, preparation.

Candidate lineage bank:

- **Engineer** — gadgets and adaptable utility.
  - Machinist — personal weapons platform and firearm specialization.
  - Automatonist — construct companion focus.
- **Gunsmith** — firearm modifications and ammunition states.
  - Cannoneer — heavy firearm/cannon unlock and delayed burst.
- **Alchemist** — mixtures, transmutation, status interactions.
  - Transmuter — converts buffs/debuffs/resources rather than simple potion spam.
  - Bombardier — volatile mixtures and row/AoE pressure.
- **Apothecary** — medicine, cleanse, poison, prevention; support/damage hybrid.
- **Runesmith** — equipment/weapon augmentation in combat; distinct from Arcanist Runecaster.
- **Gadgeteer** — traps, emergency tools, utility-heavy support.

## 11. Performer

**Core weapons:** light blades, bows, instrument/focus equipment.

**Core fantasy:** rhythm, morale, performance, distraction, party tempo, emotional/sonic magic.

Candidate lineage bank:

- **Bard** — broad party buffs, debuffs, song states.
  - Minstrel — healing/support emphasis.
  - War Chanter** — offensive party tempo and morale.
- **Dancer** — movement/tempo buffs and enemy disruption.
  - Blade Dancer — light-weapon offensive hybrid.
- **Skald** — martial songs, front-line support, fear resistance.
- **Piper** — charm-like control, enemy action manipulation, summons/creature influence where appropriate.
- **Jester** — disruption, debuff inversion, misdirection.
- **Conductor** — party timeline orchestration without requiring manual ally turn reordering.
- **Dirge Singer** — anti-morale, fear, death/low-HP support; thematically dark without inheriting Occultist skills.

## Weapon-family policy

Weapon compatibility is broad enough to support class fantasy but narrow enough to keep loot understandable.

Suggested system-level families:

1. one-handed blades;
2. heavy blades / axes;
3. maces / hammers;
4. shields;
5. polearms;
6. daggers / finesse weapons;
7. fist weapons;
8. bows / crossbows;
9. firearms;
10. arcane/ritual foci (staff, wand, tome, orb variants can share economy rules where useful);
11. specialist/signature weapons that normally derive from an existing family rather than creating a new economy for every class.

A visual subtype does not automatically require a separate loot family. For example, a scythe may be treated internally as a polearm/heavy-focus hybrid if that avoids unnecessary item fragmentation.

## Class-resource rule

A class-specific resource must remain functional in a low-enemy-count battle and in a single-boss encounter.

Bad primary resource design:

- only gain resource when an enemy dies;
- only function when many adds spawn;
- require another specific class to make the loop work.

Kill/add events may be **bonus accelerants**, not the only engine.

Example Pyromancer Ash sources could include:

- applying Burn;
- consuming/detonating Burn;
- hitting with specific fire skills;
- bonus Ash from killing a burning enemy.

## Passives and status identity

Every mature class stage should normally have an innate class passive or mechanic. Major promotions should change rules, not only numbers.

Class identity may come from:

- resource generation/spending;
- threat and interception;
- front/back-row interaction;
- speed/timeline manipulation;
- cooldown rules;
- buffs/debuffs;
- CC and boss-break contribution;
- summons;
- conditional skill transformation;
- HP-risk or defensive conversion;
- target marks and enemy-intent manipulation.

## Hidden / unusual advancements

Rookvale may use some hidden, quest, exploration, boss, faction, or mastery-based class unlocks. Hidden classes should not simply be numerically superior; they should open unusual playstyles.

Examples worth reserving for later design include:

- Rune Knight;
- Arcane Archer;
- Soul Reaper;
- Sanguine Knight;
- Dragon-themed martial path;
- monster/beast transformation path;
- relic/ancient-technology Artificer path.

## First implementation subset

The first implementation intentionally proves only a small sample of this class architecture.

### Initial four origins

1. **Armsman**
   - Knight
   - Duelist
2. **Ranger**
   - Hunter
   - Marksman
3. **Arcanist**
   - Pyromancer
   - Cryomancer
4. **Acolyte**
   - Priest
   - Oracle

This sample tests:

- front-line tanking and threat;
- precision/counter melee;
- ranged damage and marks/companions;
- elemental DoT/control;
- healing/prevention/cleanse;
- buff/debuff and intent/timeline support;
- several distinct class resources/passives;
- skill loadouts within the same ancestry;
- solo viability versus 2-4 player role synergy.

Do **not** implement the remaining class bank until this subset proves the underlying systems and presentation quality.

## Expansion rule

When a new class is proposed, it must answer all of these before implementation:

1. What fantasy does it satisfy that the roster does not already satisfy well?
2. What does the player do differently turn-to-turn?
3. What passive/resource rule makes it recognizable?
4. What party contribution does it have?
5. How does it remain viable solo?
6. Which ancestral weapons does it use, and does it genuinely need a new weapon unlock?
7. Which CC/buffs/debuffs does it interact with differently?
8. Does it remain legible in the 20-second sequential multiplayer turn model?

If these answers are weak, the concept should become a build/passive/loadout option inside an existing class rather than a new class node.
