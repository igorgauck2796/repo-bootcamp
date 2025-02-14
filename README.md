# Repo Bootcamp

<div align="center">

```
╦═╗╔═╗╔═╗╔═╗  ╔╗ ╔═╗╔═╗╔╦╗╔═╗╔═╗╔╦╗╔═╗
╠╦╝║╣ ╠═╝║ ║  ╠╩╗║ ║║ ║ ║ ║  ╠═╣║║║╠═╝
╩╚═╚═╝╩  ╚═╝  ╚═╝╚═╝╚═╝ ╩ ╚═╝╩ ╩╩ ╩╩
```

**Turn any GitHub, GitLab, or Bitbucket repository into a Day 1 onboarding kit**

[![GitHub Copilot SDK Contest Award](https://img.shields.io/badge/GitHub%20Copilot%20SDK-Contest%20Award%20Winner%20🏆-gold?style=for-the-badge&logo=github&logoColor=white)](https://github.com/features/copilot)

### 🏆 One of the Winners of the GitHub Copilot SDK Contest

[![Built with Copilot SDK](https://img.shields.io/badge/Built%20with-GitHub%20Copilot%20SDK-8957e5?logo=github&logoColor=white)](https://github.com/github/copilot-sdk)
[![CI](https://github.com/Arthur742Ramos/repo-bootcamp/actions/workflows/ci.yml/badge.svg)](https://github.com/Arthur742Ramos/repo-bootcamp/actions/workflows/ci.yml)
[![npm version](https://img.shields.io/npm/v/repo-bootcamp)](https://www.npmjs.com/package/repo-bootcamp)
[![npm downloads](https://img.shields.io/npm/dm/repo-bootcamp)](https://www.npmjs.com/package/repo-bootcamp)
[![npm provenance](https://img.shields.io/badge/npm-provenance-enabled-2ea44f?logo=npm)](https://docs.npmjs.com/generating-provenance-statements)
[![codecov](https://codecov.io/gh/Arthur742Ramos/repo-bootcamp/branch/main/graph/badge.svg)](https://codecov.io/gh/Arthur742Ramos/repo-bootcamp)
[![Node.js](<https://img.shields.io/badge/node-22.x%20(%3E%3D22.18)%20%7C%20%3E%3D24-brightgreen>)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-6.0-blue)](https://www.typescriptlang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[Features](#features) • [Quick Start](#quick-start) • [How It Uses Copilot SDK](#how-it-uses-the-github-copilot-sdk) • [Examples](#example-output)

</div>

---

<details>
<summary><b>Table of contents</b></summary>

- [The Problem](#the-problem) · [The Solution](#the-solution) · [Why This Tool Wins](#why-this-tool-wins)
- [How It Uses the GitHub Copilot SDK](#how-it-uses-the-github-copilot-sdk) · [Features](#features)
- [Example Output](#example-output) · [Generated Documentation](#generated-documentation)
- [Quick Start](#quick-start) · [Usage](#usage) · [CLI Options](#cli-options) · [Commands](#commands)
- [Programmatic API](#programmatic-api) · [Architecture](#architecture) · [How It Works](#how-it-works)
- [Configuration](#configuration) · [Development](#development) · [Requirements](#requirements)
- [Model Configuration](#model-configuration) · [Tech Stack](#tech-stack) · [Contributing](#contributing) · [License](#license)

</details>

---

## The Problem

New developers joining a project waste **days or weeks** trying to understand:

- How do I set up my environment?
- What's the architecture? Where do I start reading?
- What are safe first contributions?
- Who do I ask when I'm stuck?

Most READMEs are outdated. Most wikis are incomplete. Most senior devs are too busy.

## The Solution

**Repo Bootcamp** uses agentic AI to analyze repositories from GitHub, GitLab, or Bitbucket and generate comprehensive, actionable onboarding documentation in **under 60 seconds**.

```bash
npx repo-bootcamp https://github.com/facebook/react
```

That's it. You get 14+ interconnected markdown files covering everything a new contributor needs.

<div align="center">

https://github.com/Arthur742Ramos/repo-bootcamp/raw/main/media/demo-sonnet.mp4

_Generate comprehensive onboarding docs in under 60 seconds_

</div>

<details>
<summary><b>See CLI in action</b></summary>

```
  ╦═╗╔═╗╔═╗╔═╗  ╔╗ ╔═╗╔═╗╔╦╗╔═╗╔═╗╔╦╗╔═╗
  ╠╦╝║╣ ╠═╝║ ║  ╠╩╗║ ║║ ║ ║ ║  ╠═╣║║║╠═╝
  ╩╚═╚═╝╩  ╚═╝  ╚═╝╚═╝╚═╝ ╩ ╚═╝╩ ╩╩ ╩╩

  Turn any repo into a Day 1 onboarding kit

──────────────────────────────────────────────────
  Repository:  https://github.com/sindresorhus/ky
  Branch:      default
  Focus:       all
  Audience:    backend
  Style:       OSS (Community-friendly)
──────────────────────────────────────────────────

✔ Cloned sindresorhus/ky (branch: main)
✔ Scanned 45 files (12 key files read)

Detected Stack:
  Languages:  TypeScript
  Frameworks: None
  Build:      npm
  CI:         Yes
  Docker:     No

✔ Analysis complete

Security Score: 85/100 (B)
Onboarding Risk: 18/100 (A) 🟢

  ╔══════════════════════════════════════════════════════╗
  ║        ✓ Bootcamp Generated Successfully!            ║
  ╚══════════════════════════════════════════════════════╝

  📁 Output: ./bootcamp-ky/

  Generated files:
  ├── BOOTCAMP.md      → 1-page overview (start here!)
  ├── ONBOARDING.md    → Full setup guide
  ├── ARCHITECTURE.md  → System design & diagrams
  ├── CODEMAP.md       → Directory tour
  ├── FIRST_TASKS.md   → Starter issues
  ├── RUNBOOK.md       → Operations guide
  ├── DEPENDENCIES.md  → Dependency graph
  ├── SECURITY.md      → Security findings
  ├── RADAR.md         → Tech radar & risk score
  ├── IMPACT.md        → Change impact analysis
  ├── METRICS.md       → Codebase metrics & hotspots
  ├── HEALTH.md        → Onboarding-readiness health check
  ├── diagrams.mmd     → Mermaid diagrams
  ├── repo_facts.json  → Structured data
  ├── summary.json     → Scores & emitted files
  └── ANALYSIS_MANIFEST.json → Run metadata and evidence map

  🚀 Next step: open ./bootcamp-ky/BOOTCAMP.md
```

</details>

## Why This Tool Wins

| Traditional Approach            | Repo Bootcamp                     |
| ------------------------------- | --------------------------------- |
| Manual documentation takes days | Generate from repository evidence |
| Gets outdated immediately       | Regenerate anytime                |
| Inconsistent quality            | Structured, validated output      |
| Requires deep knowledge         | Works on any public repo          |
| Static documents                | Interactive Q&A mode              |
| No security insights            | Built-in security analysis        |

### What Makes It Different

1. **Powered by GitHub Copilot SDK** - Leverages the official SDK for agentic AI with tool-calling
2. **Truly Agentic** - Claude autonomously explores codebases, not just template filling
3. **Schema Validated** - All output is validated with Zod schemas and auto-retried on failures
4. **Validation** - Strict source and test typing, automated CLI and browser checks
5. **Full Feature Set** - A 22-command CLI: interactive Q&A, a combined scan dashboard, health/metrics/security scoring, coupling & impact graphs, machine preflight, ownership maps, cross-ecosystem task discovery, docs-drift analysis, guarded kit publishing, and a web UI
6. **Beautiful Output** - Mermaid diagrams, structured markdown, professional formatting

### By the Numbers

| Metric              | Value                                  |
| ------------------- | -------------------------------------- |
| Generated files     | 14+                                    |
| Unit configuration  | 3,201 passed, 8 skipped                |
| Source files        | 90 TypeScript files                    |
| Test files          | 137 unit / 51 CLI / 30 browser         |
| Source lines        | 28,369, including comments and blanks  |
| Languages supported | 10+                                    |
| Generation time     | Varies with repository, model and mode |

Inventory measured on 2026-10-12 from tracked files in this campaign. The unit
result is the complete local Windows run on Node 24; platform-dependent skips
can differ in CI. The unit and CLI configurations both include `test/e2e.test.ts`,
so their file counts overlap. Generation time has not been qualified with a fresh
live-model benchmark. See [release qualification](docs/release-qualification.md)
for the verification scope and the remaining release decisions.

## How It Uses the GitHub Copilot SDK

Repo Bootcamp is a showcase of the **GitHub Copilot SDK's agentic capabilities**. Here's how we leverage the SDK:

### Agentic Tool Calling

The SDK enables Claude to autonomously explore repositories using custom tools:

```typescript
import { CopilotClient } from "@github/copilot-sdk";

const client = new CopilotClient();

// Define tools the agent can use
const tools = [
  {
    name: "read_file",
    description: "Read contents of a file in the repository",
    parameters: { path: { type: "string" } },
  },
  {
    name: "list_files",
    description: "List files matching a glob pattern",
    parameters: { pattern: { type: "string" } },
  },
  {
    name: "search",
    description: "Search for text across the codebase",
    parameters: { query: { type: "string" } },
  },
];

// Agent autonomously decides which files to read
const session = await client.createSession({
  model: "claude-opus-4-5",
  systemMessage: { content: systemPrompt },
  tools,
  streaming: true,
});

await session.sendAndWait({ prompt: analysisPrompt });
```

### Why This Matters

| Traditional LLM Approach           | Copilot SDK Agentic Approach                  |
| ---------------------------------- | --------------------------------------------- |
| Dump entire codebase into context  | Agent selectively reads relevant files        |
| Context window limits scalability  | Works on repos of any size                    |
| Static, one-shot analysis          | Dynamic, multi-turn exploration               |
| No ability to search or drill down | Agent searches, reads, and follows references |

### Key SDK Features Used

1. **Multi-turn Conversations** - Agent iterates until it has enough information
2. **Tool Calling** - Custom tools for file reading, searching, and metadata
3. **Model Selection** - Automatic fallback through claude-opus-4-5 → claude-sonnet-4-5
4. **Streaming** - Real-time progress updates during analysis
5. **Schema Validation** - Zod schemas validate output, with auto-retry on failures

### Architecture Integration

```
┌─────────────────────────────────────────────────────────────┐
│                   GitHub Copilot SDK                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐  │
│  │   Claude    │  │   Tools     │  │   Streaming         │  │
│  │   Models    │  │   System    │  │   Responses         │  │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘  │
└─────────┼────────────────┼─────────────────────┼────────────┘
          │                │                     │
          ▼                ▼                     ▼
┌─────────────────────────────────────────────────────────────┐
│                    Repo Bootcamp Agent                       │
│                                                              │
│  "Read package.json" → "Search for test files" →            │
│  "Read src/index.ts" → "Find CI workflow" →                  │
│  "Generate structured onboarding JSON"                       │
└─────────────────────────────────────────────────────────────┘
```

The Copilot SDK transforms what would be a simple template-filler into an intelligent agent that understands code structure, identifies patterns, and produces genuinely useful onboarding documentation.

## Features

- **GitHub Copilot SDK Integration** - Built on the official SDK for agentic AI capabilities
- **Agentic Analysis** - Claude autonomously reads files, searches code, and understands architecture
- **Streaming LLM Output** - Streams assistant deltas live to terminal output (verbose) or progress callbacks
- **Multi-host Repository Support** - Works with GitHub, GitLab, and Bitbucket repository URLs
- **Complete Documentation Suite** - Generates 14+ interconnected markdown files
- **Smart Prioritization** - Intelligently samples files based on importance and byte budget
- **Fast File Walking** - Uses concurrent `fast-glob` traversal while honoring skip directories and file limits
- **Schema Validation** - Validates LLM output with auto-retry on failures
- **Model-aware Fast Mode Budgets** - Adjusts inline key-file/entrypoint budgets by selected model context window
- **Multi-language Support** - Works with TypeScript, Python, Go, Rust, Java, and more
- **Interactive Q&A Mode** - Chat with the codebase using natural language
- **Docs Drift Analyzer** - Detect stale/mismatched docs with `bootcamp docs --check`, and auto-fix with `--fix`
- **Phase-level Cache Management** - Reuses deps/security/impact analysis phases and supports `bootcamp cache list|prune|clear` (with `--json` listing for scripts)
- **Tech Radar** - Identify modern, stable, legacy, and risky technologies
- **Change Impact Analysis** - Understand how file changes affect the codebase
- **Codebase Metrics & Hotspots** - Deterministic `METRICS.md` with language breakdown, largest-file hotspots, test-to-source ratio, and an Approachability score (0-100 + grade)
- **Repo Health Check** - Deterministic `HEALTH.md` scoring onboarding-readiness across documentation, community, quality, and automation signals (0-100 + grade) with prioritized, actionable recommendations
- **Environment Doctor** - Diagnose Node, git, GitHub CLI/auth, mermaid-cli, and cache health with `bootcamp doctor` (`--json` for CI)
- **Combined Scan Dashboard** - `bootcamp scan` reports health, metrics, security, and onboarding risk from a single clone, with a `--check` CI gate on the lowest score
- **Module Coupling Map** - `bootcamp coupling` ranks modules by import coupling to reveal the load-bearing core, orchestrator hubs, and possibly-orphaned dead code
- **Circular Dependency Detection** - `bootcamp cycles` finds circular import groups (Tarjan SCC) on the import graph, with a `--check` CI gate
- **Machine Preflight** - `bootcamp preflight` checks your machine against the target repo's declared toolchain (Node, package manager, Python, Go) with a per-row remedy
- **Ownership Map** - `bootcamp owners` parses `CODEOWNERS` to answer "who do I ask?" with default owners, per-area maintainers, and top committers
- **Task Discovery** - `bootcamp tasks` answers "how do I build/test/run this?" deterministically across ecosystems (package.json scripts, Makefile, justfile, go-task Taskfile, docker-compose, pyproject/poetry, composer.json, qualifying Cargo manifests), grouped by category with a suggested getting-started sequence (`--json`, `--category`)
- **Style Pack Explorer** - `bootcamp styles` lists the built-in style packs and the doc sections each one enables
- **Version & PR Comparison** - Compare refs with `--compare` or analyze pull requests with `bootcamp diff`
- **Auto-Issue Creator** - Generate GitHub issues from starter tasks
- **Web Demo Server** - Beautiful browser UI for analyzing repositories
- **Template Packs** - Customize output style for different contexts
- **Diagram Rendering** - Convert Mermaid to SVG/PNG with mermaid-cli
- **Watch Mode** - Re-run analysis automatically when new commits are detected

Generated onboarding setup instructions preserve an explicit `install` command from the
analyzed quickstart. Without one, only npm, pnpm, Yarn, and Bun get a conventional install
command; other or unknown tools get guidance to the repository's README or contribution
guide. A package-manager label alone does not establish a runnable installation command.
Within the selected scan root, `poetry.lock` and `uv.lock` identify those Python workflows;
`requirements.txt` or a plain `pyproject.toml` retain the generic `pip` indication. This
does not parse TOML workflow configuration or establish whether Poetry or uv is used
without a lockfile. Poetry can also use standard `[project]` metadata.

Development, testing, and build/verify guidance uses semantic command names or recognized
simple script, task, and runner invocations. Dependency-group arguments and file paths
do not establish a command's role. Unknown or compound shell commands need an explicit
role name to appear in these steps; this is not a general shell parser.

Declared dotted tasks such as `build.prod` and `test.unit`, including colon namespaces,
can establish roles for package.json npm-family `run` commands (`run-script` for npm)
and Taskfile `task` commands when the literal target matches the declared task name.
Dotted leaf segments must be known role/setup words or `prod`; unknown qualifiers,
file extensions, paths and extra invocation arguments do not establish new dotted
roles. Make and Just guidance retains its existing behavior.

## Example Output

<details>
<summary><b>BOOTCAMP.md</b> - 1-page overview</summary>

```markdown
# sindresorhus/ky Bootcamp

> Tiny Fetch-based HTTP client with ergonomic helpers, retries, and hooks.

## Quick Facts

|                  |            |
| ---------------- | ---------- |
| **Languages**    | TypeScript |
| **Frameworks**   | None       |
| **Build System** | npm        |

## Quick Start

1. Install dependencies: npm install
2. Run tests: npm test
3. Build: npm run build

## If You Only Have 30 Minutes

1. Read this document
2. Run `npm install && npm test`
3. Pick a starter task from FIRST_TASKS.md
```

</details>

<details>
<summary><b>ARCHITECTURE.md</b> - System design with diagrams</summary>

```markdown
# Architecture

## Component Diagram

​`mermaid
graph TD
    A[ky.ts] --> B[Ky Class]
    B --> C[request]
    B --> D[retry logic]
    B --> E[hooks]
    C --> F[Response helpers]
​`

## Data Flow

Request → Options Merge → Hooks (before) → Fetch → Retry? → Hooks (after) → Response
```

</details>

<details>
<summary><b>FIRST_TASKS.md</b> - Starter issues by difficulty</summary>

```markdown
# First Tasks

## Beginner Tasks

### 1. Add README badge for Node.js version

- **Files:** README.md
- **Why:** Easy first contribution, improves documentation

### 2. Add test for edge case

- **Files:** test/main.ts
- **Why:** Improves test coverage, low risk

## Intermediate Tasks

### 3. Improve TypeScript types for hooks

- **Files:** source/types/hooks.ts
- **Why:** Better DX, teaches you the hook system
```

</details>

## Generated Documentation

| File                     | Description                                                          |
| ------------------------ | -------------------------------------------------------------------- |
| `BOOTCAMP.md`            | 1-page overview - start here!                                        |
| `ONBOARDING.md`          | Complete setup guide with commands                                   |
| `ARCHITECTURE.md`        | System design with Mermaid diagrams                                  |
| `CODEMAP.md`             | Directory tour for navigation                                        |
| `FIRST_TASKS.md`         | 8-10 starter issues by difficulty                                    |
| `RUNBOOK.md`             | Operations guide (for services)                                      |
| `DEPENDENCIES.md`        | Dependency graph and analysis                                        |
| `SECURITY.md`            | Security patterns and findings                                       |
| `RADAR.md`               | Tech radar and onboarding risk score                                 |
| `IMPACT.md`              | Change impact analysis for key files, plus any circular dependencies |
| `METRICS.md`             | Codebase metrics, hotspots & approachability score                   |
| `HEALTH.md`              | Onboarding-readiness health score & recommendations                  |
| `DIFF.md`                | Version comparison (with `--compare`)                                |
| `diagrams.mmd`           | Mermaid diagram sources                                              |
| `repo_facts.json`        | Structured data for automation                                       |
| `summary.json`           | Scores and the local files emitted by this run                       |
| `ANALYSIS_MANIFEST.json` | Reproducibility metadata, scan coverage, and evidence sources        |

Optional reports depend on the selected style and available analysis. BOOTCAMP's
generated Next Steps links include only documents in the assembled kit, including
output exclusions and formatter removals. Explicit reposit