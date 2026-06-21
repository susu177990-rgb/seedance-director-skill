# Seedance 2.0 Final Prompt Template

Use this template for every final prompt-writing task. Modules inside the Markdown code block are the only user-facing final prompt structure. Modules marked **[REQUIRED]** inside the code block must ship. Modules marked **[OPTIONAL]** are conditional and only used when the brief needs them.

Before compiling the final code block, silently complete an internal director brief with: format grammar, viewer attention path, director judgment and omissions, simple-brief expansion strategy if needed, authorial visual idea, memory-point shot, mise-en-scene relationship map, and rhythm/pause plan. Do not output these as standalone analysis modules. Convert them into concrete shot choices: shot count, shot function, `### 画面`, `### 注意力控制`, `### 运镜`, `### 构图`, `### 场面调度`, `### 表演重点`, `### 节奏停顿`, `# 整体质感`, and `# 避免`.

**Mandatory checks before shipping:**

1. Every user-facing `[REQUIRED]` module inside the code block is present and not stubbed.
2. `# 避免` is present with **at least 5 lines** spanning lighting, filter, performance, and continuity.
3. `# 整体质感` repeats the **same texture chain wording** as `# 核心风格` (filter stack + light source + color palette + dynamic range). Drift is a fail.
4. Each shot's `### 画面` block contains a **beat chain** matching `rules/beat_choreography_rules.md`.
5. Each principal character lock has the **face / hair / wardrobe / behavior / relationship** layers as defined in `rules/role_lock_detailed_rules.md`.
6. Each non-static shot's `### 画面` block meets `rules/detail_density_rules.md`: start state + trigger action + micro-reaction + material/space participation + landing state. Thin object-list shots must be rewritten.
7. The final code block does not contain standalone planning/process headings such as `格式与导演策略`, `观众注意力路径`, `导演判断与取舍`, `简单指令扩展策略`, `导演性记忆点`, `场面调度关系`, or `节奏与停顿策略`.

