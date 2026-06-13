# Image To Text Rules

Use when the user provides images or video frames.

## Goal

Do not refer to the image as an image in final prompt. Extract all useful visual information and rewrite it as direct text instructions.

## Extract

- subject count
- identity/appearance if relevant
- posture
- gesture
- facial direction
- wardrobe
- scene structure
- background anchors
- props
- camera height
- camera distance
- focal impression
- composition
- foreground/midground/background
- light direction
- color palette
- material/texture
- atmosphere
- motion possibility

## Do Not Copy

- accidental artifacts
- low-quality image flaws unless wanted
- irrelevant background clutter
- exact facial identity of a real person unless allowed by user-provided context and task requirements
- unsafe or disallowed detail

## Convert Language

Forbidden:

```text
参考图里的走廊
```

Use:

```text
阴天冷光下的老楼走廊，右侧为浅色墙面与关闭的房门，左侧为栏杆和灰蓝天空，地面略有潮湿反光。
```
