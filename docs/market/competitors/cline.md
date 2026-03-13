# Cline

## Company Overview

Created by Saoud Rizwan as a 2024 hackathon project (originally "Claude Dev"; package.json still references `claude-dev`). Based in Sacramento, CA. Raised $32M combined Seed + Series A (Jul 2025) led by Emergence Capital and Pace Capital. Apache 2.0 license. 50K+ GitHub stars, 5M+ VS Code installs, ~20K Discord members. GitHub's Octoverse 2025 crowned it the fastest-growing AI open source project by contributors (4,704% YoY growth). Enterprise customers include Samsung and SAP.

## Product/Service Offering

### Core Architecture

VS Code and JetBrains extension acting as an autonomous coding agent. Plan/Act dual-mode workflow: the agent first proposes an approach (Plan), then executes file edits, terminal commands, and browser actions (Act), with human approval gates at each step. Model-agnostic -- supports OpenAI, Anthropic, Google, local models via Ollama, and mid-task model switching.

### CLI and Multi-Agent

Cline CLI 2.0 (Feb 2025) rebuilt the agent for the terminal: stdin/stdout piping, `-y` flag for full autonomy, CI/CD compatible. Evolved into a standalone service powered by Cline Core, exposing a gRPC API for scriptable automation and multi-instance orchestration. Subagents spawn focused research agents in parallel, each with its own prompt and context window, returning reports to the main agent. IDE Cline can delegate to CLI subagents for fresh context windows. Multiple CLI processes can run in parallel across folders, branches, or concerns, orchestrated via shell, tmux, or CI.

### Governance and Rules

`.clinerules/` directory at project root provides hierarchical rule injection into the system prompt. Supports `.md` and `.txt` files, togglable per-file in the UI. Separates technical rules (`.clinerules/`) from business context (Cline Docs). Global rules apply across all projects from a system-level directory. Hooks (macOS/Linux) inject custom scripts at workflow moments to validate operations, monitor usage, and shape decisions. Enterprise adds RBAC, centralized policy enforcement, and OpenTelemetry-based audit trails with JSON output for custom dashboards.

### Ecosystem

MCP integration with 3,000+ servers; can self-generate MCP servers. Own MCP marketplace. Skills system for reusable agent instructions. Jupyter Notebook cell-level editing. Browser automation (headless). Checkpoints and diff review. Built-in websearch tooling.

### Enterprise

SSO (SAML/OIDC), SCIM, global policies, VPC/private link deployment, self-hosted option. OpenTelemetry export to Datadog/Grafana/Splunk. Cost breakdown by project, model performance comparison, and selective audit logging.

## Pricing Strategy

| Tier | Cost | Details |
|------|------|---------|
| Individual | Free | BYOK, pay provider directly, no markup |
| Teams | Free through Q1 2026, then free up to 10 seats | $20/user/mo beyond 10 seats; JetBrains, RBAC, centralized billing |
| Enterprise | Custom | SSO, SCIM, VPC, self-hosted, audit trails |

The BYOK model means developers pay exact provider rates with zero markup. The extension tracks total tokens and cost per task and per request. Rule of thumb from community data: if you spend over ~$40/month on API tokens, a subscription tool may be cheaper; below that, BYOK wins. Heavy Claude usage can reach $50/day or $200/month.

## Marketing & Messaging

"Open source and uncompromised." "Human in the loop every step." "Your infrastructure, your inference." Privacy-first positioning. Contrasts against subscription tools with markup. Emphasizes cost transparency, provider independence, and the fact that the free tier has no artificial capability limits.

## Market Perception

### Strengths

- Strong cross-file reasoning and complex workflow handling (CI/CD pipelines, database migrations)
- Community trust through full Apache 2.0 source availability; strongest forks (Roo Code, Kilo Code) validate the architecture
- Model flexibility is unmatched -- any provider, any model, mid-task switching
- MCP ecosystem leadership (3,000+ servers, own marketplace)
- gRPC-based CLI enables headless automation and multi-agent orchestration that IDE-only tools cannot match
- Cost transparency appeals to budget-conscious teams and solo developers
- Rapid feature cadence: Gemini 3, GPT-5.1, Opus 4.6, Hooks, Skills, SDK API all shipped 2025-2026

### Weaknesses

- Raw API costs are the user's problem -- steep for heavy usage, and weaker models degrade quality significantly
- Setup friction: BYOK config, model selection, and rule authoring reward deliberate users and frustrate those wanting a one-click experience
- Slower execution than Cursor or Copilot on simple tasks due to approval gates (~90s vs 45-60s on component generation benchmarks)
- Innovation pace sometimes trails its own forks (Roo Code, Kilo Code iterate faster on niche features)
- Browser automation struggles with heavy SPAs
- Step-by-step execution lacks automatic re-verification; no built-in retry loop on failure

### Competitive Position

- vs **Cursor**: Cline offers model freedom and no subscription lock-in, but Cursor provides a faster, more integrated IDE experience and better inline completion. Cursor's June 2025 shift to usage-based credits caused community backlash, partially validating Cline's transparency approach.
- vs **Claude Code**: Claude Code's Agent Teams offer deeper multi-agent coordination. Cline counters with model agnosticism and IDE integration. Claude Code is terminal-native; Cline bridges IDE and terminal via gRPC.
- vs **Copilot**: Copilot wins on enterprise ecosystem integration (GitHub-native) and low entry price ($10/mo). Cline wins on autonomy, agentic depth, and open source governance.

## Sources

- [GitHub repository](https://github.com/cline/cline)
- [Website](https://cline.bot/)
- [Pricing](https://cline.bot/pricing)
- [CLI 2.0 announcement](https://devops.com/cline-cli-2-0-turns-your-terminal-into-an-ai-agent-control-plane/)
- [$32M funding](https://www.globenewswire.com/news-release/2025/07/31/3125274/0/en/Cline-Raises-32M-in-Seed-and-Series-A-Funding-to-Bring-Agentic-AI-Coding-to-Enterprise-Software-Teams.html)
- [Cline Rules docs](https://docs.cline.bot/customization/cline-rules)
- [Subagents docs](https://docs.cline.bot/features/subagents)
- [Cline CLI & Core architecture](https://cline.bot/blog/cline-cli-my-undying-love-of-cline-core)
- [Enterprise overview](https://cline.bot/blog/introducing-cline-for-enterprise)
- [Cline review 2026](https://vibecoding.app/blog/cline-review-2026)
- [Kilo Code vs Roo Code vs Cline comparison](https://ai505.com/kilo-code-vs-roo-code-vs-cline-the-2026-ai-coding-battle-nobody-saw-coming/)
- [Best AI Coding Agents 2026 (Faros AI)](https://www.faros.ai/blog/best-ai-coding-agents-2026)
- [Cline vs Cursor vs Copilot](https://designrevision.com/blog/cline-vs-cursor-vs-github-copilot)
- [BYOK economics](https://cline.bot/blog/the-real-economics-of-ai-development-why-clines-transparent-token-based-approach-delivers-superior-results-2)
