<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="logo-light.svg">
    <img alt="learn-codebase — anti-vibe coding" src="logo-light.svg" width="480">
  </picture>
</p>
<p align="center">
  <strong>The anti-vibe-coding skill.</strong> A Socratic tutor that teaches you codebases
  through questioning and active recall — because on mature projects,
  understanding matters more than speed.
</p>
<hr>
<p align="center">
  <a href="https://skills.sh/ktaletsk/learn-codebase/learn-codebase"><img src="https://skills.sh/b/ktaletsk/learn-codebase" alt="skills.sh"></a>
</p>

For onboarding to a large repo, preparing a PR, or working on legacy code without pretending you understand it.
On mature projects, understanding matters more than speed.


## Try It in 2 Minutes

1. Install the skill with [`npx skills`](https://www.npmjs.com/package/skills) (see [Installation](#installation) for options)
2. Open any project you want to understand
3. Start a session with `/learn-codebase`

Example (install once for all projects, then open a repo):

```bash
npx skills add ktaletsk/learn-codebase -g
cd /path/to/repo-you-want-to-learn
# then in your AI agent:
/learn-codebase
```

What happens next:
- it asks what you're trying to learn
- it makes you predict before revealing answers, so you can't skim past a gap
- it keeps a learning journal in `.claude/learning-journal.md` that tracks what you confidently know vs. what you're still bluffing
- it helps you build a mental model that survives after the chat ends

> **Did it click?** If this helped you actually understand a codebase, [share your story](https://github.com/ktaletsk/learn-codebase/issues/new?title=Story:+&labels=show+%26+tell&body=What+codebase+were+you+learning%3F%0AWhat+clicked+that+hadn%27t+before%3F%0AAnything+surprising+about+the+experience%3F) — and [star the repo](https://github.com/ktaletsk/learn-codebase) if you found it useful.

## Who This Is For

**Great fit for:**
- engineers onboarding to an unfamiliar or mature codebase
- open source contributors preparing their first meaningful PR
- developers and students who want to understand code, not just generate it
- people debugging or refactoring systems they did not write
- anyone willing to say "I don't actually know" out loud instead of nodding along

**Probably not for:**
- greenfield prototyping where speed matters more than depth
- "just give me the patch" workflows
- people who want AI to answer immediately without pushback
- anyone who wants the feeling of understanding without the work of it

## Why This Exists

AI coding tools make it easy to ship code you don't understand — and, worse,
easy to *feel* like you understand it. That works for greenfield projects.
On a mature codebase with real quality standards, "it works on my machine"
is how you write a PR you can't defend in review.

This skill is the friction you opted out of when you started vibe-coding.
It flips the default AI interaction model:

| | Regular AI Coding | learn-codebase |
|---|---|---|
| Shows code immediately | ✅ | ❌ Asks you to predict first |
| Answers your questions | ✅ | ❌ Asks clarifying questions back |
| Optimizes for speed | ✅ | ❌ Optimizes for retention |
| Forgets between sessions | ✅ | ❌ Maintains learning journal |
| Makes you dependent | 😬 | ❌ Builds your independence |

## The Problem

You know that feeling after heavy AI-assisted coding — like swimming with fins,
then taking them off? The skill atrophy is real, but that's the smaller problem.
The bigger one is the gap between what you think you know and what you can
actually defend.

A 2025 study found developers using AI on familiar codebases were 19% *slower*
than those without AI, yet believed they were 20% faster. That 39-point delta
is the cost of not being honest with yourself.

**This skill is for when you need to actually learn**, not just feel productive:
- Onboarding to a new team's codebase
- Preparing to contribute to open source
- Understanding legacy code before refactoring
- Building confidence before code review — the earned kind, not the vibes kind

## Battle-Tested

Tested on a popular open-source project (5M+ monthly downloads, large TypeScript monorepo).

**Starting point:** needed to contribute to the upload flow, but did not yet have a reliable mental model of the architecture.

**What the skill did:**
- asked for predictions before showing code
- surfaced a misunderstanding around `AbortController`
- kept the discussion at the architecture level before diving into files
- recorded progress in the learning journal for the next session

**Result after ~30 minutes:**
- 2 concepts moved from 🔴 to 🟡
- 1 aha moment captured
- full upload flow traced independently in the learner's own words
- confidence shifted from "I can maybe poke at this" to "I can implement without faking understanding"

### What It Looks Like in Practice

| Scenario | Regular AI agent | learn-codebase |
|----------|---------------------|----------------|
| "How does upload work?" | Shows full code dump | "What do you *expect* `upload()` to return?" |
| User doesn't know AbortController | Assumes knowledge or over-explains | Detects gap, explains simply, returns to questions |
| Complex architecture | "Here are 5 files to read" | "Conceptually it's three layers: UI, Model, Services" |
| Session end | "Let me know if you need anything else" | "Here are 4 concrete options for next steps" |
| Next session | Starts fresh | Reads journal: "Last time you explored upload flow..." |

## Why not just use your agent the usual way?

Most coding agents are tuned to **finish the task**: ship the answer, unblock you, move on. This skill is tuned to **leave you able to explain what you shipped** — different objective, different friction. You still use the same agent; you add a mode that resists false fluency.

| | Generic coding agent | learn-codebase |
|---|---|---|
| Default behavior | Answers quickly | Pushes you to think first |
| Main optimization | Task completion | Mental model formation |
| During confusion | Tends to smooth over it | Uses confusion as a teaching signal |
| Across sessions | Often starts fresh | Compounds understanding in a journal |
| Long-term effect | Faster now, often shallower later | Slower now, more independent later |

If you already know the repo and just need a patch fast, use the normal agent flow. This skill is for the part before that, when false confidence is expensive — the stage where you can still admit "I don't know yet" before it ossifies into "I'd better not ask."

## How It Works

The skill uses proven pedagogical techniques:

- **Socratic questioning** — Asks you to explain before explaining to you
- **Prediction before revelation** — You predict behavior before seeing it  
- **Active recall** — Quizzes you on what you've learned
- **Spaced repetition** — Schedules reviews at optimal intervals
- **Zone of Proximal Development** — Calibrates difficulty to your level
- **Persistent learning journal** — Tracks understanding across sessions

## Installation

The default path is the **Skills CLI** (`npx skills`): it pulls this repo from GitHub and installs into the right agent skill directories for Cursor and many other AI coding agents. You need [Node.js](https://nodejs.org/) so `npx` is available.

### Recommended: `npx skills`

**All projects (global / user-level):**

```bash
npx skills add ktaletsk/learn-codebase -g
```

**This repository only (from inside the project):**

```bash
npx skills add ktaletsk/learn-codebase
```

Use `-a <agent>` to target specific agents (e.g. `-a cursor`), or run without it and follow the prompts. To update later: `npx skills update` (add `-g` for global installs). More skills: [skills.sh](https://skills.sh/).

### Manual: `git clone`

If you prefer to place the skill yourself:

**Personal skill (all projects)**

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/ktaletsk/learn-codebase ~/.claude/skills/learn-codebase
```

**Project skill (specific project)**

```bash
mkdir -p .claude/skills
git clone https://github.com/ktaletsk/learn-codebase .claude/skills/learn-codebase
```

## Usage

Start a learning session:

```
/learn-codebase
```

Helpful first prompts:
- "Help me understand the architecture before I touch anything"
- "I want to prepare a PR in this part of the repo, but I don't want to fake it in review"
- "Quiz me as we go, don't just explain — call me out when I hand-wave"
- "I need to understand this legacy module well enough to refactor it without guessing"

## Turn Off Answer Suggestions

Claude Code shows grayed-out "prompt suggestions" in the input box, pre-filling what you might say next. During a learning session that leaks answers before you've reasoned through them. It's a CLI feature the skill can't disable for you, so turn it off yourself:

- Run `/config` and disable **Prompt Suggestions**, or
- Launch with `CLAUDE_CODE_ENABLE_PROMPT_SUGGESTION=false claude` (read at startup only).

The skill reminds you of this once per project.

## Example Session

```
You: /learn-codebase

Agent: I don't see a learning journal yet—let's set one up.

What's your goal with this codebase? Are you:
- Contributing new features
- Fixing bugs
- Doing code review
- General exploration

You: I want to contribute to the file browser module

Agent: Good, concrete goal. Before we dive in, what's your familiarity 
with the overall architecture? Have you worked with this codebase before?

You: I know it's TypeScript and uses Lumino widgets, but I'm new to the code

Agent: Perfect starting point. Looking at the directory structure, 
where do you *expect* file browser code to live?

You: Maybe `packages/filebrowser` or something like that?

Agent: Good instinct — it's actually `packages/filebrowser-extension` 
and `packages/filebrowser`. Before I show you the difference, why do 
you think they split it into two packages?

You: Hmm... maybe one is the core logic and one is the JupyterLab plugin?

Agent: 🎯 Exactly. Now let's trace what happens when a user clicks 
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
- Example journals or anonymized transcripts showing good learning flows

Good first contribution ideas:
- framework-specific concept primers
- repo walkthrough examples
- tighter compatibility notes for other AI agent environments
- clearer demo transcripts for the README

## Acknowledgments

Built on research from:
- Paul & Elder's Socratic questioning framework
- Spaced repetition research (SM-2 algorithm concepts)
- Zone of Proximal Development (Vygotsky)
- Patterns from [learn-faster-kit](https://github.com/hluaguo/learn-faster-kit) and [fluent](https://github.com/m98/fluent)

## Compatibility

This skill uses the open [Agent Skills](https://agentskills.io) standard.

**Tested:**
- Claude Code (`~/.claude/skills/`)

**Expected to work with compatible Agent Skills environments, but not fully validated here:**
- Cursor (`.cursor/skills/`) — `npx skills add` can target Cursor with `-a cursor`
- VS Code, GitHub Copilot, and other compatible agents

## Support This Project
If you liked this skill, consider supporting to build more cool things in the future:
[![Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/orbrx)

## License

MIT
