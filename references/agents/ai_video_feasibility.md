# AI Video Feasibility Agent

## Purpose

Optimize the prompt for stable Seedance 2.0 generation.

## Risk Categories

### High Motion Risk

Examples:

- complex dancing
- multiple people crossing
- fight choreography
- fast acrobatics
- detailed hand gestures
- changing costumes mid-shot
- vehicles and characters moving together in different directions

Fix:

- split the action
- reduce simultaneous movement
- use clearer camera angle
- keep one main action per shot

### Identity Risk

Examples:

- face covered for long time
- extreme profile without identity anchors
- fast head turns
- heavy rain/smoke/hair blocking face
- multiple similar people

Fix:

- use controlled close-up
- preserve hairstyle/wardrobe identifiers
- show face before obstruction
- keep expression simple

### Prop Risk

Examples:

- tiny prop changing hands
- flexible objects
- reflective objects with faces
- food/liquid changing shape
- phones/screens/text

Fix:

- describe prop size, color, position
- reduce handoff complexity
- avoid relying on readable screen text
- use inserts for important props

### Scene Risk

Examples:

- mirrors/reflections
- glass walls
- crowds
- complex architecture
- water/fire/smoke/particles
- fantasy elements with realistic people

Fix:

- anchor space with large stable elements
- use shallow depth for secondary complexity
- keep particles atmospheric, not action-critical
- avoid exact mirror/reflection logic unless necessary

## Feasibility Rewrite Principles

- Replace abstract intention with visible behavior.
- Replace complex multi-step movement with one clear action.
- Replace simultaneous choreography with sequential beats.
- Replace unstable details with stronger spatial/prop anchors.
- Keep camera movement slow and motivated unless the user asks for high energy.

## Output Shape

The feasibility agent silently marks:

```text
Risk:
Cause:
Fix:
Final wording:
```
