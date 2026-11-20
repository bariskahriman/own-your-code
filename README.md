# Own Your Code — v0.1.0 (experimental)

**Understand the code behind the products you build with AI.**

Own Your Code is a beginner-friendly **Codex Agent Skill**. It reads relevant source code and teaches you how a feature of *your own app* works, with verifiable references and short comprehension checks.

It is **not** a code editor, a security auditor, or a guarantee that you can independently review production code. Version 0.1 is instruction-only and read-only.

## Install for Codex

From Codex, ask the built-in skill installer (if available) to install the skill at:

```text
https://github.com/bariskahriman/own-your-code/tree/main/own-your-code
```

Alternatively, clone the repository and copy its inner skill directory into your personal skill directory:

```bash
git clone https://github.com/bariskahriman/own-your-code.git
mkdir -p ~/.agents/skills
cp -R own-your-code/own-your-code ~/.agents/skills/
```

For project-only installation, place the inner `own-your-code` folder in `<repo-root>/.agents/skills/` instead. Don't overwrite an existing installation without reviewing it first.

From Codex in the relevant project, invoke `$own-your-code` and describe the feature you want to understand. If it does not show up, restart Codex.

No extra Python or Node packages, accounts, or API keys are required by the skill itself.

## Example invocation

> $own-your-code
>
> Run a learning experiment. Teach me how a user pressing Generate results in an image appearing on screen, using the real source. My baseline: I think the app checks credits, calls the image model, shows the image, and subtracts a credit. Treat this as a hypothesis, not as verified architecture. Work read-only. Start with the first small concept, then ask me one question.

## What it does
- Asks for or accepts a baseline mental model.
- Follows a concrete feature across code layers.
- Explains one stage at a time with `path:line` references.
- Checks whether you can explain that code in your own words.
- Can compare pre/post understanding using a transparent rubric.

## Safety and scope
- Read-only instructions: no source edits, generated comments, code execution, installs, commits, or pushes.
- Does not print credentials or claim implementation equals verified deployed behavior.
- Does not silently generate documentation files inside the repository.
- These are agent instructions, not a sandbox or an independently enforced security boundary.

## Status
**Prototype, not yet user-validated.** Test first on a real product, then assess whether it adds value beyond a normal Codex explanation.

## Repository layout

```text
own-your-code/
├── README.md
└── own-your-code/
    ├── SKILL.md
    └── references/
        └── evaluation.md
```

## Skill format
`SKILL.md` with YAML frontmatter (`name` and `description`), plus a supporting evaluation reference.

Specification / Codex paths: https://agentskills.io/ and https://developers.openai.com/codex/skills
