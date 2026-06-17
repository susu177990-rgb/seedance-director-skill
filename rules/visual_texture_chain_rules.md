# Visual Texture Chain Rules

The **single largest gap** between amateur and director-grade Seedance prompts is the texture chain: light source → color science → filter stack → grain → lens character. A prompt that names only "warm light, soft mood" loses to a prompt that names "厚云阴天漫射光 + 旧 DV + 16mm 胶片混合 + Pro-Mist 雾化 + 轻颗粒 + 奶白 bloom + 边缘失焦".

This file is mandatory for any prompt with a defined cinematic, MV, TVC, mood, or visual-style intent. It is optional only for true amateur / raw / minimal-direction briefs where style is intentionally uncontrolled.

## Why Texture Chains Matter

AI video generators read texture words as high-priority signals. Without a written chain, the generator defaults to "modern digital video, neutral lighting, generic beauty filter" — presentable but not authored. With a chain, the generator composes a coherent visual identity that's reproducible across shots.

## The Six-Layer Texture Format

Write texture in this order. Be specific. Each layer is one strong phrase; never collapse layers.

### Layer 1 — Light Source

Name the exact physical light source and its atmospheric state.

| Generator default (bad) | Authored (good) |
|---|---|
| 暖色灯光 | 左后方暖黄色台灯，单一主光，无补光 |
| 阴天 | 夏日厚云阴天漫射光 |
| 暗调 | 室内只开一盏床头灯，窗外无光 |
| 日落 | 日落前 30 分钟，低角度暖橙直射，长阴影 |

Generic weather adjectives lose. Always include:

- **Source type**: 直射太阳 / 厚云层漫射 / 钨丝灯 / 荧光灯 / 蜡烛 / 屏幕反光 / 霓虹 / 头灯 / 台灯 / 窗外反射
- **Direction**: 正前偏上 / 左后方 45 度 / 顶部 / 高位漫射 / 全方位
- **Atmospheric state**: 干燥 / 潮湿 / 闷白 / 颗粒空气 / 灰尘漂浮

### Layer 2 — Color Science

Lock one of these named palettes. Never use "高级感" alone.

**Pastel youth:** 奶白灰 / 淡青 / 灰蓝 / 柔粉 / 浅米 — 低饱和清淡
**Noir cold:** 冷白 / 灰蓝 / 青灰 / 黑 — 高对比低彩度
**Warm amber:** 琥珀 / 蜂蜜 / 暖橙 / 黄铜 / 焦糖 — 中度饱和暖调
**High contrast natural:** 实色 / 真实肤色 / 真实布料色 — 不滤镜化
**Dreamcore haze:** 灰雾 / 浅紫 / 灰粉 / 奶白 — 整体偏灰高调
**Neon night:** 霓虹紫 / 蓝绿 / 品红 / 黑底 — 强光反差
**Muted documentary:** 灰黄 / 墨绿 / 土色 / 暗红 — 纪实低彩度

Lock palette + saturation level + skin tone preservation rule in one sentence.

**Skin tone preservation rule is mandatory**: 保留真实肤色，未被滤镜偏移 / 不出现蜡感磨皮 / 保留毛孔和细小肤质. Without this rule, the AI assumes "make everyone look porcelain".

### Layer 3 — Filter Stack

Pick the named stacks that fit the format. Combine 3-5 max.

| Stack name | Components | Use when |
|---|---|---|
| **Vintage DV + Film Mix** | 旧 DV 低保真 + 16mm 胶片 + 轻偏色 | 千禧年青春 / 复古 MV |
| **Pro-Mist Haze** | Pro-Mist 雾面滤镜 + 高光溢出 + 边缘柔化 | 青春梦境 / 气息回忆 |
| **Stock Anamorphic** | 变形宽银幕镜头 + 拉丝光斑 + 椭圆高光 | 电影感 / 叙事片段 |
| **Modern Cinema Sharp** | 现代数字 + 中等锐化 + 自然反差 | 当代剧情 / 高端 TVC |
| **iPhone Native Cam** | iPhone 原相机 + 计算摄影 + 数字锐化 + 高反差 | 真实感 / Vlog / 现实主义 |
| **Flash On Raw** | 强制闪光 + 极硬光 + 数字锐化拉满 | 纪实抓拍 / 怪诞情绪 |
| **Soft Dream Bloom** | 大光圈 + 重 bloom + 边缘虚化 + 焦外柔光 | MV 情绪梦境 / 少女感 |
| **Cold Clean Diode** | 冷调 + 高对比低彩度 + 无雾化 | 极简 / 时尚 / 未来感 |

