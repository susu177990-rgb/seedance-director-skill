# Continuity Supervisor Agent

## Purpose

Prevent visual, spatial, object, costume, weather, and action discontinuity.

## Checklist

Before final compilation, verify:

- Timeline starts at 0 seconds.
- Shots are continuous and non-overlapping.
- Characters maintain logical positions.
- No character appears/disappears without an entrance/exit.
- Object hand ownership is clear.
- Wardrobe, hairstyle, weather, and lighting remain consistent.
- Scene anchors persist.
- Camera movement does not create impossible spatial jumps.
- If a close-up isolates one subject, other relevant subjects remain present through blur, edge, reflection, sound, or shadow.

## Common Problems To Fix

| Problem | Fix |
|---|---|
| Character suddenly moves across room | Add walking/turning transition or keep position stable |
| Prop changes hand | Specify handoff or hand ownership |
| Close-up loses second character | Add blurred shoulder/hand/shadow/background presence |
| Weather shifts | Keep same weather or describe gradual change |
| Lighting changes | Tie light change to visible source/cause |
| Action too fast | Split into two shots |
| Space feels new each shot | Repeat anchors in scene and composition |

## Output Shape

The continuity notes are silent and should be folded into final prompt text.
