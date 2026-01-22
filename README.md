# learn-codebase

> **The anti-vibe-coding skill.** A Socratic tutor that teaches you codebases 
> through questioning and active recall — because on mature projects, 
> understanding matters more than speed.

[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://code.claude.com/docs/en/skills)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Why This Exists

AI coding tools make it easy to generate code without understanding it. 
That works for greenfield projects. But when you're joining a mature codebase 
with high quality standards, "it works" isn't enough — you need to understand 
*why* it works.

This skill flips the AI interaction model:

| | Regular AI Coding | learn-codebase |
|---|---|---|
| Shows code immediately | ✅ | ❌ Asks you to predict first |
| Answers your questions | ✅ | ❌ Asks clarifying questions back |
| Optimizes for speed | ✅ | ❌ Optimizes for retention |
| Forgets between sessions | ✅ | ❌ Maintains learning journal |
| Makes you dependent | 😬 | ❌ Builds your independence |

## The Problem

You know that feeling after heavy AI-assisted coding — like swimming with fins, 
then taking them off? The skill atrophy is real. Research backs this up: a 2025 
study found developers using AI on familiar codebases were 19% *slower* than 
those without AI, yet believed they were 20% faster.

**This skill is for when you need to actually learn**, not just ship:
- Onboarding to a new team's codebase
- Preparing to contribute to open source
- Understanding legacy code before refactoring
- Building confidence before code review

## How It Works

The skill uses proven pedagogical techniques:

- **Socratic questioning** — Asks you to explain before explaining to you
- **Prediction before revelation** — You predict behavior before seeing it  
- **Active recall** — Quizzes you on what you've learned
- **Spaced repetition** — Schedules reviews at optimal intervals
- **Zone of Proximal Development** — Calibrates difficulty to your level
- **Persistent learning journal** — Tracks understanding across sessions

## Installation

### Personal skill (all projects)

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/ktaletskiy/learn-codebase ~/.claude/skills/learn-codebase
```

### Project skill (specific project)

```bash
mkdir -p .claude/skills
git clone https://github.com/ktaletskiy/learn-codebase .claude/skills/learn-codebase
```

## Usage

Start a learning session:

```
/learn-codebase
```

Or let Claude detect learning intent:
- "teach me about this codebase"
- "help me understand the auth system"
- "I need to learn how this works before contributing"
- "quiz me on what I learned"

## Example Session

```
You: /learn-codebase

Claude: I don't see a learning journal yet—let's set one up.

What's your goal with this codebase? Are you:
- Contributing new features
- Fixing bugs
- Doing code review
- General exploration

You: I want to contribute to the file browser module

Claude: Good, concrete goal. Before we dive in, what's your familiarity 
with the overall architecture? Have you worked with this codebase before?

You: I know it's TypeScript and uses Lumino widgets, but I'm new to the code

Claude: Perfect starting point. Looking at the directory structure, 
where do you *expect* file browser code to live?

You: Maybe `packages/filebrowser` or something like that?

Claude: Good instinct — it's actually `packages/filebrowser-extension` 
and `packages/filebrowser`. Before I show you the difference, why do 
you think they split it into two packages?

You: Hmm... maybe one is the core logic and one is the JupyterLab plugin?

Claude: 🎯 Exactly. Now let's trace what happens when a user clicks 
"New Folder"...
```

## Learning Journal

The skill maintains `.claude/learning-journal.md` tracking:

- **Focus & Goals** — What you're trying to accomplish
- **Concept Mastery** — Topics at 🔴 Confused / 🟡 Learning / 🟢 Confident
- **Open Questions** — Confusions to resolve
- **Spaced Review Queue** — Concepts due for review
- **Aha Moments** — Insights in your own words
- **Session Log** — History of exploration

This file persists across sessions and is yours to review and edit.

## Customization

### Teaching style preferences

Add to your journal's Focus & Goals:
```markdown
- Learning style: Prefers tracing real user actions through the code
- Learning style: Learns best by comparing to patterns I already know
- Learning style: Wants to understand tests before implementation
```

### Project-specific concepts

Create `CONCEPTS.md` alongside the skill to prime domain knowledge:
```markdown
# Key Concepts

## Lumino Widgets
The UI component system — everything visible inherits from Widget...

## Extension vs Package
Extensions register with JupyterLab, packages are standalone...
```

## Files

```
learn-codebase/
├── SKILL.md              # Main skill instructions
├── JOURNAL-TEMPLATE.md   # Template for new learning journals  
├── QUESTION-PATTERNS.md  # Socratic question reference
├── README.md             # This file
└── LICENSE               # MIT
```

## Contributing

This skill improves through real-world usage. After testing, consider contributing:

- New question patterns that worked well → `QUESTION-PATTERNS.md`
- Edge cases the skill handled poorly → GitHub Issues
- Domain-specific adaptations → Fork or PR

## Acknowledgments

Built on research from:
- Paul & Elder's Socratic questioning framework
- Spaced repetition research (SM-2 algorithm concepts)
- Zone of Proximal Development (Vygotsky)
- Patterns from [learn-faster-kit](https://github.com/hluaguo/learn-faster-kit) and [fluent](https://github.com/m98/fluent)

## License

MIT
