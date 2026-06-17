# Beat Choreography Rules

A Seedance shot is not a state; it is a **choreographed time slice**. The single largest fix-vs-rewrite trigger between amateur and director-grade prompts is whether the action is described as a **chained beat list with punctuation-gated pauses** or as a single verb-phrase blob.

This rule is mandatory for any shot where motion or performance is the primary attention target.

## The Default Failure Mode

Most prompts write shots like this:

> 桌上放着一杯咖啡。女子端起咖啡喝了一口。

This describes a before-state and an after-state without describing the **time slice in between**. Seedance interprets these as "either-or", and the generator tends to render the before-state because that's what's stable. Result: shots look like still photography with implied but unrendered action.

## The Required Format: Beat Chain

Every active shot must specify the action as a **4-7 beat chain** with punctuation-gated time slices, in this order:

```
[stall beat] → [approach beat] → [contact beat] → [reaction beat] → [settle beat]
```

Read top to bottom, each beat = roughly 0.3-0.5 seconds of real time. For a 3-second shot, that's ~6 beats. For a 2-second shot, ~4 beats.

### Beat naming

Each beat must be named with a stable verb phrase:

- **Stall beat** (凝固): 身体停顿 / 视线停住 / 手指悬停在 X 上 / 屏息 — the prior-state pause
- **Approach beat** (引动): 手指缓慢抬起 / 头部微微偏过 / 肩膀下沉 / 目光短暂下移 — the setup motion
- **Contact beat** (触碰): 指尖碰到杯口 / 视线落进对方眼睛 / 手背擦过脸颊 / 衣物碰到地面 — the contact instant
- **Reaction beat** (反应): 嘴角松动 / 下颌收回 / 呼吸停半拍 / 手指微蜷回自己身上 / 视线压低再抬回 — the response
- **Settle beat** (落定): 视线回到主点 / 肩膀稳住 / 呼吸恢复 / 身体重心重新静止 — the return-to-base

The chain is **read top to bottom by Seedance**, so the order is the temporal order, which is also the narrative order.

## Writing the Chain

Use **between-beat punctuation as time marks**. The grammar is:

- 中文顿号`、` or comma = sub-step within a beat (sub-second micro-motion)
- 中文句号`。` = beat boundary (~0.5 second real time)
- 省略号`……` = held beat (pause extends a beat by another 0.3-0.5 second)
- 破折号`——` = internal pressure mark within a beat (light emphasis but no time)

Example chain (3-second shot):

> 视线先停在镜头左下角约 0.5 秒……手指从桌面慢慢抬起……指尖摸到杯身瓷面……杯沿缓缓靠向嘴唇……嘴唇微启含住杯口……吸气停顿半拍……放下杯，手指回到杯身瓷面上停住。

Count the beats: 7 (≈ 3 seconds at 0.5 sec/beat). Note the punctuation: `……` on the stall beat, `。` between beats, internal commas within reach beat. The chain is internable.

### Counter-example (the failure mode)

> 女子端起咖啡喝了一口。

One verb-phrase. No beats, no pause grammar, no settle. Seedance has to guess.

## Beat Chain Length by Shot Duration

| Shot duration | Required beats |
|---|---|
| 1.0 second spike shot | 2-3 beats |
| 2.0 seconds | 4 beats |
| 3.0 seconds (standard) | 6 beats |
| 4.0 seconds | 7-8 beats |
| 5.0 seconds (longest allowed) | 8-10 beats |

Spike shots (single-action highlights) can have fewer beats but must still chain. A "raise hand" shot at 1s needs even: 手指抬起 → 手指停住 = 2 beat minimum.

## Invisible-Action Beats

For shots that show no obvious motion (a held gaze, a frozen smile, a quiet environment shot), beats still apply but they're **internal or atmospheric**:

- 眼睑轻闭一次 → 睁开时瞳孔对焦回到镜头
- 呼吸起伏一次 → 呼出时嘴角微松
- 头发丝轻轻被风推动 1 厘米 → 落回原位
- 前景植物叶子轻微晃一下 → 静止