```markdown
片段名：[片段名称]
时长：[用户未指定具体时长时固定写15秒；用户指定15秒以内具体时长时写用户时长]
比例：[16:9 / 9:16 / 1:1 / 2.39:1 等]
类型：[选择3-10个关键词：真人电影感 / 产品广告 / 青春MV / 动作片段 / CG动画 / 奇幻短片 / 生活方式广告 等]
分镜数量：[1-9个分镜；只写最终数量，不写判断过程]

## 核心风格  [REQUIRED]
[一段完整的视觉锚点陈述。必须包含:
- 风格名 + 流派标签（例:2000年代东亚青春MV / 千禧年少女影像 / iPhone 原生 vlog）
- 滤镜栈名称（旧 DV + 16mm 胶片混合 / Pro-Mist 雾化 / Stock Anamorphic / iPhone Native / Modern Cinema Sharp 等)
- 色板名 + 4+ 种具体颜色（例:奶白灰 + 淡青 + 灰蓝 + 柔粉）
- 光源类型 + 方向 + 大气状态（例:厚云阴天漫射 + 经白纱窗帘过滤 + 闷白低对比)
- 反差规则（high key / mid key / low key / 暗部抬灰 / 暗部死黑)
- 颗粒 + bloom + 跑焦等artifact选择
- 皮肤保留规则（保留真实肤色 + 毛孔 + 细小色点 / 不磨皮)
]
## 场景锁定  [REQUIRED — 若场景不重要可压缩到 2-3 行]
[固定场景。明确时间、地点、天气、空间结构、主要环境元素、色彩、光线与必须保留的空间锚点。]
## 角色锁定  [REQUIRED — 含人物、拟人主体、角色、动物或需要跨镜头身份一致的主体时；纯产品/空间片可省略]
### @角色A / 主体A  [REQUIRED]
[必须按以下顺序书写，遵循 rules/role_lock_detailed_rules.md 的五层密度:

1. **脸与身体锚点**：脸型 + 颊 + 下颌 + 下巴 + 眼型 + 瞳孔色 + 卧蚕 + 鼻型 + 唇型 + 唇色 + 眉形 + 皮肤纹理 + 关键痣/斑 + 身形
2. **发型**：长度 + 色 + 刘海 + 发丝细节
3. **服装**：上衣 + 下装 + 鞋袜 + 外搭 + 配饰，每件写颜色 + 面料 + 剪裁
4. **本段状态**：一段话描述本片段起点的内在/外在状态、动作倾向
5. **关系锁定**（多人场景）：关系类型 + 权力动态 + 触摸边界 + 当前关系状态 + 禁止互动

如任务开始时用户提供该角色图像，先把图像转写为脸型、五官、发型、体态、服装等纯文本锚点；block 开头写 "身份锚点：必须保持上述脸型、五官结构、发型和体态一致。" 不写“参考图 / 图源 / 如图所示”等词。
]
### @角色B / 主体B  [OPTIONAL — 多人/双主体时启用]
[与主体A 同样五层结构。]
## 表演控制谱  [REQUIRED — 含人物或拟人主体时]
### @角色A / 主体A  [REQUIRED]
[内在状态 + 外在掩饰 + 情绪泄露点 + 眼神目标 + 嘴部/下颌 + 呼吸节奏 + 手部动作 + 身体重心 + 动作速度 + 起点与终点。使用 rules/beat_choreography_rules.md 的情绪→节拍对照表。]
### @角色B / 主体B  [OPTIONAL]
[与主体A 同样的表演控制维度，强调两人之间的视线、距离、接触、反应节奏。]
## 道具锁定  [REQUIRED — 重要道具独立 block；不重要可压缩]
### @道具A  [REQUIRED for any locked prop]
[道具名称 + 外观细节 + 初始位置 + 使用方式 + 最终位置 + 跨镜头不变条件。]
## 关键统一原则  [REQUIRED — 锁定资产有跨镜头一致性需求时]
[例如:Yingying 全程戴蓝白针织帽，不出现未戴帽子版本；粉色猫咪手机始终保持粉色硅胶壳+白色珠串挂绳+粉色爱心吊坠的识别特征。]
## 片段核心  [REQUIRED]
[这个片段真正要表达的核心。写成可生成的最终创作约束，不写推理过程：情绪任务、视觉重点、人物/产品/空间关系、记忆点画面、最终落点。]

——————
# 分镜画面模块  [REQUIRED — 每镜独立 block]
## 分镜1：（[景别] / [镜头类型] / [功能定位；若为记忆点镜头，在此标注“记忆点”]）
### 画面：  [REQUIRED — 必须包含节拍链 + 细节密度]
[动作必须按 rules/beat_choreography_rules.md 写成节拍链，建议 0.5 秒/拍，用顿号/逗号分隔子拍，用「……」标记停顿，用「——」标记强调。镜头持续时间内的总拍数 = 时长(秒) × 2，对于 3 秒镜约为 6 拍。

同时必须满足 rules/detail_density_rules.md: 起点状态 + 触发动作 + 微反应 + 材质/空间参与 + 落点状态。标准 2-3 秒镜头通常写 90-180 个中文字符；记忆点镜头可写 150-260 个中文字符。不要只列人物、道具和地点。]
### 注意力控制：  [REQUIRED]
[先看什么，再看什么；由光线、动作、眼神、焦点、声音、颜色、前景、线条、尺度或留白如何引导；本镜头最后视线落在哪里。]
### 镜头参数：  [REQUIRED]
[焦距 + 光圈 + 快门 + ISO + 景深。优先使用具名的视觉性格（iPhone 原相机 50mm 2x / Stock Anamorphic / Modern Cinema Sharp 等)。]
### 运镜：  [REQUIRED]
[拍摄方式与运动路线。以画面左右、前后、上下、靠近/远离描述。]
### 构图：  [REQUIRED]
[人物/主体位置、前景/中景/背景关系、留白、线条、视线引导、运动动线。]
### 场面调度：  [REQUIRED]
[人物/主体、产品/道具、镜头、光线、空间、动作之间的关系；进入、退出、遮挡、反射、距离变化或空间压力。]
### 光影：  [REQUIRED]
[光源方向、光线性质、明暗分布、特殊光影、色彩。]
### 表演重点  [REQUIRED]
[表情、眼神、呼吸、手部、身体重心、动作力度、情绪泄露或掩饰、产品/主体呈现方式。性能细节必须匹配景别。]
### 节奏停顿：  [REQUIRED]
[本镜头何时移动、何时放慢、何时停住；停顿要让观众记住什么。]
### 音效：  [REQUIRED]
[环境声、动作声、呼吸声、物体声、空间声。]
### 台词：  [REQUIRED — 无台词时显式写「无。」]
[台词。无台词写：无。]
### 时间：0-X秒  [REQUIRED — 整数秒]

——————
[其余分镜按相同模板重复]

——————
# 整体质感  [REQUIRED]
[年代感、清晰度、颗粒、柔焦、色彩、对比度、光线、材质、湿润感、广告感、电影感或CG质感。

**关键要求**: 开头必须复述一次 `# 核心风格` 中相同的滤镜栈 + 色板 + 光源 + 反差规则。整体质感的 filter stack 与 `# 核心风格` 不一致视为 QC 失败。]
# 音效设计  [REQUIRED]
[完整音效方向。包括环境底噪、动作声、物体声、呼吸声、远近空间声、音乐节奏感。无对白则明确写：无对白。]
# 避免  [REQUIRED — 至少 5 行]
[禁止出现的视觉/性能/连续性失败。每行一条具体指令，参考 rules/avoidance_section_rules.md 的分类模板:
- 1-2 行针对光线/时段（避免晴天太阳直射 / 避免暖黄日照斑块 ...)
- 1-2 行针对滤镜/外观（避免商业广告清透 / 避免蜡感磨皮 ...)
- 1-2 行针对表演/情绪（避免夸张大笑 / 避免突然很配合 ...)
- 1-2 行针对构图/镜头（避免普通正面叙事机位 / 避免远景 ...)
- 1+ 行针对锁定资产的连续性锚点（[角色名] 全程穿 X / 不要中途换 ...）

省略此段、或少于 5 行，输出视为不合格。]
# 核心关键词总结  [REQUIRED]
[3-10个关键词。]
```
