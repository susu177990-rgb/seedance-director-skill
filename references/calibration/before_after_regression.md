# Before-After Regression Test

This is the live record of regression tests run against the Seedance director skill after each structural upgrade. The goal is not to "pass" demos; the goal is **to measure density, specificity, and visual-concept coverage** in the prompt body, then write any missed dimension back into the skill's rules.

For each regression run, three artifacts are kept:

1. The user brief (clean, original).
2. The old prompt (skill output before the upgrade).
3. The new prompt (skill output after the upgrade, applying the new rules).
4. The qualitative diff and the rule it implies.

---

## Run 2026-06-17 / Round 1 — 短视频美女随拍

### Brief
```
9:16 短视频，10 秒，卧室，床头灯，玩偶挡镜，暖灯氛围，眼部特写，近距离
```

### Reason for the run
User reported that the skill's first-pass output felt "thin", "every shot looks the same", "feels like stock beauty footage", and "didn't capture any mood". The user had previously worked from the skill's first pass without iteration. They saved the prompt as `/Users/griffith/Desktop/效果不好的案例/短视频美女随拍.txt`. Reformulation of the same brief under the upgraded skill lives in `references/calibration/before_after_regression_v2.md`.

### Old Prompt (excerpted key fields)

| Field | Old value | Character count |
|---|---|---|
| Role A description | "年轻女性，长直黑发，干净淡妆，穿奶油白蕾丝边居家吊带套装" | 28 字 |
| Performance谱 | "嘴部自然闭合，下颌放松，呼吸慢，右手指尖轻压玩偶绒面，肩颈不紧绷" | 32 字 |
| 核心风格 | "暖色床头灯、奶油白布料、柔软床品、浅粉色毛绒玩偶、低照度手机质感" | 32 字 |
| Texture chain | absent (only lighting + color 名, no filter stack, no atmosphere, no skin rule, no deny list) | 0 字 |
| Beat chain per shot | absent (single verb-phrase actions: "手指触到绒面") | absent |
| `# 避免` section | does not exist | 0 行 |
| Locked assets | 0 anchor lines | 0 行 |
| Continuity lock | 角色 + 玩偶有，但无显式 "全程不换" 约束 | 无 |

### New Prompt (Upgrade v2)

| Field | New value | Character count |
|---|---|---|
| Role A description | 5-layer lock: 脸型/颊/下颌 + 眼型/瞳孔/卧蚕 + 鼻/唇/唇色 + 皮肤纹理/面色毛孔 + 身形 + 发型长度色刘海 + 服装 3+ 项 + 本段状态 + 视觉识别锚点痣位 | ~210 字 |
| 表演控制谱 | 内在 + 外在掩饰 + 情绪泄露点 + 眼神目标 + 嘴部/下颌 + 呼吸 + 手部 + 身体重心 + 动作速度 + 起点 + 终点 | ~280 字 |
| 核心风格 | 风格名 + iPhone 原相机 2x stack + 色板 6 色 + 光源方向距离 + 反差规则 + artifact trio + 皮肤保留 + 多条 deny | ~330 字 |
| Texture chain | 显式 6 层：色板 / 光源 / 反差 / artifact / 镜头参数 / 皮肤保留 / deny list | 6 层 |
| Beat chain per shot | 每镜 #画面 写成 6-8 个节拍，含「……」停顿符号，动作链终止于状态而非动词 | 每镜 30-50 字 |
| `# 避免` section | 7 行覆盖光线 / 滤镜 / 皮肤 / 道具一致性 / 表演尺度 / 服装一致性 / 过程语言 | 7 行 |
| 关键统一原则 / 锁资产 | 4 行：服装 / 玩偶 / 灯光位置 / 镜头比例 | 4 行 |
| Continuity lock | 显式 "全程不换" 约束 + 角色识别锚点痣 | ✅ |

### Dimension Coverage Diff

