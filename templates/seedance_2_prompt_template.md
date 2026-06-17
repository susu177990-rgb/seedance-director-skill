# Seedance 2.0 Final Prompt Template

Use this template for every final prompt-writing task. Modules marked **[REQUIRED]** must ship. Modules marked **[OPTIONAL]** are conditional and only used when the brief needs them. Do not collapse required modules. Add optional modules before `# 整体质感` or as dedicated shot annotations.

**Mandatory checks before shipping:**

1. Every `[REQUIRED]` module is present and not stubbed.
2. `# 避免` is present with **at least 5 lines** spanning lighting, filter, performance, and continuity.
3. `# 整体质感` repeats the **same texture chain wording** as `# 核心风格` (filter stack + light source + color palette + dynamic range). Drift is a fail.
4. Each shot's `#画面` block contains a **beat chain** matching `rules/beat_choreography_rules.md`.
5. Each principal character lock has the **face / hair / wardrobe / behavior / relationship** layers as defined in `rules/role_lock_detailed_rules.md`.

```markdown
片段名：[片段名称]
时长：[用户未指定具体时长时固定写15秒；用户指定15秒以内具体时长时写用户时长]
比例：[16:9 / 9:16 / 1:1 / 2.39:1 等]
类型：[选择3-10个关键词：真人电影感 / 产品广告 / 青春MV / 动作片段 / CG动画 / 奇幻短片 / 生活方式广告 等]
分镜数量判断：[导演根据内容密度、注意力路径和节奏自行判断1-9个分镜]

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
## 格式与导演策略  [REQUIRED]
[明确本片段属于电影/剧情、TVC、MV、短视频、vlog/随手拍、纪录感、产品广告、动作、CG/动画、奇幻、旅行、美食、时尚等哪种格式。写清楚观看场景、注意力速度、真实感/精致度、表演方式、镜头克制程度和最终落点。]
## 观众注意力路径  [REQUIRED]
[观众第一眼看哪里，第二眼被引到哪里，什么信息先隐藏，什么时候揭示，最终视线落在哪里。写清楚注意力引导手段：光、动作、眼神、焦点、声音、颜色、前景、线条、尺度或留白。]
## 导演判断与取舍  [REQUIRED]
[本片段最该拍的瞬间、不该拍或应删掉的信息、镜头距离判断、该动的镜头、该停的镜头、最终希望观众感受到什么。]
## 简单指令扩展策略  [OPTIONAL — 仅当用户输入非常简短时启用]
[如果用户只提供很简单的指令，写清楚如何扩展成完整15秒片段：开场读画面、触发动作、发展变化、揭示或转折、停顿、最终记忆画面。若用户信息已经充分，可删除本模块。]
## 导演性记忆点  [REQUIRED]
[本片段最值得被记住的视觉主意。写清楚哪个镜头是记忆点镜头，以及它通过构图、遮挡、物件、空间关系、动作节奏、光线或反差制造不可替代的观看点。]
## 场面调度关系  [REQUIRED]
[人物/主体、产品/道具、镜头、光线、空间、动作之间如何互相发生关系。写清楚前景/中景/背景角色、空间锚点、运动路径、遮挡/反射/光线参与方式和关系变化。]
## 节奏与停顿策略  [REQUIRED]
[开场让观众读画面的时间、动作加速点、揭示点、停顿点、最终落点。明确哪里必须停住让产品、情绪、动作或空间被记住。]
## 场景锁定  [REQUIRED — 若场景不重要可压缩到 2-3 行]
[固定场景。明确时间、地点、天气、空间结构、主要环境元素、色彩、光线与必须保留的空间锚点。]
## 角色锁定  [REQUIRED — 每个主体独立 block]
### @角色A / 主体A  [REQUIRED]
[必须按以下顺序书写，遵循 rules/role_lock_detailed_rules.md 的五层密度:

1. **脸与身体锚点**：脸型 + 颊 + 下颌 + 下巴 + 眼型 + 瞳孔色 + 卧蚕 + 鼻型 + 唇型 + 唇色 + 眉形 + 皮肤纹理 + 关键痣/斑 + 身形
2. **发型**：长度 + 色 + 刘海 + 发丝细节
3. **服装**：上衣 + 下装 + 鞋袜 + 外搭 + 配饰，每件写颜色 + 面料 + 剪裁
4. **本段状态**：一段话描述本片段起点的内在/外在状态、动作倾向
5. **关系锁定**（多人场景）：关系类型 + 权力动态 + 触摸边界 + 当前关系状态 + 禁止互动

如任务开始时用户提供该角色的参考图，需在 block 开头加 "（必须完美还原 [图源描述] 的五官长相）"。
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
[这个片段真正要表达的核心。写清楚情绪任务、视觉重点、人物/产品/空间关系、镜头重点和观众应该感受到什么。]

——————
# 分镜画面模块  [REQUIRED — 每镜独立 block]
## 分镜1：（[景别] / [镜头类型] / [功能定位]）
### 画面：  [REQUIRED — 必须包含节拍链]
[动作必须按 rules/beat_choreography_rules.md 写成节拍链，建议 0.5 秒/拍，用顿号/逗号分隔子拍，用「……」标记停顿，用「——」标记强调。镜头持续时间内的总拍数 = 时长(秒) × 2，对于 3 秒镜约为 6 拍。]
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
### 性能重点  [REQUIRED]
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
