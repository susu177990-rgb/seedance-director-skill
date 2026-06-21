# Detail Density Rules

Most failed first-pass Seedance prompts are not wrong; they are thin. They have the right modules but each shot's `### 画面` reads like a location list instead of a filmable moment.

These rules are mandatory for final prompt-writing tasks unless the user explicitly asks for a very short minimal prompt.

## Minimum Shot Density

Every non-static shot's `### 画面` block must contain all five layers below:

1. **Start state** — where the subject is, what body state or object state exists before the action.
2. **Trigger action** — what physical action begins the shot.
3. **Micro-reaction** — what face, gaze, hand, breath, posture, prop, or environment does in response.
4. **Material / space participation** — how light, fabric, water, glass, hair, prop texture, floor, wall, foreground, background, shadow, or reflection participates.
5. **Landing state** — what exact visible arrangement the shot settles on.

Thin:

```text
她坐在床边，手拿帽子看向对方，表情开心。
```

Dense:

```text
床边近景。Ling 身体微侧坐在床沿，刚把书页压在膝盖上停住；Yingying 已经戴着蓝白针织帽，从右后方探进来，双手举着黄色兔耳帽往 Ling 头顶比划。Ling 肩膀先缩一下，头偏向另一侧，眉头轻轻蹙住，左手抬到帽檐前但没有真正推开；黄色兔耳帽的毛线边快碰到她的头发，蓝白帽垂饰随 Yingying 前倾轻轻晃动。镜头落在两顶帽子同时进入画面的瞬间，关系一眼成立。
```

## Per-Shot Minimums

For final prompts:

- Standard 2-3 second shots: `### 画面` should usually be 90-180 Chinese characters.
- Dense memory-point shots: 150-260 Chinese characters is normal.
- Very short spike shots under 1.5 seconds may be shorter, but must still include start state, trigger, and landing state.
- If a shot's `### 画面` is under 70 Chinese characters, it is presumed thin and must be rewritten unless it is a deliberate still-life insert.
- If three or more shots in one prompt have `### 画面` under 90 Chinese characters, the prompt has failed density QC.

This is not a request for bloated language. Every added phrase must give the generator a visible instruction.

## The Dense Shot Formula

Use this internal formula before writing each shot:

```text
[where / whose body or object starts] + [what enters, moves, touches, turns, or stops] + [who reacts and how] + [what light/material/space changes or guides attention] + [what exact visual state the shot lands on]
```

Examples:

- `地毯边的小物散着` is not enough. Add what hand tries to pick up, what slips again, what sound or material marks the mistake, and where the eye lands.
- `两人差点撞上` is not enough. Add who carries what, which path crosses, whose body retracts first, what eye contact lasts less than a second, and how the space feels tighter.
- `玩偶遮住脸` is not enough. Add starting scale, hand pressure, distance pushed, which facial part disappears first, what remains sharp, and where the final highlight sits.

## Material Participation

At least one material or spatial element must do a job in every shot. It can:

- guide attention: light line, reflection, foreground, sound, color contrast
- create pressure: doorway, table edge, wall, crowd, narrow space
- reveal relationship: hand-to-prop, subject-to-animal, product-to-light, face-to-reflection
- stabilize continuity: same lamp, same floor, same prop location, same wardrobe edge
- create memory: water ripple, glass distortion, fabric edge, hair movement, plush bloom

Reject shots where the environment merely exists as decoration.

## Thin-Shot Rewrite Triggers

Rewrite silently before output if `### 画面` does any of these:

- Lists objects without an action sequence.
- Says only "她看向镜头 / 他走过去 / 产品在桌上".
- Names emotion without a visible leak.
- Uses a prop only as a label, not as something touched, moved, blocked, reflected, revealed, or anchored.
- Describes composition elsewhere but leaves the `画面` block generic.
- Has no final settled frame.
- Could be reused in another prompt by only swapping character names.

## Density Without Overload

Do not solve thinness by adding too many simultaneous events. Good density is not more events; it is clearer physical resolution of one event.

Prefer:

```text
one subject + one prop + one reaction + one light/material behavior + one landing frame
```

Avoid:

```text
three subjects + five props + multiple camera moves + changing location + emotional twist in one 2-second shot
```

## Final QC Question

For every shot, ask:

> If Seedance only read the `### 画面` block and ignored the other modules, would it still know what physically happens, what reacts, and what frame to land on?

If the answer is no, rewrite the shot.