If a shot truly has no internal motion, write **explicit stillness** as the beat chain:

> 镜头近 5 秒内完全静止……仅屋檐一滴雨水落下……其余全部静止。

The word 静止 is mandatory for true still shots so the AI doesn't invent motion.

## Multi-Character Shot Beat Chains

For two-character shots, beats must specify **whose beat, in what order**:

> Yingying 手指先轻微抬起……帽身微微前推……Ling 头部轻轻向反方向偏……肩膀微微一缩……手指象征性挡在帽子前方……Yingying 身体略微前倾……眼睛亮起来……

Pattern: 主主动方 beat → 接受方 response beat → 主主动方 confirm beat. Cycle 2-3 times per shot. **Always alternate** — never give one character two consecutive beats without the other responding.

## Emotion-to-Beat Translation Table

Replace abstract emotion labels with beat chains:

| Abstract label | Beat chain replacement |
|---|---|
| 紧张 | 手指收紧 → 呼吸屏住 → 嘴角抿住 → 视线下移不到 1 秒 → 抬起眼 |
| 心虚 | 眼神从镜头快速扫过 → 落在角落 → 又被拉回 → 嘴角出现微小动作 |
| 释然 | 肩膀明显下沉 → 呼气延长 → 眼神回到远处而不是镜头 → 手指自然松开 |
| 压抑的哭啼 | 吸气停顿 → 下颌抖动 → 声音从喉咙挤出来 → 头垂下去 → 手指压在膝盖上 |
| 期待+紧张 | 视线先看窗台 → 手指轻轻点桌面 → 手收回 → 再看向门口 → 嘴角微微松 |
| 克制的笑 | 下眼睑轻收 → 掀起嘴角一点点 → 下颌不动 → 视线停在某个物体上 |
| 无奈 | 抬头看一眼 → 眼神停半秒 → 长呼气 → 语气平 → 手落回原位 |
| 调皮得逞 | 嘴角上扬先停一下 → 肩膀跟着轻微抖一下 → 眼神快速看向对面 |
| 安静的拒绝 | 头微微偏向一侧 → 视线从镜头落下 → 手指轻抬做出半挡的动作 → 不再说话 |

These chains are trial-tested in MV / iPhone-native short-form briefs. Each one survived 5-10s generations without collapse.

## Beat Chain Anti-Patterns

Reject the chain if any of these appear:

- **No settle beat** at the end (chain ends mid-action) → flag as action cut-off
- **Same beat twice in a row** for one character → flag as thinking-out-loud
- **Two simultaneous contradictory beats** (e.g., 嘴角上扬 + 眉头紧锁) without intentional contrast
- **Chain shorter than shot duration** → AI will pad with random motion
- **Chain with no pause punctuation** (no `……` or `——`) → action reads as one rushed blur
- **Final beat is a verb**, not a state → flag because final beat must be the settled state, not a continued motion

## Beat-Chain Verification

Before slotting the chain into a shot:

1. Read top-to-bottom at 0.5 sec/beat. Does the timeline match the shot duration?
2. Read the last beat alone. Is it a state, not an action? (e.g., "手指停在 X 上 / 肩膀保持原位", yes; "手指继续向上", no)
3. Identify the dominant beat (the contact beat). Does it match the shot's primary attention target?
4. For multi-character shots, count beats per character. They should be roughly equal, ±1.
5. Are there `……` hold beats near the most important moment? (The most important moment usually wants a hold before it.)

If verification fails, revise the chain before generating.

## Beat Chain vs. Format

Some formats have intentionally fast beat chains:

- **MV rhythm cuts**: 2 beats per second, sometimes single-beat spike shots
- **Action / suspense**: Tight beats, no holds except in reveal
- **Vlog / handheld casual**: Long holds with micro-motion (breath, blink)
- **Beauty / fashion**: Beat chain emphasizes gaze + posture shifts over hand motion
- **Documentary**: Beat chain is environmental (background motion carries the beats)

Match the beat cadence to the format grammar, not to a single universal tempo.
