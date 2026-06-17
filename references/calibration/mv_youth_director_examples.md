# MV Youth Director Examples — Symptom Calibration Library

This file is the symptom-to-fix lookup table for Seedance 2.0 prompts. When the user describes a poor output, find the matching symptom, then jump to the demonstrated fix pattern.

These examples are abstracted from real MV-generation cases. The pattern names (MV-A, MV-B, ...) are stable references.

---

## Pattern MV-A: "Lifestyle" Brief That Loses All Mood

### Symptom
User: "写一个 10 秒短视频，卧室，暖灯，床品，女性，眼神，柔软"

Generator output: clean stock photos. Pleasant but flat. No signature. Plays back as "no one directed this".

### Diagnosis
- Light source named but not atmospheric ("暖灯" instead of "暖黄色台灯 + 左后方主光 + 唯一光源"）
- No filter stack named
- No texture chain
- Role description thinner than 30 characters
- No `# 避免` section
- No memory-point shot — every shot is generic beauty
- No continuity lock on wardrobe / props

### Fix pattern
1. Specify exact light position + direction + as the only source
2. Name the texture chain (filter stack + grain + bloom + skin preservation)
3. Expand role to 5-layer detailed lock
4. Add `# 避免` with 5+ lines including 避免商业广告式清透 / 避免过度锐化 / 避免普通正面叙事机位
5. Pick one memory-point shot and make it the only shot that breaks the formula

### Reference: see `优秀提示词案例/抒情MV片段 真人电影感 1.txt` (the bedroom-near-lamp warm light variant) for full density.

---

## Pattern MV-B: "Casual Vlog" Brief That Becomes a Commercial

### Symptom
User: "一个女生在便利店吃关东煮，夜晚，一个人，刚分手"

Generator output: dramatic couple breakup scene, soft commercial music cue, hand-held cinematic. Doesn't match casual handheld intent.

### Diagnosis
- Format grammar not locked (vlog casual vs TVC drama conflict)
- Mood abstracts (情绪低落) instead of visible behavior
- No "this is not a commercial" negative constraint
- No scene noise floor (便利店 noise, fridge hum, fluorescent buzz)
- No micro-action beats for the eating

### Fix pattern
1. Lock format to vlog casual handheld: iPhone 原相机 / 数字锐化 / 真实荧光灯 / 不打柔光
2. Translate emotion to visible beats: 眼神短暂下落 / 手指停住不动 / 嘴里刚咬下没咽下去
3. Add `# 避免`: 不要电影感打光 / 不要背景音乐自动出现 / 不要把独处拍成偶像剧
4. Specify environmental sound floor: 便利店荧光灯嗡嗡声 / 冷柜点击声 / 远处脚步

### Reference: `references/calibration/user_case_upgrade_patterns.md` for vlog-to-cinematic diagnostic patterns.

---

## Pattern MV-C: Noodle-Western Shot Listing Looks Stiff

### Symptom
User: "三明治广告，15 秒，俯拍，分层，光线干净"

Generator output: shots look like catalog product photos. No life in the bread. No steam. No hand. No light-and-shadow play.

### Diagnosis
- Product-as-foreground but no hand relationship
- No sense of light moving through the product
- No texture chain (no grain, no bloom, no slight softness)
- No negative constraint preventing "stock product photo" appearance

### Fix pattern
1. Add hand relationship: 一只手从画面右侧伸入 / 拇指和食指夹住中层夹心 / 轻轻抬起 1 厘米
2. Specify light behavior through material: 顶部偏侧柔光 / 三明治上层面包有几粒芝麻带细高光 / 夹心蔬菜边缘溢光
3. Name texture chain with at least Pro-Mist haze + light bloom + slight softness on edges
4. Add `# 避免`: 避免产品摆拍中心居中 / 避免硬白商业补光 / 避免磨皮蜡感
5. Specify a memory-point shot: the moment bread pulls apart to show the cheese stretch, or the moment steam hits the side-light

### Reference: `examples/product_ad_brief.md` (and `优秀提示词案例/抒情MV片段 真人电影感 4.txt` for texture-chain density).

---

## Pattern MV-D: Performance Close-Up That Doesn't Land Emotion

### Symptom
User: "女生特写，眼神从镜头短暂下移再回升，结尾留住"

Generator output: a pleasant close-up of a face looking at camera. No micro-action. No specificity.

### Diagnosis
- Shot described as a state, not a beat chain
- "下移" is an emotion label, not visible behavior
- Eye contact mechanism not specified (gaze direction, pupil motion, lid droop, blink frequency)
- No relationship between action and shot tightness
- No `# 避免` containing "不要无表情直拍"

### Fix pattern
1. Write a beat chain with at least 5 beats for a 3-second close-up:
   - 视线先停在镜头中央瞳孔约 0.5 秒
   - 眼睑轻闭约 0.3 秒再打开
   - 视线下移到画面左下 / 嘴角轻微松
   - 停 0.5 秒
   - 抬回时视线走斜线而非垂直
   - 落回镜头时屏住呼吸
2. Specify眼界级别行为: 瞳孔对焦 / 卧蚕轻微收缩 / 下眼睑阴影变化
3. Specify relationship between tight framing and performance: 特写镜头里所有动作必须在毫米级别可读，眨眼、嘴角、视线、指甲、皮肤纹理都放大呈现
4. Add `# 避免`: 避免无表情直拍 / 避免一般正面大头贴 / 避免没有呼吸

### Reference: `references/calibration/bad_to_great_patterns.md` (close-up fix pattern).

---

## Pattern MV-E: Multi-Character Scene Where One Character Disappears

### Symptom
User: "朋友帮我递烤鸡翅，路边摊，8 秒"

Generator output: only the receiving hand shows up. The friend becomes a vague shape. Identity drift across shots.

### Diagnosis
- No role lock for friend
- No identification anchor (痣 / 帽子 / 衣服 / 配饰)
- No defensive line for: 朋友必须全程可见 / 必须戴红帽子 / 必须穿深色工装

### Fix pattern
1. Lock friend even if brief seems thin: 年轻人 / 中等身高 / 单眼皮 / 围着深灰围裙 / 头戴红色鸭舌帽 / 双手粗大
2. Give friend visual anchor: 红色鸭舌帽 / 围裙带子 / 手指上有一个旧疤
3. Specify friend's behavior baseline: 动作快 / 笑声大 / 直接递上 / 不等反应
4. Add anchor constraint lines: 朋友必须全程戴红色鸭舌帽，不要中途换。
5. Add `# 避免`: 朋友不要消失到画面外 / 朋友不要被前景完全遮盖 / 不要中途换衣服

### Reference: `references/calibration/strong_director_examples.md` (multi-character anchoring).

---

## Pattern MV-F: MV Beat Without Music Cue

### Symptom
User: "抒情 MV，女孩在房间里跳舞，15 秒，按歌词"

Generator output: dance rehearsals without any musical sense. Beat markers ignored.

### Diagnosis
- No beat markers specified
- No music description (BPM / style / mood)
- No relationship between shot transitions and music phrases
- No negative constraint: 不做成纯动作剪辑

### Fix pattern
1. Specify BPM if known (e.g., 80 BPM, slow ballad). If unknown: "抒情慢板，约 70-90 BPM"
2. Specify beat markers: 前奏 / 进唱第一句 / 桥段切入 / 重复乐段 / 结尾
3. Map each shot to a beat phrase: "0-3 秒 = 前奏 / 3-6 秒 = 第一句进唱 / 6-9 秒 = 副歌前置 / 9-12 秒 = 副歌 / 12-15 秒 = 重复二"
4. Specify cut type per beat phrase: 0-3 秒用静态 / 3-6 秒进入轻微飘移 / 6-9 秒换景别到特写 / 9-12 秒重新拉远
5. Specify music texture as part of texture chain

### Reference: see `优秀提示词案例/抒情MV片段 真人电影感 4.txt` (whole-segment slow-beat handling) and case 5 (multi-shot rhythm cut design).

---

## Pattern MV-G: Image-to-Video Prompt Without Translation

### Symptom
User supplies 1 reference image of a girl in a green dress. User: "让她转身走过来对我笑"

Generator output: different dress, different face, generic smile.

### Diagnosis
- Visual reference converted via forbidden phrases ("参考图" / "如图所示")
- Image content not translated into text (with which dress / which hair / which mood)
- Continuity hook only says "based on image"
- No defensive lines locking continuity

### Fix pattern
1. Read reference image first; extract descriptive layers (face / dress / hair / environment)
2. Translate image to text using role lock format
3. Add defensive line: 主体全程穿 [dress color+cut+fabric] / 发型保持 [description] / 脸部保持 [feature anchor] / 不要换装 / 不要换发型
4. Specify motion translation: 不动 → 转身 → 走近 → 笑的 beat chain
5. End prompt with: 视觉参考来自任务开始时提供的图像，最终提示词不再提及图片来源

### Reference: `rules/image_to_text_rules.md` and `references/calibration/user_case_upgrade_patterns.md` (image-to-video upgrade).

---

## Symptom Index — Quick Lookup

| If the user says... | Pattern |
|---|---|
| "出来不像我要的氛围" | MV-A |
| "像广告不像 vlog" | MV-B |
| "拍产品像淘宝详情页" | MV-C |
| "特写没情绪" | MV-D |
| "另一个角色中途没了" | MV-E |
| "口型/节奏对不上音乐" | MV-F |
| "图生视频不像原图" | MV-G |

For each pattern, the fix already lives in the referenced rules:

- MV-A: visual_texture_chain_rules + avoidance_section_rules + role_lock_detailed_rules
- MV-B: format_intelligence_rules + rules/domain_adaptation_rules (vlog section)
- MV-C: mise_en_scene_rules + visual_texture_chain_rules
- MV-D: beat_choreography_rules + performance_translation_rules
- MV-E: role_lock_detailed_rules + continuity_rules + avoidance_section_rules
- MV-F: beat_choreography_rules + format_intelligence_rules (MV section)
- MV-G: image_to_text_rules + role_lock_detailed_rules + avoidance_section_rules

When the user describes a poor output, the fix chain is: identify pattern → load referenced rules → rewrite using the pattern's fix template → ship with `# 避免` section.
