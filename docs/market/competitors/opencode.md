# OpenCode

## Company Overview

Created by the SST team (Jay CEO, Frank Wang CTO, Dax Raad, Adam Elmore). SST is YC W21, profitable in 2025, with 25K GitHub stars on the SST framework. OpenCode launched Jun 19, 2025. Reached 400K monthly users within 5 months and 2.5M monthly users by early 2026. 120K+ GitHub stars (30K added in Jan 2026 alone). MIT license.

## Product/Service Offering

Terminal-native agent built in Go with a client-server architecture separating TUI frontend from backend logic. The TUI originally used Bubble Tea, then migrated to OpenTUI -- a custom TypeScript framework with Zig bindings supporting React, SolidJS, and Vue renderers -- for v1.0. Current release line is v1.2.x (Mar 2026).

**Provider system.** Supports 75+ LLM providers via models.dev registry. Includes OpenAI, Anthropic, Google Gemini, AWS Bedrock, Groq, Azure OpenAI, OpenRouter, and local models via Ollama/Docker Model Runner. GitHub Copilot and ChatGPT Plus/Pro subscriptions work directly. Two bundled free models available (big-pickle, grok-code).

**Mid-session model switching.** The `/models` command swaps the active model while preserving conversation context. This enables a cost-optimization workflow: plan with a frontier reasoning model, execute with a fast/cheap local model (e.g., Qwen 2.5 Coder), escalate back to the frontier model for complex decisions. No other major competitor offers this with the same breadth of providers.

**Dual-agent architecture.** Separates a Build agent (full tool access, writes code) from a Plan agent (read-only, reasons about architecture). Tool access is configured via permissions. Intended workflow: Plan first to establish understanding, then switch to Build for implementation.

**LSP integration.** Connects to 30+ language servers automatically based on file extension. Provides the LLM with real-time diagnostics, type info, hover data, go-to-definition, find-references, and call hierarchy. Servers are lifecycle-managed and file-change-aware. This gives OpenCode richer code understanding than competitors relying solely on text-based context.

**Session persistence.** SQLite-backed storage for conversations, messages, and file history. Sessions survive terminal restarts -- a unique feature in the space. MCP support for external tool integration.

## Pricing Strategy

Free (MIT). Users pay only for their chosen LLM API. Local models via Ollama run at $0. GitHub Copilot works with existing subscriptions. OpenCode Enterprise offers centralized config, SSO, and internal AI gateway integration for organizations requiring code to stay on-premises.

## Marketing & Messaging

"The open source coding agent." Provider-agnostic, privacy-first ("we store nothing"), works without sign-up or credit card. Targets a wide spectrum from individual developers to Fortune 500 (Cloudflare is a known adopter). Privacy architecture: zero server-side code storage, all processing local, direct API calls to chosen provider. When paired with Ollama or Docker Model Runner, achieves fully air-gapped operation.

Telemetry status is ambiguous -- GitHub issues (#459, #5554) show community requests for clarification and disable options, but no definitive official statement on default behavior.

## Market Perception

### Strengths

- Broadest provider coverage (75+) with seamless mid-session switching -- the defining differentiator
- MIT license -- most permissive in the space
- LSP integration provides richer code intelligence than text-only competitors
- SQLite session persistence is unique and practical for long-running tasks
- Strong privacy architecture; enterprise offering for on-prem requirements
- Fastest growth metrics among competitors (120K+ stars, 2.5M monthly users)
- Dual plan/build agent architecture enforces separation of concerns
- Product Hunt reception highlights clean TUI and low-friction setup ("one of the simplest and fastest setups")

### Weaknesses

- Output quality entirely provider-dependent -- OpenCode adds no model fine-tuning or prompt engineering layer
- Configuration complexity across 75+ providers; Ollama defaults to 4K context window requiring manual tuning
- Terminal-only (no IDE integration), though the TUI is well-regarded
- Anthropic blocked Claude Max OAuth (Jan 2026) via legal request, breaking workflows for subscribers who relied on it
- RCE vulnerability discovered Jan 2026 (patched) -- exposed risk surface of agent tool-execution model
- No git-aware workflow (contrast with Aider's automatic commit-per-edit approach)
- Telemetry posture unclear despite privacy-first marketing

### Competitive Positioning

| Dimension | OpenCode | Claude Code | Aider | Gemini CLI |
|---|---|---|---|---|
| Model lock-in | None (75+) | Anthropic only | Any via LiteLLM | Google only |
| Pricing | BYOK / free | $20+/mo, often $150-200 | BYOK / free | 1K free req/day |
| Git integration | Standard | Standard | First-class (auto-commit) | Standard |
| Code intelligence | LSP (30+ servers) | Built-in | None | None |
| Session persistence | SQLite | None | None | None |
| Privacy | Air-gappable | Cloud-dependent | Air-gappable | Cloud-dependent |

## Sources

- [GitHub repository](https://github.com/opencode-ai/opencode)
- [Website and docs](https://opencode.ai/docs/)
- [LSP documentation](https://opencode.ai/docs/lsp/)
- [Agents documentation](https://opencode.ai/docs/agents/)
- [Privacy policy](https://opencode.ai/legal/privacy-policy)
- [Enterprise offering](https://opencode.ai/enterprise)
- [Anthropic OAuth crackdown (The Register)](https://www.theregister.com/2026/02/20/anthropic_clarifies_ban_third_party_claude_access/)
- [Anthropic OAuth crackdown (VentureBeat)](https://venturebeat.com/technology/anthropic-cracks-down-on-unauthorized-claude-usage-by-third-party-harnesses)
- [CLI comparison (sanj.dev)](https://sanj.dev/post/comparing-ai-cli-coding-assistants)
- [Aider vs OpenCode (NxCode)](https://www.nxcode.io/resources/news/aider-vs-opencode-ai-coding-cli-2026)
- [Docker Model Runner integration](https://www.docker.com/blog/opencode-docker-model-runner-private-ai-coding/)
- [InfoQ coverage](https://www.infoq.com/news/2026/02/opencode-coding-agent/)
- [Growth analysis](https://blog.devgenius.io/how-opencode-went-from-zero-to-titan-in-eight-months-dcdcd8ff5572)
