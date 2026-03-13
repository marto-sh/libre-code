# Competitor Landscape: AI Coding Agents

Deep-dive analyses are in the individual files alongside this README.

## Direct Competitors

Terminal-first or editor-based AI coding agents targeting professional developers.

### Proprietary

| Name | Maker | Form Factor | Pricing | Key Trait |
|------|-------|-------------|---------|-----------|
| [Claude Code](claude-code.md) | Anthropic | Terminal | $20–200/mo | Deepest reasoning, 200K context |
| [Cursor](cursor.md) | Cursor Inc | VS Code fork | $20–200/mo | Most polished IDE experience |
| [Windsurf](windsurf.md) | Codeium/Cognition | VS Code fork | $15/mo+ | Cheaper Cursor alternative, strong inline completion |
| [Kiro](kiro.md) | AWS | VS Code fork | Free–$200/mo | Spec-driven development, Agent Hooks |
| [Amp](amp.md) | Sourcegraph | Terminal + editor | Credit-based | Persistent threads, subagent parallelization, server-stored sessions |

### Open Source

| Name | License | Form Factor | Model Access | Key Trait |
|------|---------|-------------|--------------|-----------|
| [Codex CLI](codex-cli.md) | Apache 2.0 | Terminal (Rust) | OpenAI (BYOK) | Sandboxed, ties into ChatGPT subscription |
| [Gemini CLI](gemini-cli.md) | Apache 2.0 | Terminal | Google (free tier) | 1M context, generous free tier (1000 req/day) |
| [Aider](aider.md) | Apache 2.0 | Terminal | BYOK (any provider) | Git-first, automatic staging/commits, model-agnostic |
| [OpenCode](opencode.md) | MIT | Terminal | 75+ providers, local | Mid-session model switching, privacy-focused |
| [Cline](cline.md) | Apache 2.0 | VS Code + headless CLI | BYOK | Subagents, audit trail, governance |
| [Goose](goose.md) | Apache 2.0 | Terminal + desktop | BYOK | Extensible, operational tasks beyond code |
| [Plandex](plandex.md) | MIT | Terminal | BYOK | 2M token context, large project focus (cloud winding down) |

## Indirect Competitors

Solve related problems with a different approach or focus.

| Name | Maker | Differentiator |
|------|-------|----------------|
| [GitHub Copilot](github-copilot.md) | Microsoft | Dominant install base, IDE autocomplete + agent mode, $10–39/mo |
| [Augment Code](augment-code.md) | Augment | 400K file context engine, multi-model routing, code review agent |
| [Devin](devin.md) | Cognition | Fully autonomous (runs hours/days), 15% complex task success, $20/mo+ |
| [Qodo](qodo.md) | Qodo (ex-Codium) | Quality-focused: multi-agent code review, test gen, AI governance rules |
| [Codegen](codegen.md) | ClickUp (acquired) | Infrastructure layer for deploying/orchestrating agents at scale (deprecated) |

## Adjacent (Different Market)

AI app builders targeting non-developers — not direct competitors but part of the broader "AI builds software" space.

| Name | Target Audience |
|------|-----------------|
| [Lovable](lovable.md) | Non-developers building apps via natural language |
| [Bolt](bolt.md) | Non-developers, rapid prototyping |
| [v0](v0.md) | Designers/non-developers generating UI components |
| [Replit Agent](replit-agent.md) | Browser-based, targets non-traditional developers |
