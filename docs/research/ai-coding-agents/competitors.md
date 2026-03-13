# Competitor Landscape: AI Coding Agents

## Direct Competitors

Terminal-first or editor-based AI coding agents targeting professional developers.

### Proprietary

| Name | Maker | Form Factor | Pricing | Key Trait |
|------|-------|-------------|---------|-----------|
| Claude Code | Anthropic | Terminal | $20–200/mo | Deepest reasoning, 200K context |
| Cursor | Cursor Inc | VS Code fork | $20–200/mo | Most polished IDE experience |
| Windsurf | Codeium/Cognition | VS Code fork | $15/mo+ | Cheaper Cursor alternative, strong inline completion |
| Kiro | AWS | VS Code fork | Free (preview) | Spec-driven development, Agent Hooks |
| Amp | Sourcegraph | Terminal + editor | Credit-based | Persistent threads, subagent parallelization, server-stored sessions |

### Open Source

| Name | License | Form Factor | Model Access | Key Trait |
|------|---------|-------------|--------------|-----------|
| Codex CLI | Open source | Terminal (Rust) | OpenAI (BYOK) | Sandboxed, ties into ChatGPT subscription |
| Gemini CLI | Apache 2.0 | Terminal | Google (free tier) | 1M context, generous free tier (1000 req/day) |
| Aider | Apache 2.0 | Terminal | BYOK (any provider) | Git-first, automatic staging/commits, model-agnostic |
| OpenCode | Open source | Terminal | 75+ providers, local | Mid-session model switching, privacy-focused |
| Cline | Apache 2.0 | VS Code + headless CLI | BYOK | Subagents, audit trail, governance |
| Goose | Open source | Terminal + desktop | BYOK | Extensible, operational tasks beyond code |
| Plandex | Open source | Terminal | BYOK | 2M token context, large project focus (cloud winding down) |

## Indirect Competitors

Solve related problems with a different approach or focus.

| Name | Maker | Differentiator |
|------|-------|----------------|
| GitHub Copilot | Microsoft | Dominant install base, IDE autocomplete + agent mode, $10–39/mo |
| Augment Code | Augment | 400K file context engine, multi-model routing, code review agent |
| Devin | Cognition | Fully autonomous (runs hours/days), 15% complex task success, $500/mo |
| Qodo | Qodo (ex-Codium) | Quality-focused: multi-agent code review, test gen, AI governance rules |
| Codegen | Codegen | Infrastructure layer for deploying/orchestrating agents at scale |

## Adjacent (Different Market)

AI app builders targeting non-developers — not direct competitors but part of the broader "AI builds software" space.

| Name | Target Audience |
|------|-----------------|
| Lovable | Non-developers building apps via natural language |
| Bolt | Non-developers, rapid prototyping |
| v0 (Vercel) | Designers/non-developers generating UI components |
| Replit Agent | Browser-based, targets non-traditional developers |
