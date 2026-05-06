# Claude Skills

A personal collection of [Claude skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) — modular, on-demand instruction sets that extend Claude with specialized workflows for finance, education, document generation, and developer productivity.

Each skill is a folder containing a `SKILL.md` (with YAML frontmatter that tells Claude when to trigger it) plus any supporting files the workflow needs.

## Skills

### 📊 [`fundamentals`](./fundamentals)
**Trigger:** `/fundamentals [TICKER]`
Full interactive investment dashboard for any publicly traded company. Pulls financials, margins, free cash flow, valuation, DCF, SWOT, leadership, ESG, and political/lobbying exposure — every section scored 1–10. Pure fundamentals, no analyst-target reliance.

### 💡 [`investment-thesis`](./investment-thesis)
**Trigger:** any macro event, geopolitical conflict, commodity shock, or policy change ("how do I trade X", "what are the plays around Y").
Builds multilayer investment theories with causal chain diagrams, conviction ratings, risk profiles, and cross-asset analysis. Goes beyond first-order plays to map second- and third-order effects.

### 💰 [`roi-analyzer`](./roi-analyzer)
**Trigger:** ROI, business case, NPV, payback period, "is this worth it", "justify this spend".
Walks through a structured ROI conversation, then produces a professional editable Excel model. All assumptions exposed as blue-font inputs. Captures revenue, cost avoidance, savings, speed and accuracy gains against development, implementation, and ongoing costs (5% default discount rate).

### 📐 [`frd-generator`](./frd-generator)
**Trigger:** FRD, functional requirements, technical proposal, "research approaches for this problem", "design an architecture for this".
Produces a deep-research Functional Requirements Document. Researches the solution landscape (open source emphasis), compares approaches in a structured matrix, and proposes a modular architecture designed for future change.

### 🗺️ [`foodattractions`](./foodattractions)
**Trigger:** "top places in X", "best spots in X", "make me a map of X" for any city/destination.
Researched Google Maps location guide covering top 3 places per category (food, nightlife, entertainment, shopping, etc.). Cross-references TripAdvisor, Google Reviews, travel blogs, and YouTube vlogs.

### 🧮 [`1000mapmath6th`](./1000mapmath6th)
**Trigger:** `/1000mapmath6th` or any request to refresh a MAP-style 6th-grade math question bank.
Generates a 1000-question CSV in the schema consumed by a MAP Math practice app, distributed across 4 strands × 6 RIT bands × 4 formats. Mix of script-verified procedural arithmetic and Claude-authored word/geometry problems.

### ✂️ [`token-miser`](./token-miser)
**Trigger:** "be brief", "tl;dr", "no fluff", "save tokens", or any direct task-oriented question.
Forces shortest-correct-response mode. Strips preamble, hedging, restated context, and filler transitions. Every token has to earn its place.

## Repo layout

```
user-skills/
├── README.md
├── 1000mapmath6th/SKILL.md
├── foodattractions/SKILL.md
├── frd-generator/SKILL.md
├── fundamentals/SKILL.md
├── investment-thesis/SKILL.md
├── roi-analyzer/SKILL.md
└── token-miser/SKILL.md
```

## Using these skills

Skills live under `~/.claude/skills/` (Claude Code) or are uploaded via the Claude.ai UI. Drop any of these folders into your skills directory and Claude will pick them up automatically based on the trigger conditions in each `SKILL.md`'s `description` field.

For the official guide on authoring and deploying skills, see [Anthropic's Agent Skills documentation](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview).

## License

Personal-use. Adapt freely.
