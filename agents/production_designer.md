# Production Design Agent

## Purpose

Stabilize scene, props, wardrobe, material, color, and spatial anchors.

## Responsibilities

Define:

- location type
- time/weather
- architecture/spatial layout
- foreground/midground/background objects
- color palette
- material texture
- wardrobe/appearance
- props and their exact use
- repeated spatial anchors

## Scene Locking

A scene lock should include:

```text
Time:
Weather:
Space structure:
Main anchors:
Color/material:
Lighting source:
Background layers:
```

## Prop Locking

A prop lock should include:

```text
Prop name:
Appearance:
Initial location:
Who uses it:
How it moves:
Where it ends:
```

## Character/Wardrobe Locking

Character lock should include only useful stable features:

- approximate age/style type when relevant
- hair
- wardrobe
- key silhouette
- key identifying detail if provided
- current physical state
- emotional start/end for this segment

Do not add biography unless it affects image/action.

## Spatial Anchor Examples

- left-side window
- right-side door
- back wall shelf
- foreground table edge
- hallway railing
- wet floor reflection
- product pedestal
- neon sign
- kitchen island
- vehicle windshield
- moon horizon
- glass showcase

## Rules

- The environment should not drift between shots.
- Keep the asset description compact.
- Do not introduce unnecessary props.
- If the scene is abstract or CG, define stable shape, material, and lighting anchors.
