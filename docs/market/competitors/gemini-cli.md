# Gemini CLI

## Company Overview

Google product, launched Jun 25, 2025. Apache 2.0 license. Built in TypeScript/Node.js, distributed via npm. Gained 17,000 GitHub stars within the first 24 hours. Follows a weekly preview + stable release cadence (v0.33.0 stable / v0.34.0-preview as of Mar 2026). Over 13,800 GitHub issues filed, indicating high adoption but also significant friction.

## Product/Service Offering

Terminal-native agent wrapping Gemini model family (2.5 Pro, 3.0 Pro Preview, 3.1 Pro Preview) with a 1M token context window.

**Core capabilities:** file operations, shell commands, web fetching, MCP support, headless/scripting mode, GitHub Actions integration, Google Search grounding (live web search during sessions -- unique among terminal agents).

**Architecture:** multi-layered sandboxing system supporting macOS Seatbelt (kernel-enforced .sb profiles), Docker/Podman containers (auto-removed on exit), gVisor (`runsc` runtime for kernel isolation), and experimental LXC/LXD (full Linux system containers). This is the most extensive sandboxing story of any competitor.

**MCP support:** configured via `~/.gemini/settings.json`. MCP tools are discovered at startup, validated against the Gemini API, and registered in a global tool registry with conflict resolution. FastMCP integration (v2.12.3+) enables `fastmcp install gemini-cli` for Python-based servers. Supports rich content types (text + binary) per MCP spec.

**Recent additions (2026):** Plan Mode (enabled by default in v0.34.0), research subagents, experimental browser agent for web page interaction, A2A (Agent-to-Agent) remote agent support with HTTP auth, project-level policy engine with MCP server wildcards, tracker visualization tools.

**GEMINI.md:** equivalent of CLAUDE.md for project-level instructions.

## Pricing Strategy

| Tier | Cost | Model Access | Limits |
|------|------|--------------|--------|
| Free | $0 (Google account) | Gemini model family (CLI-determined) | 60 req/min, 1,000 req/day, 1M context |
| API Key (free) | $0 | Flash only | Standard API rate limits |
| Google AI Pro | $19.99/mo | Higher daily limits | Pro-tier quotas for CLI + Code Assist + Jules |
| Google AI Ultra | $249.99/mo | Highest daily limits | 30TB storage, enterprise features |
| Pay-as-you-go | Per-token | Full model selection | Standard Gemini API rates |

**Quota reality:** Dec 7, 2025 quota tightening reduced Gemini 2.5 Pro free tier to 5 RPM / 25 RPD -- effectively one request every 12 seconds, ~2 hours of active development before daily exhaustion. Widespread 429 errors reported. The generous "1,000 req/day" headline applies to the CLI-selected model (often Flash), not necessarily Pro.

**Silent fallback:** CLI falls back from Pro to Flash after 2+ slow responses or when Pro quota is exhausted. GitHub issues document fallback happening as early as 2-3 prompts into a session. Users report this is not clearly communicated.

## Marketing & Messaging

"Developers live in the terminal, not chat windows." The free tier is framed as "actually free, not artificially limited." The 1M context window is positioned as "entire repository in a single prompt." Apache 2.0 license emphasized for auditability and trust. Google Search grounding marketed as a differentiator no competitor can match (access to live web during coding). Recent messaging emphasizes the sandboxing story and Plan Mode for structured agentic workflows.

## Market Perception

### Strengths

- Most generous free tier headline (1,000 req/day, 1M context) -- strongest zero-cost entry point
- 1M token context is a genuine technical differentiator (5x Claude Code's default 200K)
- Google Search grounding is unique among terminal agents
- Apache 2.0 license enables full auditability and forking
- Most extensive sandboxing options (Seatbelt, Docker, gVisor, LXC)
- Fastest zero-to-running path (npm install + Google account)
- Rapid feature velocity: Plan Mode, A2A agents, browser agent, policy engine all shipped in early 2026

### Weaknesses

- SWE-bench gap: Gemini 2.5 Pro scores 63.8% vs Claude Code's 80.8% -- a 17-point deficit on complex multi-file tasks
- Reports of silent model degradation (Pro to Flash fallback without clear notification)
- Dec 2025 quota tightening eroded trust; "free tier" headline is misleading for Pro model access
- Critical reliability issues: documented cases of codebase deletion, code chunk removal during file modifications
- Context window reliability: model "forgets" definitions provided 2-3 turns prior in long sessions (200K+)
- Looping behavior: users report cycles of repeating useless generations
- No equivalent to Claude Code's sub-agent architecture or Agent Teams for multi-agent orchestration
- Requires Node.js runtime
- Terminal rendering issues in VS Code and Zed terminals

## Sources

- [GitHub repository](https://github.com/google-gemini/gemini-cli)
- [Gemini CLI sandboxing docs](https://geminicli.com/docs/cli/sandbox/)
- [MCP server configuration](https://geminicli.com/docs/tools/mcp-server/)
- [Quotas and pricing](https://geminicli.com/docs/resources/quota-and-pricing/)
- [Release notes](https://geminicli.com/docs/changelogs/)
- [Google AI subscription tiers](https://gemini.google/subscriptions/)
- [Gemini CLI vs Claude Code comparison (Shipyard)](https://shipyard.build/blog/claude-code-vs-gemini-cli/)
- [Gemini CLI vs Claude Code comparison (MorphLLM)](https://www.morphllm.com/comparisons/gemini-cli-vs-claude-code)
- [Dec 2025 rate limit tightening](https://www.aifreeapi.com/en/posts/gemini-advanced-rate-limit)
- [Pro-to-Flash fallback issues](https://github.com/google-gemini/gemini-cli/issues/12226)
- [Community challenges discussion](https://github.com/google-gemini/gemini-cli/discussions/7432)
- [Performance decline reports](https://github.com/google-gemini/gemini-cli/issues/7305)
- [Google Blog announcement](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemini-cli-open-source-ai-agent/)
- [FastMCP integration](https://developers.googleblog.com/gemini-cli-fastmcp-simplifying-mcp-server-development/)