The chosen stack must be named in **核心风格** and **整体质感** with the same wording — drift between the two segments is a common failure.

### Layer 4 — Grain and Texture Artifact

Pick one of:

- 无颗粒 / 极轻颗粒 / 轻胶片颗粒 / DV 数字噪点
- 轻 bloom / 中 bloom / 重 bloom / 高光溢出
- 轻微跑焦 / 焦点呼吸 / 焦外融化 / 边缘失焦
- 轻偏色 / 巧克力色偏 / 偏光闪烁 / 轻微彩边 / 色彩偏移到青绿

Combine into one sentence describing the artifact texture: "轻胶片颗粒 + 轻 bloom + 轻微跑焦 + 焦外柔化处轻微彩边".

Be explicit about **what does not appear**: 不出现过度锐化 / 不出现磨皮蜡感 / 不出现商业广告式清透. The negative constraint here is as important as the positive visual.

### Layer 5 — Lens Character

Always name a focal length + aperture + sensor personality:

- **焦距**: 24mm 广角拉长线条 / 28mm / 35mm 标准 / 50mm / 65mm / 85mm 近摄 / 135mm
- **光圈**: f/1.4 极致浅景深 / f/1.8 / f/2.0 / f/2.8 / f/4 / f/5.6 全景深
- **快门**: 1/30 拖影 / 1/50 自然 / 1/100 / 1/200 抓拍 / 1/1000 / 1/2000 高速定格
- **ISO**: 200 干净 / 400 / 640 轻噪 / 800 / 1000 高噪 / 1600+
- **镜头特点**: 边缘畸变 / 焦外二线性 / 焦外旋转 / 抗眩光性能差

For iPhone-native camera briefs, write: "iPhone 原相机 50mm 焦段（2x 长焦调用） / f/1.8 算法光圈 / 数字锐化痕迹".

### Layer 6 — Dynamic Range and Black Point

Lock these or the AI defaults them:

- **High key** (高调): 大面积亮部 + 暗部少量
- **Mid key**: 平衡明暗
- **Low key**: 暗部为主 + 光源附近少量亮
- **Black point**: 暗部不压死黑，轻微抬灰 / 暗部死黑，对比度极强
- **White point**: 奶白溢出 / 硬白 / 纯白高光 / 软白

For dreamcore / youth / MV: **暗部抬灰 + 高光奶白溢光** 是反复出现的组合。
For noir / suspense / cyberpunk: **暗部死黑 + 高光硬白** 是反复出现的组合。

## Texture Chain Template (Copy Format)

Use this exact sentence pattern in **核心风格**:

```
[Format 名] / [年代 / 风格流派] / [色板名] / [滤镜栈名] /
[光: source + 方向 + 大气状态] /
[反差: high key / mid key / low key] /
[颗粒: 强度] / [bloom: 强度] / [跑焦: yes/no + 强度] /
[skin 保留规则] /
[deny list: 不出现 X / 不出现 Y]
```

Example correctly filled:
```
2000 年代东亚青春 MV / 旧 DV + 16mm 胶片混合 / 奶白灰 + 淡青 + 灰蓝 + 柔粉 / Pro-Mist 雾化混合 stack /
光: 厚云阴天夏日 + 灰白漫射 + 经过白纱窗帘再次过滤 / 高 key 偏暗 /
轻颗粒 + 轻 bloom + 轻微跑焦 + 边缘失焦 / 保留真实肤色毛孔和细小色点，不磨皮 /
不出现晴天太阳直射 / 不出现暖黄日照斑块 / 不出现蜡感商业磨皮
```

## Cross-Section Repetition Lock

**整体质感** 段必须使用与 **核心风格** 相同的滤镜栈、相同的色板、相同的光源类型、相同的反差规则。漂移 = QC flag。

具体写法: 在整体质感段开头复述一次风格名 + 色板名 + 滤镜栈名, 然后再展开单帧描述。

## Auto-Correct Triggers

Before final output, rewrite if:

- Texture chain has fewer than 4 named layers
- 色板 has fewer than 4 named colors
- 滤镜栈 not named with stock filter or composition
- 反差规则 absent
- skin 保留规则 absent
- deny list absent
- 整体质感 与 核心风格 在光源/色板/反差上不一致
