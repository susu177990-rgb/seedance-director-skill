# Time Design Rules

## Default Duration Strategy

If the user does not specify a concrete duration, use exactly 15 seconds.

If the user specifies a concrete duration of 15 seconds or less, use that exact duration.

If the user requests more than 15 seconds for Seedance 2.0, compress the concept into 15 seconds unless the user explicitly changes platform, batch structure, or segment format.

Never exceed 15 seconds for one Seedance 2.0 segment.

Shot count is not a fixed recommendation. The director must choose 1-9 shots by content density, viewer attention path, rhythm, and readability:

- 1 shot: one continuous gesture, hero product hold, spatial reveal, vlog/casual observation, or quiet emotional beat.
- 2-3 shots: simple insert, product reveal, character reaction, food/beauty/lifestyle moment, or short social beat.
- 4-6 shots: standard 15-second story, commercial, MV, travel, fashion, or character sequence.
- 7-9 shots: dense montage, action, transformation, multi-object product detail, or music-rhythm structure that still remains readable.
- Do not use 10 or more shots in one 15-second segment unless the user explicitly changes the format.

## Sparse Brief Expansion

When the user gives only a simple instruction, still build a complete 15-second segment. Expand through director judgment:

- Add a clear visual setup, not extra plot noise.
- Add one attention-guiding trigger or reveal.
- Add one development beat that makes the subject, product, emotion, or space change.
- Add a pause or inspection moment so the image has weight.
- End on a specific landing frame the viewer can remember.

Do not leave the prompt as a tiny action stretched over 15 seconds. Do not fragment simple briefs into many empty micro-shots. Choose the shot count that makes the 15 seconds feel intentional.

## Timing Patterns

### 5 seconds

```text
0-1秒：detail trigger
1-3秒：main action
3-5秒：hero/reaction
```

### 8 seconds

```text
0-2秒：space/subject setup
2-5秒：main action
5-8秒：reaction/hero ending
```

### 10 seconds

```text
0-2秒：setup
2-4秒：detail or trigger
4-7秒：main movement
7-10秒：resolution
```

### 15 seconds

```text
0-2秒：establish
2-5秒：action begins
5-7秒：detail/reaction
7-11秒：main development
11-15秒：resolution/hero frame
```

## Compression Rules

If there is too much content:

- remove secondary action
- reduce number of locations
- combine similar reaction shots
- replace complex movement with a single readable gesture
- make environment details static background anchors

## Warning Signs

- A 1-second shot contains walking, turning, speaking, and picking up an object.
- A 15-second segment has more than 9 shots.
- Every shot is 1 second.
- The most important emotional beat is shorter than the setup.
