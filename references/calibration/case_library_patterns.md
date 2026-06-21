# Case Library Calibration Patterns

This file summarizes the usable directing patterns from `examples/case_library/`. Load it when a prompt risks becoming thin, generic, or first-pass ordinary, especially for MV, youth film, lifestyle, relationship, dream, casual short video, and character-atmosphere briefs.

The case library's strongest lesson: good prompts are not merely more cinematic. They give each shot enough physical, relational, and material detail that a generator can stage a specific moment.

## Current Case Library

- `优秀-抒情MV片段1-戴帽子打闹.txt` — relationship tug, prop continuity, refusal/softening beats
- `优秀-抒情MV片段2-同住乌龙碎片.txt` — used-space montage, small mess, room becoming lived-in
- `优秀-抒情MV片段3-天台电话告白.txt` — weather, prop, body collapse, suppressed emotion
- `优秀-抒情MV片段4-发光鹿与森林碎片.txt` — dream logic, occlusion, partial body, natural-space scale
- `优秀-抒情MV片段5-暴烈奔跑与梦核片段.txt` — high-contrast rhythm cuts, extreme angle, hard style shifts
- `优秀-抒情MV片段6-猫陪伴日常片段.txt` — three-participant staging, animal as emotional buffer
- `不佳-短视频美女随拍-对比样例.txt` — modules complete but shot density too thin
- `不佳-短视频美女随拍2-对比样例.txt` — atmosphere and styling present but role/action/detail still underspecified

## Good vs Thin

Thin first-pass prompts usually have:

- correct sections but short `### 画面` blocks
- role lock thinner than the action needs
- props named but not physically used
- mood stated instead of staged
- camera grammar described, but the frame lacks a concrete event
- no negative guardrail against stock beauty, generic vlog, or ordinary centered coverage

Good case-library prompts usually have:

- one complete micro-event per shot
- prop continuity and object logic repeated when important
- body reactions specific enough to generate: shoulder shrink, hand half-block, gaze down then back, breath stop, step back
- space participates: fish tank reflection, floor mess, doorway pressure, window light, water reflection, cat as middle point
- sound is tied to the visible material: paper, fabric, water, fur, footsteps, phone, rain, fan, shutter
- the `# 避免` section names the exact default failure mode

## Pattern 1 — Prop Tug / Relationship Refusal

Source: `优秀-抒情MV片段1-戴帽子打闹.txt`

Use when: two people, playful conflict, repeated object, resistance, reluctant acceptance.

Recipe:

1. Lock the prop's identity and ownership before shots begin.
2. Make the prop visible in every important shot.
3. Each shot should include: initiator action -> receiver refusal -> initiator persistence -> relation landing.
4. Receiver's refusal must be visible but not exaggerated: shoulder shrink, head turn, hand half-block, mouth pressed, gaze away.
5. Add a continuity defense line: who wears/holds which object, and what must never change.

Prompt smell to reject:

```text
她拿帽子给对方戴，对方害羞拒绝。
```

Rewrite direction:

```text
她已经戴着自己的帽子，从对方侧后方探进来，双手举着另一顶帽子往头顶比划；对方肩膀先缩、头偏开、手抬到帽檐前但不真正推开，帽子边缘快碰到头发时停住。
```

## Pattern 2 — Used-Space Montage

Source: `优秀-抒情MV片段2-同住乌龙碎片.txt`

Use when: cohabitation, daily life, room atmosphere, cute chaos, casual memory.

Recipe:

1. Pick 5-8 small actions rather than one summary event.
2. Each shot must show the room being used: object slips, book moves, glass passes, fish tank reflects, floor receives footsteps.
3. The other character can be partial, blurred, passing, or noticing from a distance.
4. Avoid sitcom action. The change should be light, small, and visually pretty.
5. Use sound to prove life: paper, fabric, candy wrapper, barefoot wood floor, water pump.

Prompt smell to reject:

```text
房间变得更有生活气息，两人相处自然。
```

Rewrite direction:

```text
她抱着抱枕从沙发边经过，抱枕边缘扫到书堆，几本书滑出一点；她停住低头看，像做错事一样顿半拍，另一人在远处虚焦里抬眼看她。
```

## Pattern 3 — Weather Body Collapse

Source: `优秀-抒情MV片段3-天台电话告白.txt`

Use when: emotional scene, phone call, rain, rejection, isolation, alone in space.

