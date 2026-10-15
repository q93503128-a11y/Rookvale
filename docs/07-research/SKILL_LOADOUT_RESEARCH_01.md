# Skill Loadout Research 01

**Status:** Research note — design discussion, not final slot-count lock.

## Rookvale constraint that changes the problem

Rookvale is not a collectible-party RPG. A human player develops one persistent avatar and joins other human avatars for multiplayer parties. This means combat variety cannot rely on swapping between a roster of collected characters. The player's single character must have enough learned skills and build choices to remain tactically expressive over a long RPG progression.

## External references

### Hero of Aethric / Orna

Useful because the game is structurally close to Rookvale's persistent-avatar RPG model.

Observed reference points:

- classes learn multiple skills over progression;
- classes have a limited number of combat skill slots rather than placing every learned skill in combat at once;
- the slot count grows across progression/classes in existing Orna/Aethric references;
- examples found in current reference material range from very small early-game loadouts to substantially larger late-game skill bars.

Design lesson for Rookvale:

- learning more skills than can be equipped creates build choices within the same class;
- however, Rookvale should not blindly copy very large late-game slot counts because its combat UI must remain readable on web, mobile, and Roblox and turns have a 20-second ceiling.

### Guild Wars 2

Guild Wars 2 gives one persistent character a ten-skill combat bar. Five slots are largely determined by equipped weapons, while the remaining slots include healing, utility and elite choices. It also exposes profession-specific mechanics outside the normal ten-skill bar.

Design lesson for Rookvale:

- separate ordinary equipped skills from universal/class-mechanic controls when useful;
- equipment can influence skill identity without consuming all build freedom;
- profession/class mechanics do not necessarily need to occupy ordinary skill slots.

### Elder Scrolls Online

ESO is a useful limited-action-bar reference because characters can learn far more abilities than they can place on the active bar. Its compact bar creates meaningful build selection, although community discussion also shows the danger of making the bar so small that single-character roles feel deprived of necessary utility.

Design lesson for Rookvale:

- scarcity is useful only until it starts removing the tactical breadth expected from one persistent RPG character;
- healer/support/tank builds are especially sensitive to overly small active bars because they need defensive, offensive and utility tools at the same time.

## Rookvale candidate model

The current strongest candidate is:

- a large learned skill library;
- a smaller equipped combat loadout;
- no random draw mechanic;
- one normal action per natural turn;
- turn-based cooldowns;
- class-specific combat resources in addition to cooldowns where appropriate;
- universal commands outside ordinary skill slots where appropriate;
- optional class mechanic/resource controls outside ordinary skill slots.

### Candidate slot count for prototype

**8 equipped active skills at mature progression** is a strong first prototype target, not a final lock.

Why 8:

- 5–6 may be too restrictive for a game where the player controls only one long-term character and may need damage, defense, support, setup and solo tools;
- 8 still forces real loadout decisions;
- 8 is small enough to display cleanly on mobile/web/Roblox with paging or a two-row layout if needed;
- one action per turn keeps eight available choices manageable under the 20-second limit;
- universal actions such as Defend and system item access can sit outside those eight slots.

Possible progression test:

- early game: 4 equipped skills;
- early-mid: 6;
- mature build: 8;

Do not add slots indefinitely merely as a numerical progression reward. The mature maximum should stay stable once the intended tactical breadth is reached.

## Cooldown + resource recommendation

Rookvale can use both cooldowns and resources, but should avoid making every skill pay both costs by default.

Recommended categories:

1. **Basic / setup skill** — no or very short cooldown, generates or prepares class resource.
2. **Normal skill** — primarily controlled by cooldown.
3. **Resource spender** — primarily controlled by class resource, possibly with a modest cooldown.
4. **Signature / major skill** — may require both meaningful resource and a longer cooldown.

This keeps the two systems from feeling like duplicate restrictions.

## Mana recommendation

Do not give universal MP to every class solely because the genre traditionally does so.

Mana can still exist as a real class resource for caster branches. Other classes may use resources such as Rage, Resolve, Grace, Momentum or Focus. A resource is valuable only if its generation and spending pattern reinforces the class's behavior.

Examples:

- tank Resolve from successfully drawing/intercepting dangerous attacks;
- healer Grace from effective healing, prevention or cleansing rather than overhealing spam;
- martial Rage from attacking/taking meaningful pressure;
- rogue Momentum from successful sequencing, crits, evasion or marked-target play;
- mage Mana as a finite or semi-finite casting budget.

## Important balance constraint

Speed already increases natural turn frequency and therefore accelerates turn-based cooldown recovery. Resource generation should not universally grant a fixed amount every natural turn, or Speed risks multiplying action frequency, cooldown cycling and resource generation simultaneously.

Prefer class resources generated by meaningful actions/events, with explicit exceptions where passive per-turn generation is part of a class's identity.

## Open decisions

- final mature active-skill slot count after prototype testing;
- whether signature/ultimate skills use a dedicated slot;
- whether passive skills use separate slots or talent-tree choices;
- number of saved loadout presets;
- where loadouts may be changed: any out-of-combat location, towns/rest points, or activity-specific preparation screens;
- how much the equipped weapon changes available skills;
- whether advanced class branches inherit all earlier skills, a subset, or cross-class unlocks;
- how PvP handles loadout information and counter-picking.

## Sources consulted

- Orna / Hero of Aethric class references and codex pages for learned skills and class skill-slot progression.
- Guild Wars 2 official new-player guide and Guild Wars 2 Wiki skill-bar documentation for the ten-slot bar and profession-mechanic separation.
- Elder Scrolls Online public developer/community material on its limited ability-bar philosophy and long-term skill learning.
