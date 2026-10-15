# Turn-Based Combat

**Status:** Open — intentionally not locked yet

## Confirmed requirement

Combat is turn-based and must support both solo characters and multiplayer parties.

## Design goals

- Faster and more readable than a menu-heavy traditional JRPG battle.
- Deep enough that class roles and party composition matter.
- Support healing and support as genuinely useful play styles.
- Reward tactical decisions rather than pure stat checks.
- Make enemies mechanically distinct, not just differently sized health bars.
- Remain understandable on desktop, mobile, and Roblox UI layouts.
- Leave room for strong animation, impact, and boss presentation despite being turn-based.

## Decisions we need to make together

### Turn structure

Candidate families to investigate:

- strict party turn / enemy turn;
- speed-based timeline;
- visible future initiative order;
- simultaneous planning followed by resolution;
- action-point system;
- hybrid system with reactions, interrupts, or timed elements.

### Multiplayer decision flow

Questions:

- Do party members choose actions simultaneously?
- Is there a planning timer?
- Can players revise choices before resolution?
- How are disconnected or idle players handled?
- Can allies react to each other's actions within the same round?

### Tactical identity

Rookvale still needs one or more mechanics that make its combat recognizable. Candidates should be researched from multiple external games before locking this section.

## Avoid by default

- basic attack spam as the optimal default;
- healer gameplay that is only repeated HP restoration;
- tanks that work only through inflated defense numbers;
- enemies differentiated only by elemental color;
- excessive animation time that makes ordinary encounters tedious.
