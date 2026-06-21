# Role Lock Detailed Rules

Every principal character or recurring subject in a Seedance 2.0 prompt must be locked at five-layer density. A thin role lock ("年轻女性，长直黑发，干净淡妆") makes AI video default to generic beauty footage and lose character identity across shots.

These five layers are mandatory unless the brief is genuinely single-character casual handheld with no continuity need.

## Layer 1 — Face and Body Anchors

Write the identity anchors that survive a 3-15 second shot, in this exact order:

1. **Face shape** (鹅蛋脸 / 圆短鹅蛋脸 / 窄长鹅蛋脸 / 方圆脸 / 心形脸 / 菱形脸)
2. **Specific structural cues** (下颌线 / 下巴 / 颧骨 / 发际线)
3. **Eye shape, color, and signature** (杏眼 / 细长眼 / 圆杏眼 + 瞳孔颜色 + 卧蚕 / 单眼皮内外双 / 眼距 / 是否有下眼睑特征)
4. **Nose shape** (小圆鼻 / 细直鼻梁 / 翘鼻 / 鼻头大小)
5. **Lip shape and color** (薄唇 / 饱满唇 / 嘴角走势 / 唇色)
6. **Eyebrow** (平眉 / 弯眉 / 粗细)
7. **Skin** (白皙 / 偏黄 / 古铜 + 真实纹理：毛孔 / 痘印 / 色斑 / 痣位置 — 至少 1 个不可忽略的识别点)
8. **Body type** (纤细柔软 / 高挑修长 / 小只紧凑 / 瘦削单薄 / 微胖)
9. **Signature expression cue** (微笑克制 / 嘴角平直 / 月牙眼 / 小虎牙 / 眼下暗沉)

For multi-character scenes, **at least one character must carry a single unique identification mark** (e.g., a small mole at the left outer canthus, a chipped nail, a specific ear piercing, a single freckle pattern) — this is what prevents two-char identity drift.

## Layer 2 — Hair and Styling

Hair must be described as a fixed rather than abstract asset:

- **Length** (短波波头 / 中长锁骨发 / 长直发到腰 / 及肩短发)
- **Color base** (自然黑 / 深棕黑 / 冷棕 / 染过的具体色号)
- **Texture and cut** (空气刘海 / 中分 / 偏分 / 内扣 / 外翘 / 自然直 / 自然卷)
- **Movement signature** (碎发飞发 / 蓬松 / 服贴 / 局部挑染 / 发丝飞扬的镜头行为)
- **Daily styling baseline** (头发状态：干净 / 微油 / 刚洗吹蓬松 / 戴帽子压过的痕迹 / 已固定的马尾)

For long shoots, lock hair behavior phrase — 头发全程自然 / 雨天湿贴 / 风吹时飞发 — so multiple shots stay consistent.

## Layer 3 — Wardrobe and Body Wear

Replace "穿 X 套装" with structured wardrobe that survives costume-detail questions:

- **Top**: color, fabric feel, cut, neckline (圆领 / V领 / 吊带 / 荷叶边 / 褶皱), sleeve, fit
- **Bottom**: color, length, waist, fit
- **Footwear**: must be present if visible in any shot
- **Layering**: cardigan / coat / apron / scarf / socks distinctly named
- **Accessories**: jewelry / hair accessories / glasses / watch / bag / headwear

If a wardrobe has multiple states across shots (e.g., Yingying wears sleepwear but Ling wears outdoor jacket), **state each wardrobe's full coordinates** so there's no ambiguity. Every wardrobe must have at least **3 named items + color + fabric cue**, never just 1-2 generic words.

If the user provides reference images of characters before writing, **read those images first and lock wardrobe only after visual confirmation**. Do not invent character visuals when the user supplies reference images.

## Layer 4 — Body Behavior Baseline and Emotional Posture

A role needs an internal posture, not just an identity. Lock these before writing any shot:

1. **Default body weight** (重心靠前 / 收在后 / 上半身松 / 下半身紧)
2. **Movement rhythm** (动作慢而软 / 动作快而有节奏 / 动作小而克制 / 动作碎而灵动)
3. **Hand behavior default** (手常放哪 / 手指放松 / 手紧握 / 手搭下巴 / 手插口袋)
4. **Eye behavior default** (经常看哪 / 看镜头方式 / 视线距离感)
5. **Mouth / jaw default** (嘴角走势 / 牙是否可见 / 下颌紧松)
6. **Breath default** (浅慢 / 深稳 / 屏息 / 抽泣节奏)
7. **Voice rhythm** (话少 / 不说 / 低语 / 沉默为主)
8. **Distance posture** (近人 / 远人 / 不主动贴近 / 倾向保持一臂距离)

These are the **return states** the character falls back to between actions. Without them, every shot invents a new character.

## Layer 5 — Relationship Anchor and Status State

This layer is what makes two-character scenes work. For each role, write:

1. **Relationship type** (朋友 / 同事 / 室友 / 暧昧未挑明 / 陌生人 / 母女 / 姐妹 / 师生)
2. **Power dynamic** (主动方 / 接受方 / 互不退让 / 一个暗恋一个不知 / 一个欠一个)
3. **Touch baseline** (允许触碰的部位 / 距离阈值 / 谁先发起)
4. **Status current state** (本段起点：亲昵但未点破 / 假装不在意 / 刚落单 / 暂住对方家 / 刚认识)
5. **Forbidden interactions** (绝对不要做的事: 不贴脸 / 不对视到镜头感 / 不做亲密暧昧 / 不暴露关系)

For multi-character scenes, write a separate **双人关系限制** section listing 3-5 lines of "两人是 X，不是 Y；不贴脸，不恋爱"，because Seedance defaults toward dramatic couple framing if not explicitly told otherwise.

## Continuity Lock Format

When writing the role lock block, use this exact field order — it is the field order Seedance parses most reliably:

```
### @角色名：
年龄 / 气质 / 身形
脸型 / 颊 / 下颌 / 下巴
眼型 / 瞳孔色 / 卧蚕 / 标识点
鼻型 / 唇型 / 唇色 / 眉形
皮肤 + 真实纹理 + 关键识别痣/斑
发型：长度 / 色 / 刘海 / 发丝细节
服装：上衣 + 下装 + 鞋袜 + 外搭 + 配饰
本段状态：（一段话描述本片段起点的内在/外在状态）
```

Final prompts that ship without all five layers are flagged as **thin locks** in QC and rewritten before output.

## Role Image Reference Convention

When the user supplies character images at task start:

1. **Treat the image as the visual ground truth.** Do not re-invent face, body type, or styling from imagination.
2. **Translate the image into text** using the five layers above.
3. **Do not mention the image source in the final prompt.** At the head of the role block, write a source-free identity lock such as: "身份锚点：必须保持上述脸型、五官结构、发型和体态一致。" Then list the extracted face/body/hair/wardrobe anchors as direct text.
4. **Lock wardrobe separately from identity** — wardrobe changes across segments even when identity stays fixed, and image references usually only confirm identity, not wardrobe across the whole project.

When the user does not supply character images, treat character description as inferred. Make stable, generation-friendly choices, but do not add visible "inferred/guessed" labels to the final prompt unless the user asks for an audit or planning note.