| Dimension | Old coverage | New coverage |
|---|---|---|
| Role lock 五层密度 | 1/5 (only identity 名) | 5/5 |
| 纹理链 6 层 | 1/6 (only palette hint) | 6/6 |
| 节拍链密度 | 0 (one-verb blob) | 4 镜 × 6-8 节拍 |
| `# 避免` 段 | 0 行 | 7 行 |
| 锁定资产连续性锚点 | 0 行关键统一 | 4 行 |
| 表演情绪 → 节拍翻译 | 0 (性能谱只有抽象描述) | 12 项具体动作节拍 |
| 反差规则 | absent | mid key 偏暗 + 暗部抬灰明确 |
| 皮肤保留规则 | absent | 保留真实肤色毛孔和细小色点 + 不磨皮 |
| Filter stack | absent (无 Pro-Mist / DV / Native Camera stack 名) | iPhone 原相机 50mm 2x 长焦调用 stack |
| Memory-point shot | 一句模糊描述 | 4 个机制点（半遮 + 不否认 + 不动 + 高光） |
| 跨段风格一致性自检 | absent | `#整体质感` 重述 `#核心风格` 同款 stack + 色板 + 光源 + 反差 |

### Qualitative Diff (drawn from user perception)

The old prompt read to the generator as:
- "young woman in bedroom, warm light, soft bed, pink plush doll, calm mood, eye close-up, low light, phone-camera quality."

The new prompt reads to the generator as:
- "竖屏夜间 iPhone 原相机 2x 长焦短视频，床头灯单主光竖向构图，浅粉色爆米绒面毛绒玩偶伪装道具，9-10 秒内分四段：玩偶前-指头探入-玩偶遮脸-眼神停住；色板锁到 6 色，反差规则 mid key 偏暗 + 暗部抬灰；每镜动作用节拍链写完；锁定服装/玩偶/灯光四个一致性锚点；皮肤保留真实；显式禁止晴天、商业广告、过度锐化、角色换装；memory-point 是分镜 3 玩偶半遮后眼睛独自成为画面唯一清晰人物元素。"

Density is roughly 4-5x in the new prompt at the same target time.

### Expected Outcome
The new prompt should produce a generation that:
- Has noticeably consistent warm color across all 4 shots (no daylight drift)
- Has a defined filter stack visible as soft bloom on the plush edge
- Plays dress- and prop-consistent across shots (no wardrobe change, no plush substitution)
- Lands on the memory-point moment (半遮脸 + 眼神回来) with the eye stably inside the bloom of the table lamp
- Has a visible texture of soft cool bleed in shadows, not flat digital darkness
- Is monotone 9:16 cropped tight to the face and doll, not pulled out

If any of these fail, the rule that failed will be patched in the next iteration.

---

## Run 2026-06-17 / Round 1 takeaways — rules to add or strengthen

After this run, the existing rules covered most of the dimensions but with the following gaps that should be filled:

| Gap | Resolution |
|---|---|
| 模板没有显式 `[REQUIRED]` 标 | templates/seedance_2_prompt_template.md 改成 `[REQUIRED]` 标记 |
| `# 避免` 段没有强制 | 新增 rules/avoidance_section_rules.md 给分类模板，并把 `# 避免` 加进 QC fail list |
| 节拍链没有强制格式 | 新增 rules/beat_choreography_rules.md 给 5-beat 模板和标点节奏准则 |
| 纹理链没有强制格式 | 新增 rules/visual_texture_chain_rules.md 给 6 层格式，并把 `# 整体质感` 与 `# 核心风格` 一致性写入 QC |
| 角色锁没有 5 层格式 | 新增 rules/role_lock_detailed_rules.md 给 5 层顺序和最低字数 |
| calibration 没有症状 → 修复索引 | 新增 references/calibration/mv_youth_director_examples.md 给 MV-A 到 MV-G 模式诊断表 |
| 回归测试本身没有正式落档 | 新增本文件 references/calibration/before_after_regression.md |

All gaps above have been resolved in this same upgrade cycle.

---

## How to Run the Next Regression

1. Pick a user-reported failure case from `/Users/griffith/Desktop/效果不好的案例/` (or any new failure the user ships).
2. Capture the user brief verbatim into this file.
3. Copy the old prompt into this file (excerpted key fields).
4. Re-run the **same brief** against the upgraded skill; capture the new prompt.
5. Score both on:
   - Role lock density (5 layers?)
   - Texture chain density (6 layers?)
   - Beat chain density (~2 beats/sec?)
   - `#避免` presence (≥5 lines?)
   - Continuity anchor lines
   - 整体质感 vs 核心风格 consistency
6. Write the dimension diff into this file.
7. If any dimension regresses or any new failure appears, patch the relevant rule and rerun.

This file is the institutional memory of "what kinds of failures this skill still produces" — keep it open, append runs, never delete a failed case.