Recipe:

1. Weather must affect body, wardrobe, floor, prop, sound, and reflection.
2. Phone/prop must have exact identity and movement path.
3. Emotion must drop through a body sequence: face empties -> hand lowers -> prop hangs -> knees fold -> head lowers.
4. Include an environmental substitute for emotion: rain hits puddle, reflection breaks, wet fabric clings, far city hum.
5. Keep performance controlled; no melodramatic crying unless requested.

Prompt smell to reject:

```text
她接到电话后很难过，在雨中哭。
```

Rewrite direction:

```text
挂断提示音后，她眼神先空掉，手机从耳边放下，白色珠串挂绳顺着手腕垂落；身体像被抽掉力气一样抱膝缩到台阶右侧，湿发贴在脸侧，哭声压低在雨声里。
```

## Pattern 4 — Dream Through Surface

Source: `优秀-抒情MV片段4-发光鹿与森林碎片.txt`

Use when: dream, fantasy, nature, symbolic object, surreal but not overloaded.

Recipe:

1. Use one wonder object only.
2. Reveal through a surface: blind slats, grass, water reflection, branches, wet lens, far silhouette.
3. Avoid full explanatory close-ups. Let partial body and scale make the image strange.
4. Give natural elements real behavior: grass sweeps, water breaks reflection, branch cuts frame, white light blooms.
5. Keep the wonder distant or partially obscured until the memory shot.

Prompt smell to reject:

```text
森林里有一只发光鹿，画面梦幻。
```

Rewrite direction:

```text
镜头贴在百叶窗内侧，只出现一只手轻轻拨开叶片；窗外野草和河岸被叶片横向切开，远处一只纯白过曝的鹿站着，细节被光吞掉，只剩头颈轮廓和边缘溢光。
```

## Pattern 5 — Hard Rhythm Contrast

Source: `优秀-抒情MV片段5-暴烈奔跑与梦核片段.txt`

Use when: fast MV cuts, contrast montage, emotional rupture, dreamcore, harsh digital texture.

Recipe:

1. Assign each shot a strong visual grammar: flash, low angle, hard sunlight, top-down still, dead-black room, high-speed run.
2. Let rhythm come from contrast, not continuous explanation.
3. Every shot needs one dominant visual mechanism: hard shadow, fan, sink water, photo stack, staircase diagonal, covered heads.
4. Style can shift only if each shift is deliberate and named.
5. Sound cuts matter: beat enters, drops out, low-pass, fan hum, water noise, silence.

Prompt smell to reject:

```text
情绪混乱，镜头快速切换，有梦核感。
```

Rewrite direction:

```text
强制闪光灯直打，两个主体并排坐在姜黄色切斯特菲尔德沙发上，头部被白色布袋完全包住；皮革纹理、布料褶皱和墙纸被硬光切得过分清楚，身体微微前倾却没有交流。
```

## Pattern 6 — Third-Life Anchor

Source: `优秀-抒情MV片段6-猫陪伴日常片段.txt`

Use when: animal, product, object, lamp, or room detail should become more than decoration.

Recipe:

1. Lock the third element's visual identity.
2. Build triangle staging: person-object-person, person-animal-room, product-hand-light.
3. The third element must react or change slightly: paw moves, ear twitches, label catches light, lamp reflection shifts.
4. Human relationship is expressed through the third element, not by posing.
5. End with the third element carrying the aftertaste if useful.

Prompt smell to reject:

```text
两个人和猫一起生活，很温柔。
```

Rewrite direction:

```text
猫坐在床前中景，伸出一只爪子与 Ling 指尖轻轻搭住；Ling 趴在床上只勾一下猫爪，Yingying 在右侧前倾看着这一下笑出来，三者形成稳定三角关系。
```

## Calibration Procedure

When writing a prompt:

1. Identify the closest case-library pattern.
2. Borrow the pattern's grammar, not its literal subject.
3. Before final output, compare the weakest shot against the matching pattern.
4. If the weakest shot has no micro-event, material participation, or landing frame, rewrite it.
5. Add `# 避免` lines naming the default failure from that pattern.

## Minimum Density Reminder

For a prompt intended to be used directly for generation, do not ship a shot where the `### 画面` block is only a summary sentence. A usable generation prompt needs enough detail that one shot can be imagined as a finished clip without reading the rest of the document.
