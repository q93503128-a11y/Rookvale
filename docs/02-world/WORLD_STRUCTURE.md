# World Structure

**Status:** Draft

## Confirmed direction

Rookvale uses a broad handcrafted open world with a recognizable starting settlement and multiple distinct spaces, regions, enemies, and activities.

## World goals

- Strong regional identity.
- Exploration routes rather than a single corridor.
- Towns and safe locations that feel useful and memorable.
- Dungeons and special spaces with their own gameplay purpose.
- Enemies appropriate to local ecology, culture, faction, or magical conditions.
- Content density high enough that travel is interesting without turning the map into icon clutter.

## Candidate hierarchy

```text
World
  -> Region
       -> Settlement / hub
       -> Field zones
       -> Dungeons
       -> Landmarks
       -> Hidden / special spaces
       -> Dynamic or scheduled content
```

This hierarchy is a planning model, not a technical map-loading decision yet.

## Starting-area requirements

The opening area should demonstrate the game's identity quickly:

- a visually distinct starting town;
- nearby low-risk exploration;
- several enemy behaviors rather than reskins;
- at least one reason to party up;
- a dungeon or equivalent focused activity;
- visible hints of higher-level places that cannot yet be fully handled;
- enough optional discovery that the route does not feel scripted.

## Open questions

- Seamless versus region-transition world.
- Day/night and weather.
- Dynamic events.
- World scaling versus fixed danger regions.
- Fast travel rules.
- Resource gathering and crafting presence.
- How much environmental interaction exists outside combat.
