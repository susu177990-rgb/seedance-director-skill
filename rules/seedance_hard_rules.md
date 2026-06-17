# Seedance Hard Rules

These rules are mandatory for final Seedance 2.0 prompt output.

## Time

- Total duration <= 15 seconds.
- If the user does not specify a concrete duration, default to exactly 15 seconds.
- If the user specifies a concrete duration of 15 seconds or less, use that duration.
- If the user requests more than 15 seconds for Seedance 2.0, compress the idea into 15 seconds unless the user explicitly changes platform or segment format.
- Shot count must be director-selected within 1-9 shots according to content density, attention path, rhythm, and readability.
- Each segment starts at `0秒`.
- Time ranges must be continuous.
- Use integer seconds only.
- No decimal seconds.

Correct:

```text
时间：0-2秒
时间：2-5秒
时间：5-8秒
```

Incorrect:

```text
时间：0-2.5秒
时间：2.5-5秒
```

## Segment Independence

- Every segment is a separate generation.
- Shot numbering starts from 1 in every segment.
- Do not continue numbering from a previous segment.
- Do not rely on an earlier segment unless the user provides it as context.

## Image/Reference Conversion

Final prompt must not say:

- 参考图
- 以图为参考
- 根据图
- 如图所示
- 图中
- 保持图片

Convert visual reference into text:

- scene layout
- subject appearance
- body posture
- prop design
- camera angle
- composition
- lighting
- color palette
- texture
- atmosphere

## Final Language

Do not write iteration/process phrases:

- 这次改成
- 之前的问题
- 重新设计
- 不再
- 改为
- 上一版
- 修复

Use only final visible instructions.

## Output Format

- Use Markdown code block for final prompt-writing tasks.
- Keep structure compact.
- No meaningless blank lines.
- Do not add explanations after the code block unless the user asks.
