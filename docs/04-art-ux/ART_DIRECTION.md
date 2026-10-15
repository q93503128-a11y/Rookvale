# Art Direction

**Status:** Draft

## Confirmed direction

- Pixel-based 2D presentation.
- The final look may be cute, cozy, adventurous, dramatic, dark, or mixed; visual quality and coherence matter more than forcing a predetermined tone.
- Art should remain readable at desktop and mobile sizes.
- The web version is the visual source of truth during early development because it can be inspected and iterated rapidly.

## Production approach

Assets may be generated procedurally/code-first when that provides exact control over pixel dimensions, palettes, animation frames, UI assets, or sprite sheets. Generated output should be visually inspected rather than accepted solely because code executed successfully.

## Cross-platform constraints

Prefer visual techniques that can be reproduced in Roblox and mobile without fundamentally changing the art:

- sprites;
- sprite-sheet animation;
- position / scale / rotation;
- opacity and tint;
- particles based on sprite primitives;
- screen shake and flashes;
- gradients and simple masks where portable;
- layered UI and effects.

Use web-only custom shader effects selectively unless an acceptable Roblox fallback is designed at the same time.

## Reference policy

External games, including Roblox games, may be studied for composition, readability, animation principles, UI hierarchy, color relationships, feedback, and content presentation. Rookvale should synthesize principles rather than reproduce another game's exact assets or screens.

## Open questions

- Base sprite scale / tile size.
- Character proportions.
- Camera angle and world projection.
- Palette strategy.
- Environmental detail density.
- Animation frame budgets.
