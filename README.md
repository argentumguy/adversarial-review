# adversarial-review

A universal, self-adapting adversarial audit protocol for AI coding agents. Detects architectural flaws, race conditions, bottlenecks, vulnerabilities, and contract breaches before code is written or deployed.

Works on any technology stack. No hardcoded assumptions about languages, frameworks, or infrastructure.

---

## What This Skill Does

This skill instructs AI coding agents to run rigorous adversarial audits on any codebase, plan, or architecture. The auditor:

1. Discovers the repository environment autonomously (Phase 0).
2. Projects 7 universal failure axes onto the detected profile.
3. Activates dynamic lenses based on the specific technologies found.
4. Iterates through detection, mitigation, and revalidation cycles until mathematical convergence ($\Delta = 0$).

The audit is strictly read-only. The auditor never modifies source code during the analysis.

---

## Features

| Feature | Description |
|:---|:---|
| **Autonomous environment detection (Phase 0)** | Inspects manifests, dependencies, infrastructure files, and entry points. Adapts to any stack without manual setup. |
| **7 universal failure axes** | Mathematical limits, concurrency, temporal dynamics, performance, external failures, contract rigidity, and business invariants. |
| **Dynamic lens generator** | Activates context-specific audit lenses based on the detected profile. Replaces fixed technology-specific checklists. |
| **Formal convergence metric** | Uses $\Delta = \text{Count(Sev1)} + \text{Count(Sev2)}$ with a target of $\Delta = 0$. |
| **Anti-oscillation guard** | Detects decision flip-flopping between passes and escalates trade-offs to the user. |
| **Secrets detection guard** | Identifies hardcoded credentials, obfuscates them immediately, and alerts the user. |
| **UNVERIFIED findings category** | Tracks suspected defects that cannot be verified deterministically, without inflating the convergence metric. |
| **Configurable cadence** | Step-by-step with user confirmation (default) or continuous autonomous execution. |
| **Required testability** | Every mitigation must include an automated test specification. |
| **Required rollback strategy** | Every design must include a production rollback plan. |
| **Non-regression revalidation** | Re-checks all previously passing axes after each correction. |
| **Abuse and misuse lens** | Detects legitimate feature exploitation vectors (mass exfiltration, retry amplification, transactional spam). |
| **Development remnants lens** | Detects `localhost` references, mock data, staging URLs, test credentials, and debug flags left in production code. |
| **Scope partitioning guard** | Decomposes broad repository audits into sequential module sub-audits to prevent diluted passes. |
| **Mandatory call-trace proof** | Requires a complete execution path from entry point to vulnerable line for every reported defect. |
| **Core business transaction trace** | Verifies end-to-end domain state transitions, data transformations, and business invariants. |
| **Mandatory challenger pass** | Stress-tests proposed mitigations under active attack conditions before certifying convergence. |
| **Self-audit capability (meta-recursion)** | The skill can audit its own instructions using the same protocol. |

---

## Installation

This skill operates as a standard markdown protocol. It works across any AI coding agent, IDE, or CLI tool.

### Cursor

Add the skill to your project rules:
```bash
# place inside cursor rules directory
mkdir -p .cursor/rules
cp adversarial-review/SKILL.md .cursor/rules/adversarial-review.mdc
```
Alternatively, include the contents of `SKILL.md` in `.cursorrules`.

### OpenAI Codex / GitHub Copilot

Add the protocol to your repository instructions:
```bash
# append or link into copilot instructions
cat adversarial-review/SKILL.md >> .github/copilot-instructions.md
```

### Claude Code

Install the skill into your user skills directory:
```bash
cp -r adversarial-review ~/.claude/skills/
```

### Antigravity / Gemini CLI

Install into your global or workspace skills directory:
```bash
# global configuration (all workspaces)
cp -r adversarial-review ~/.gemini/config/skills/

# workspace-local configuration
cp -r adversarial-review .agents/skills/
```

### Universal Setup (Any AI Agent)

Place `SKILL.md` (or `SKILL.es.md`) in the instructions folder of your agent. You can also reference the file directly from your base instructions (`AGENTS.md`, `CLAUDE.md`, or system prompt).

---

## Usage

Ask your AI coding agent:

> "Run an adversarial review."

The agent will:

1. Present the initialization interview (scope, rigor mode, cadence).
2. Execute Phase 0 (autonomous environment detection).
3. Alert you immediately if hardcoded secrets are found.
4. Audit across 7 axes and activated dynamic lenses.
5. Iterate until $\Delta = 0$ or the Pass 5 hard stop is reached.
6. Issue a Zero Defects Certificate or escalate unresolved conflicts.

### Audit Modes

| Mode | When to use |
|:---|:---|
| **Quick Sweep** | Small scripts, isolated functions, or scoped changes. Single pass. |
| **Recursive Convergence** | Technical plans, structural changes, concurrency or security modules. Iterates until $\Delta = 0$. |

### Cadence Options

| Cadence | Behavior |
|:---|:---|
| **Step by step (default)** | Pauses after each pass. Waits for user confirmation to continue. |
| **Continuous autonomous** | Runs all passes without interruption until convergence or hard stop. |

---

## Available Languages

| File | Language |
|:---|:---|
| `SKILL.md` | English |
| `SKILL.es.md` | Spanish (Español) |

Both versions contain identical protocol logic.

---

## How It Compares

| Feature | This Skill | awdemos/adversarial-review | production-audit |
|:---|:---:|:---:|:---:|
| Autonomous stack detection (Phase 0) | Yes | No | Partial |
| Dynamic lenses (not hardcoded) | Yes | No | No |
| Formal convergence metric ($\Delta = 0$) | Yes | No | No |
| Anti-oscillation guard | Yes | No | No |
| User calibration interview | Yes | No | No |
| Configurable cadence | Yes | No | No |
| Secrets guard with notification | Yes | No | No |
| Required testability (Axis 6) | Yes | No | No |
| Required rollback strategy (Axis 7) | Yes | No | No |
| Non-regression revalidation | Yes | No | No |
| UNVERIFIED findings category | Yes | Yes | No |
| Self-audit (meta-recursion) | Yes | No | No |
| Formal report persistence | Yes | No | No |
| Plausibility filter | Yes | No | No |
| Output templates with diff + test | Yes | Partial | No |
| Abuse/Misuse dynamic lens | Yes | Yes (fixed) | Yes (fixed) |
| Development remnants lens | Yes | No | Yes (fixed) |
| Scope partitioning guard | Yes | No | No |
| Mandatory call-trace proof | Yes | Partial | No |
| Core business transaction trace | Yes | No | No |
| Mandatory challenger pass | Yes | No | No |

---

## Contributing

Contributions are welcome. Open an issue or submit a pull request.
Please write documentation and pull request descriptions following the ASD-STE100 English standard.

---

## License

MIT License. See [LICENSE](LICENSE) for details.
