# Seedance Director Skill | Seedance 2.0 AI Video Prompt Director

中文 | [English](#english)

Seedance Director Skill 是一个面向 **Seedance 2.0、AI 视频生成、电影级分镜、TVC 广告、MV、短视频、vlog、纪录感影像、产品广告、角色表演和镜头调度** 的 Codex skill。

它不是普通的提示词模板，而是一个多智能体导演系统：先做导演判断，再设计观众注意力路径、场面调度、节奏停顿、角色表演、镜头参数和 Seedance 生成稳定性。

## 适合搜索的关键词

Seedance 2.0 prompt, Seedance prompt, Seedance video prompt, AI video prompt, AI video generation prompt, cinematic prompt, video prompt director, shot-by-shot prompt, 分镜提示词, AI 视频提示词, 视频生成提示词, 电影感提示词, TVC 广告提示词, MV 分镜, 产品广告提示词, 角色表演提示词, 微表情提示词, 镜头语言, 场面调度, 观众注意力控制, director prompt, cinematic storyboard prompt.

## 这个 Skill 能做什么

- 生成专业 Seedance 2.0 视频提示词。
- 把粗略想法改写成完整电影级分镜。
- 把图片、视频帧、视觉参考转换成纯文本 Seedance prompt。
- 控制 15 秒以内的整数秒时间线。
- 设计观众注意力路径：第一眼看哪里、第二眼看哪里、何时揭示、最终落在哪里。
- 做导演判断：什么该拍、什么不该拍、镜头该多近、什么时候动、什么时候停。
- 适配不同视频类型：电影、TVC、MV、短视频、vlog、纪录片、动作、CG、奇幻、美食、时尚、旅行、随手拍。
- 设计场面调度：人物、产品、镜头、光线、空间、道具、动作之间的关系。
- 把抽象情绪转成可生成的表演控制：眼神、呼吸、嘴部、下颌、手、身体重心、动作节奏、情绪掩饰和泄露。
- 设计导演性记忆点和 memory-point shot。
- 检查 Seedance 生成风险，降低画面崩坏、动作混乱、角色漂移和道具跳变。
- 用真实优秀样例库校准 MV、生活碎片、关系感和随手拍提示词，避免第一版输出只有模块、没有细节。
- 强制每个非静态分镜写出起点、触发动作、微反应、材质/空间参与和落点状态。

## 为什么不是普通提示词模板

普通 Seedance prompt 往往只描述“发生了什么”。这个 skill 会进一步判断：

- 这个视频真正值得被看的瞬间是什么？
- 观众应该先看哪里？
- 哪个信息应该先隐藏？
- 产品、人物、光线和空间如何互相发生关系？
- 镜头为什么要动？
- 哪里必须停住，让情绪、产品或画面落下来？
- 角色的情绪如何通过身体、呼吸、眼神和手部动作体现？

目标不是写“看起来高级”的空话，而是写出 **可拍、可生成、有导演判断、有视觉秩序、有表演细节** 的 Seedance 2.0 prompt。

## 支持的视频类型

- Seedance 2.0 cinematic video prompt
- AI video generation prompt
- Film / drama scene
- TVC / product advertisement
- MV / music video
- Short video / social media video
- Vlog / casual handheld video
- Documentary / realism
- Fashion / beauty video
- Food / lifestyle video
- Travel / atmosphere video
- Action / suspense scene
- Fantasy / sci-fi / CG animation
- Character performance / micro-expression prompt
- Image-to-video prompt
- Frame-to-video prompt
- Prompt audit and rewrite

## 安装

```bash
npx skills add susu177990-rgb/seedance-director-skill
```

Fork 版本：

```bash
npx skills add <YOUR_GITHUB_USERNAME>/seedance-director-skill
```

安装后重启 Codex，让新 skill 生效。

## 使用示例

### 生成 Seedance 2.0 广告片提示词

```text
用 Seedance 2.0 写一个 15 秒香水广告，清晨浴室，玻璃水雾，女性手部拿起瓶子，整体冷白高级。
```

### 生成剧情短片提示词

```text
写一个 10 秒情绪短片，一个女生深夜在便利店吃关东煮，表面平静但刚分手。
```

### 生成 vlog / 随手拍风格提示词

```text
做一个 8 秒像手机随手拍的生活片段，朋友在路边摊递给我一串刚烤好的鸡翅，真实自然，不要广告感。
```

### 审核并重写不稳定提示词

```text
帮我检查这个 Seedance 提示词为什么容易崩，并重写成稳定、专业、有导演感的版本。
```

### 图片 / 视频帧转 Seedance 提示词

```text
根据这张图写一个 Seedance 2.0 图生视频提示词，但不要在最终提示词里写“参考图”。
```

## 内部导演系统

这个 skill 会静默协调以下导演角色，最终只输出可用提示词：

1. Creative Director
2. Director Judgment
3. Attention Director
4. Format Intelligence
5. Authorial Shot Designer
6. Editor
7. Cinematographer
8. Mise-en-scene & Staging
9. Blocking & Performance Director
10. Performance Director
11. Production Designer
12. Continuity Supervisor
13. AI Video Feasibility Reviewer
14. Prompt Compiler
15. QC Supervisor

## 核心输出结构

最终提示词会包含：

- 格式与导演策略
- 核心风格
- 观众注意力路径
- 导演判断与取舍
- 导演性记忆点
- 场面调度关系
- 节奏与停顿策略
- 场景锁定
- 角色锁定
- 表演控制谱
- 道具锁定
- 分镜画面模块
- 镜头参数
- 运镜
- 构图
- 光影
- 表演重点
- 音效与台词
- 整体质感
- 核心关键词总结

## 项目结构

```text
seedance-director-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── package.json
├── references/
│   ├── agents/
│   └── calibration/
├── rules/
├── checklists/
├── templates/
└── examples/
```

## 质量标准

一个合格输出必须满足：

- 用户未指定具体时长时，默认按 15 秒创作。
- 用户指定 15 秒以内的具体时长时，按用户时长创作。
- 单个 Seedance 2.0 片段不超过 15 秒。
- 分镜数量由导演根据内容密度、注意力路径和节奏在 1-9 个内自行判断。
- 用户只给简单指令时，skill 会主动扩展成完整、合理、有记忆点的 15 秒片段。
- 所有分镜使用整数秒时间线。
- 不出现“参考图”“如图所示”“这次改成”“上一版”等过程性语言。
- 所有视觉参考都转成文本描述。
- 有明确的观众注意力路径。
- 有导演判断和取舍。
- 有至少一个记忆点镜头。
- 有场面调度关系，而不是堆视觉元素。
- 每个非静态分镜的 `画面` 段不是一行元素列表，而是完整可生成的物理瞬间。
- MV、生活碎片、关系感和随手拍类提示词会对照样例库模式，确保每镜有生活痕迹、关系机制或记忆点。
- 有节奏停顿，而不是镜头一直动。
- 人物情绪通过可见动作表现，而不是抽象形容词。
- 创意和调度必须符合 AI 视频生成稳定性。

## English

Seedance Director Skill is a Codex skill for **Seedance 2.0, AI video prompts, cinematic shot design, TVC commercials, music videos, short-form video, vlogs, documentary-style footage, product ads, character performance, micro-expressions, mise-en-scene, and director-level prompt writing**.

It is not just a prompt template. It works like a multi-agent director system: it makes director judgments first, then builds viewer attention control, staging, rhythm, pauses, performance details, camera parameters, continuity, and Seedance generation feasibility.

## Search Keywords

Seedance 2.0 prompt, Seedance prompt, Seedance video prompt, AI video prompt, AI video generation prompt, cinematic prompt, video prompt director, shot-by-shot prompt, cinematic storyboard prompt, TVC prompt, product ad prompt, music video prompt, MV prompt, vlog prompt, documentary prompt, image to video prompt, frame to video prompt, micro-expression prompt, character performance prompt, mise-en-scene prompt, attention control prompt, director prompt.

## What It Does

- Creates professional Seedance 2.0 video prompts.
- Turns rough ideas into complete cinematic shot-by-shot prompts.
- Converts image or video-frame references into text-only Seedance prompts.
- Defaults to a 15-second timeline unless the user specifies a concrete duration.
- Uses the user's concrete duration when it is 15 seconds or less.
- Keeps one Seedance 2.0 segment within 15 seconds.
- Lets the director choose 1-9 shots per segment based on content density, attention path, rhythm, and readability.
- Expands simple briefs into complete 15-second segments with setup, development, reveal, pause, and a memorable landing frame.
- Controls viewer attention: first look, second look, reveal, and landing point.
- Applies director judgment: what to shoot, what to omit, how close the camera should be, when to move, and when to stop.
- Adapts directing grammar to film, TVC, MV, short video, vlog, documentary, action, CG, fantasy, food, fashion, beauty, travel, and casual handheld footage.
- Designs mise-en-scene relationships among subject, product, camera, light, space, props, and action.
- Translates abstract emotion into visible performance controls: gaze, breath, mouth, jaw, hands, body weight, posture, rhythm, concealment, and emotional leakage.
- Adds authorial visual ideas and memory-point shots.
- Audits Seedance generation risks and rewrites unstable prompts.
- Calibrates MV, lifestyle, relationship, and casual-but-beautiful prompts against successful case-library patterns.
- Forces each non-static shot to include start state, trigger action, micro-reaction, material/space participation, and landing state.

## Why It Is Different

A normal video prompt often describes what happens. This skill asks:

- What is the exact moment worth watching?
- Where should the viewer look first?
- What should be withheld and revealed later?
- How do product, character, light, camera, and space affect one another?
- Why should the camera move?
- Where should the shot stop so emotion, product value, or visual weight can land?
- How does the character express emotion through gaze, breath, hands, posture, and timing?

The goal is not vague “cinematic” wording. The goal is a **filmable, generatable, director-level Seedance 2.0 prompt** with visual order, attention control, performance detail, and AI video stability.

## Supported Use Cases

- Seedance 2.0 cinematic video prompt
- AI video generation prompt
- Film / drama scene
- TVC / product advertisement
- Music video / MV
- Short video / social media video
- Vlog / casual handheld video
- Documentary / realism
- Fashion / beauty video
- Food / lifestyle video
- Travel / atmosphere video
- Action / suspense scene
- Fantasy / sci-fi / CG animation
- Character performance / micro-expression prompt
- Image-to-video prompt
- Frame-to-video prompt
- Prompt audit and rewrite

## Install

```bash
npx skills add susu177990-rgb/seedance-director-skill
```

For forks:

```bash
npx skills add <YOUR_GITHUB_USERNAME>/seedance-director-skill
```

Restart Codex after installation.

## Example Prompts

### Seedance 2.0 Product Ad

```text
Create a 15-second Seedance 2.0 perfume commercial in a morning bathroom with glass mist, a female hand lifting the bottle, and a cold white luxury tone.
```

### Emotional Drama

```text
Write a 10-second emotional short film prompt: a woman eats oden alone in a convenience store late at night, appearing calm after a breakup.
```

### Casual Vlog

```text
Create an 8-second casual handheld phone video: a friend hands me a freshly grilled chicken wing at a street food stall. Make it natural, not like an advertisement.
```

### Prompt Audit

```text
Audit this Seedance prompt, explain why it may collapse, and rewrite it into a stable, professional, director-level version.
```

## Internal Director System

The skill silently coordinates:

1. Creative Director
2. Director Judgment
3. Attention Director
4. Format Intelligence
5. Authorial Shot Designer
6. Editor
7. Cinematographer
8. Mise-en-scene & Staging
9. Blocking & Performance Director
10. Performance Director
11. Production Designer
12. Continuity Supervisor
13. AI Video Feasibility Reviewer
14. Prompt Compiler
15. QC Supervisor

## Output Quality Standard

A strong output should:

- Default to 15 seconds when no concrete duration is specified.
- Stay within 15 seconds for one Seedance 2.0 segment.
- Select 1-9 shots by director judgment, not by a fixed default.
- Expand simple briefs into complete, coherent 15-second segments.
- Use integer-second shot timing.
- Avoid process language such as “reference image”, “as shown”, “rewrite”, or “previous version”.
- Convert all visual references into direct text instructions.
- Define a clear viewer attention path.
- Show director judgment and omission.
- Include at least one memory-point shot.
- Use staging relationships instead of isolated visual elements.
- Include rhythm and pause, not constant motion.
- Translate character emotion into visible behavior.
- Stay feasible for AI video generation.

## License

MIT
