# Avoidance Section Rules

Every final Seedance 2.0 prompt MUST ship with a `# 避免` section listing 5-10 hard failures the segment must not collapse into. Without this section, even technically correct prompts drift toward the generator's default amateur look (sunny day, glossy beauty filter, dramatic couple framing, etc.).

This is the **highest-impact single edit** for prompt stability across generations.

## Why This Section Exists

When you give Seedance only a positive description, the generator balances competing goals and tends toward:

1. **Generic lighting** (always-full daylight, neutral white balance)
2. **Default camera** (eye-level, centered, medium shot)
3. **Default performance** (neutral pleasant expression, attractive-but-blank)
4. **Default styling** (modern clean commercial, no genre coat)
5. **Default prop behavior** (close-up of product/face only, no interaction)

The `# 避免` section is a low-cost, high-precision counterpunch: by naming exactly what is forbidden, you force the generator to commit to the alternatives you positively specified.

## Required Format

The `# 避免` section uses **negative-adjective lists of 5-10 items**, each formatted as a one-line directive:

```
# 避免
- 不要 X
- 避免 X
- 不出现 X
- 不要 [specific failure mode A] / 不要 [specific failure mode B]
```

Each line must specify a concrete visual, performance, or stylistic failure. Never use abstract negatives like "不要坏" or "不要不好看".

## Category Templates by Format

Generate the `# 避免` list from these templates, picking 5-10 lines that match the segment:

### Lighting & Time of Day

- 避免晴天太阳直射
- 避免出现暖黄日照斑块
- 避免窗格投下的硬边光影
- 避免夜景路灯照亮
- 避免日光穿透树叶形成的高反差光斑
- 避免霓虹色光 / 红蓝光 / 紫光
- 避免暖色补光 / 冷色补光的电影感打光

### Filter & Look

- 避免商业广告式清透
- 避免过度磨皮/蜡感
- 避免高饱和鲜亮色彩
- 避免过度锐化的现代数字感
- 避免艳丽饱和色
- 避免网红滤镜感
- 避免普通正面叙事机位
- 避免过度叙事 / 旁白感
- 避免综艺感 / 综艺打光

### Performance & Emotion

- 避免夸张大笑
- 避免歇斯底里
- 避免偶像剧式甜腻
- 避免 [specific emotional exaggeration common to this format]
- 避免突然很配合（角色必须保持设定内的抗拒或保留）
- 避免第三人称叙事口吻
- 避免 [角色名] 没戴 / 没穿 [特定锁定资产]

### Composition & Camera

- 避免远景 / 大全景 / 完整空间交代
- 避免正面直拍 / 居中对称构图
- 避免商业广告 gridded 分屏
- 避免竖屏快照构图
- 避免镜头频繁运动 / 摇移
- 避免第三人称机位感

### Spatial & Continuity

- 避免出现 X 之外的物体 / 角色
- 避免场景切换 / 切换地点
- 避免 [relationship] 出现 [forbidden interaction]

### Format-specific Blocker Lines (Highest Impact)

For specific formats, certain avoid lines are **load-bearing** and must appear even when the segment is short:

#### For all 真实 / 现实 / 纪录感 / iPhone-native briefs

- 避免电影感打光 / 摄影棚补光
- 避免专业镜头畸变校正感
- 避免慢动作 / 升格感
- 避免商业调色

#### For all 青春 / 少女 / 梦境 / MV briefs

- 避免艳丽饱和色
- 避免过度叙事
- 避免情侣暧昧感（除非 brief 明确允许）
- 避免把互动拍成短剧
- 避免偶像剧对视感

#### For all 黑白 / 高反差 / Fashion briefs

- 避免彩色滤镜
- 避免低反差灰调
- 避免胶片颗粒过重
- 避免奶油柔焦 / 少女柔光

#### For all 雨天 / 阴天 / 室内夜 briefs

- 避免晴天太阳直射
- 避免晴空蓝天
- 避免暖黄色灯光主导
- 避免强光高反差

#### For all 千嬉年 / 复古 / DV briefs

- 避免现代数字锐化感
- 避免 4K 高清感
- 避免当代手机相机完美度
- 避免饱和艳丽色彩

#### For all CG / 奇幻 / 动画 briefs

- 避免真人质感
- 避免摄影镜头畸变感
- 避免 16:9 真实空间感（上镜头限制）

## When to Skip the Section

The `# 避免` section can be skipped only when:

1. The brief is **single-character, no continuity, no visual stakes** (e.g.,"一个简单日常自拍 3 秒")
2. The format is explicitly casual / minimally directed / intentionally raw
3. The user explicitly requested "no direction beyond what's stated"

In all other cases, include 5-10 lines minimum.

## Anchor Constraint Lines

Some prompts have **specific asset locks** that need anchoring lines (also placed in or near `# 避免`). Examples:

```
# 关键统一原则 / 避免
Yingying 从头到尾都戴着蓝白针织帽，不要出现她没戴帽子的版本，不要出现她中途才给自己戴帽子的动作。
Ling 必须始终穿白色棉质睡衣，赤脚，不踩任何带跟鞋。
粉色猫咪手机必须保持识别：粉色硅胶壳 + 白色珠串挂绳 + 粉色爱心吊坠。
手机壳上的猫咪图案必须在特写镜头中清楚可见。
```

These lines turn a role lock into a **continuity Grounding Statement** — they prevent assets from drifting mid-segment. Without them, Seedance gradually forgets props and re-invents them, generating "almost the same but different" designs that destroy brand identity.

## Multi-Character Defensive Lines

For two-or-more character briefs (sub-roommate, family, couple, group), add:

```
- 两人是朋友，不是情侣。不贴脸，不恋爱式对视。
- Ling 始终保持清冷克制，不主动撒娇。
- Yingying 可以黏人主动，但不要霸凌式强势。
- 两人不能突然亲昵到失真。
```

These are relation-boundary guardrails that prevent default dramatic-couple framing.

## Continuity Anti-Drift Lines

For repeated-asset continuity (same character across multiple video segments in a project):

- [角色名] 全程穿 [locked wardrobe] / 不换风格
- [场景] 全程 [locked scene] / 不切场景
- [道具] 全程 [locked state] / 不中途变
- 镜头风格统一为 [locked filter name] / 不混风格

These lines go in the `# 整体质感` section's tail or directly in `# 避免`.

## Auto-Check Trigger

After writing the prompt, run these QC checks silently:

1. Is there a `# 避免` section? If no, fail.
2. Does it have at least 5 lines? If no, fail.
3. Does it have at least 1 lighting/time avoid line? If no, fail.
4. Does it have at least 1 filter/look avoid line? If no, fail.
5. Does it have at least 1 performance avoid line? If no, fail.
6. Does it have at least 1 continuity anchor line for any locked asset? If no, fail.
7. Does it contradict any positive spec in the body? If yes, fail.

If any fail, expand the section before shipping.
