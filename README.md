# Seedance Director Skill Pack

A universal multi-agent cinematic prompt director skill for Seedance 2.0.

This skill converts rough ideas, image descriptions, video-frame analysis, revision notes, character briefs, product briefs, and cinematic concepts into structured Seedance 2.0 prompts with professional shot design, continuity control, and AI video feasibility checks.

## One-Click Install

Install directly with:

```bash
npx skills add susu177990-rgb/seedance-director-skill
```

Generic format for forks:

```bash
npx skills add <YOUR_GITHUB_USERNAME>/seedance-director-skill
```

## Repository Name

```text
seedance-director-skill
```

## What This Skill Does

- Builds complete Seedance 2.0 prompts.
- Converts image/video visual references into text-only prompt language.
- Designs cinematic shot sequences under 15 seconds.
- Controls integer-second timelines.
- Maintains character, scene, prop, wardrobe, weather, lighting, and action continuity.
- Reduces AI video generation risk before final output.
- Works across MV, product ads, fashion, food, travel, fantasy, sci-fi, action, CG animation, short drama, documentary, and visual experiments.

## Internal Multi-Agent System

The skill coordinates these specialist agents:

1. Creative Director
2. Editor
3. Cinematographer
4. Blocking & Performance Director
5. Production Designer
6. Continuity Supervisor
7. AI Video Feasibility Reviewer
8. Prompt Compiler
9. QC Supervisor

The user sees only the final polished output unless they ask for diagnosis or planning.

## Folder Structure

```text
seedance-director-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── package.json
├── agents/
├── rules/
├── checklists/
├── templates/
└── examples/
```

## Usage Examples

### Create a Prompt

```text
用Seedance 2.0写一个15秒香水广告，清晨浴室，玻璃水雾，女性手部拿起瓶子，整体高级冷白调。
```

### Revise a Prompt

```text
这个镜头太远了，改成中近景，产品占比更高，人物动作少一点，整体更稳定。
```

### Audit a Prompt

```text
帮我检查这个Seedance提示词为什么容易崩，并重写成稳定版本。
```

## Output Principle

The final prompt should feel like a compact shooting plan, not a literary description.

Best output qualities:

- Clear
- Visible
- Filmable
- AI-generatable
- Continuity-safe
- Cinematically designed
