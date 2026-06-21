# Final QC Checklist

Run this silently before output.

## Format

- Output is in one Markdown code block for final prompt tasks.
- Template structure is preserved.
- No extra explanation after final prompt unless requested.
- No meaningless blank lines.
- Total word count is compact.
- `# 避免` section is present with at least 5 lines (lighting + filter + performance + composition + continuity).
- `# 整体质感` first paragraph repeats the same filter stack name, light source, color palette, and dynamic range rule as `# 核心风格` (drift between the two is a fail).
- Final prompt does not contain standalone internal-planning headings such as `格式与导演策略`, `观众注意力路径`, `导演判断与取舍`, `简单指令扩展策略`, `导演性记忆点`, `场面调度关系`, or `节奏与停顿策略`.

## Seedance Rules

- Total duration <= 15 seconds.
- If the user did not specify a concrete duration, the prompt uses exactly 15 seconds.
- If the user specified a concrete duration of 15 seconds or less, the prompt uses that duration.
- Shot count is 1-9 shots unless the user explicitly changed the format.
- Shot count is selected by director judgment according to content density and rhythm, not by a fixed default.
- If the user brief was simple, the output expands it into a complete 15-second segment with meaningful progression.
- Every segment starts at 0 seconds.
- Shot numbering starts from 1.
- All shot times use integer seconds.
- No decimal seconds.
- Time ranges are continuous and non-overlapping.

## Forbidden Wording

- No "参考图".
- No "以图为参考".
- No "根据图".
- No "如图所示".
- No "这次改成".
- No "上一版".
- No "之前问题".
- No process or revision notes.
- No internal planning notes or reasoning summaries.

## Role Lock Density

- Each principal character has all five layers: face/body anchors, hair, wardrobe (3+ items + color + fabric), body behavior baseline, relationship anchor.
- Role description is at least 100 characters per character; thin 1-2 line locks are rewritten.
- At least one character carries a unique identification mark (痣 / 疤 / 单品特征 / 配饰).
- Multi-character prompts include a "双人关系限制" or equivalent paragraph listing forbidden interactions.
- If the user supplied character images at task start, the role block uses a source-free identity lock such as "身份锚点：必须保持上述脸型、五官结构、发型和体态一致。"; it does not mention reference images, image sources, or "如图所示".
- Locked assets have at least one `#关键统一原则` (or `#避免` line) anchoring them across shots: [角色] 全程穿 X / 全程戴 Y / 不中途换。

## Texture Chain Density

- `# 核心风格` names the texture chain in this exact order: format name + palette (4+ named colors) + filter stack + light source + atmospheric state + dynamic range rule + grain/bloom/runner artifact trio + skin preservation rule + deny list.
- `# 整体质感` repeats the same filter stack name, same palette, same light source, and same dynamic range rule as `# 核心风格` — they are visible in the same wording.
- Skin preservation rule is present: 保留真实肤色 / 不磨皮 / 不出现蜡感.
- A negative deny list appears somewhere in `#核心风格` or `#整体质感` or `#避免`.

## Beat Chain Density

- Each non-static shot includes a beat chain in `### 画面` with approximately 2 beats per second of shot duration.
- A 3-second shot has roughly 6 beats.
- Beats are separated by 顿号 / 逗号 / 句号 with `……` for holds.
- The last beat of every chain is a state, not a continued action (e.g., "肩膀保持原位" not "肩膀继续下垂").
- Multi-character shots alternate beats between characters (no same character with 2+ consecutive beats).
- Static shots explicitly state `静止` rather than implied absence of motion.

## Cinematic Quality

- Every shot has shot size, camera, composition, light, action, performance, sound, dialogue, and time.
- Every shot has attention control, staging, and rhythm/pause logic.
- Each shot has a clear function.
- No shot exists only to fill time.
- Composition is not generic unless intentional.
- Lighting is physically described.
- Emotion is visible through behavior.
- The prompt contains one authorial visual idea expressed through concrete image/action design.
- At least one shot is a memory-point shot, marked or made unmistakable inside the shot block.
- Shot hierarchy is not flat; important shots have clear priority.
- The strongest visual idea is specific to this brief, not reusable generic "cinematic" coverage.

## Director Judgment

- The format grammar matches the requested form: film, TVC, MV, short video, vlog, documentary, product ad, action, CG, fantasy, food, fashion, beauty, travel, or casual handheld.
- The prompt makes clear what should be filmed through shot selection and what should be omitted through `# 避免`; it does not use a separate judgment essay.
- Camera distance matches the information need.
- Camera movement has a purpose: reveal, follow, transfer attention, compress distance, increase pressure, or show material change.
- Stillness or pause is used where inspection, emotion, product value, or realism needs weight.

## Attention Control

- The viewer's first look, second look, reveal point, and final landing point are clear through shot-level attention controls, not a standalone attention-path module.
- No shot asks every detail to compete equally.
- The product, face, action, or emotional clue is dominant at the right moment.
- Foreground, light, focus, motion, gaze, color, sound, line, scale, or negative space guides attention.

## Staging

- People, product, camera, light, space, props, and action relate to one another inside `### 画面`, `### 构图`, `### 场面调度`, and `### 光影`.
- Foreground, midground, and background each have a role.
- Product or prop reveals have a mechanism, not just centered display.
- Character blocking shows relationship, pressure, emotion, or status.
- Casual, vlog, or documentary formats are not over-directed unless requested.

## Performance Quality

- Important emotions are translated into visible acting controls.
- Important character beats include shot-size-appropriate gaze, mouth/jaw, breath, hands, body weight, posture, movement rhythm, concealment, or emotional leakage.
- Personality appears through action choices, not labels or biography.
- Broad adjectives such as sad, nervous, mysterious, elegant, angry, lonely, or premium are converted into precise visual behavior or visual mechanism.
- Micro-expression details are not assigned to shots where they would be invisible.

## Continuity

- Characters do not teleport.
- Props do not teleport.
- Entrances/exits are clear.
- Scene anchors persist.
- Weather and lighting are stable.
- Close-ups preserve spatial context when needed.

## Feasibility

- No overloaded 1-second shots.
- No excessive simultaneous motion.
- No unnecessary face obstruction.
- Prop handling is explicit.
- Camera movement is stable enough for generation.
- Creative attention/staging choices remain physically clear and generatable.
