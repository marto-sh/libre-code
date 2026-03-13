# OpenCode

## Company Overview

Created by the SST team (Jay CEO, Frank Wang CTO, Dax Raad, Adam Elmore). SST is YC W21, profitable in 2025, with 25K GitHub stars on the SST framework. OpenCode launched Jun 19, 2025. Reached 400K monthly users within 5 months and 10M+ total downloads by Jan 2026. 120K+ GitHub stars (30K added in Jan 2026 alone). MIT license.

## Product/Service Offering

Terminal-native agent built in Go (TUI via Bubble Tea, later custom OpenTUI in TS/Zig for v1.0). Supports 75+ LLM providers via models.dev, local models via Ollama, and mid-session model switching. Features a dual-agent architecture: build (full access) and plan (read-only). Session persistence via SQLite is unique -- resume across terminal restarts. MCP support. GitHub Copilot integration added Jan 2026. Privacy architecture: zero server-side storage.

## Pricing Strategy

Free (MIT). Users pay only for their chosen LLM API. Local models via Ollama run at $0. GitHub Copilot works with existing subscriptions. Two bundled free models available (big-pickle, grok-code).

## Marketing & Messaging

"The open source coding agent." Provider-agnostic, privacy-first ("we store nothing"), works without sign-up or credit card. Targets a wide spectrum from individual developers to Fortune 500 (Cloudflare is a known adopter).

## Market Perception

### Strengths

- Broadest provider coverage (75+)
- MIT license -- most permissive in the space
- SQLite session persistence is unique and practical
- Strong privacy architecture
- Copilot integration expands audience to existing subscribers
- Fastest growth metrics among competitors (120K+ stars)
- Dual plan/build agent architecture is thoughtful design

### Weaknesses

- Output quality entirely provider-dependent
- Configuration complexity across 75+ providers
- Terminal-only (no IDE integration)
- Anthropic blocked Claude Max OAuth (Jan 2026)
- RCE vulnerability discovered Jan 2026 (patched)
- Ollama 4K default context window needs manual configuration

## Sources

- [GitHub repository](https://github.com/sst/opencode)
- [Website](https://opencode.ai/)
- [Background story](https://techfundingnews.com/opencode-the-background-story-on-the-most-popular-open-source-coding-agent-in-the-world/)
- [Growth analysis](https://blog.devgenius.io/how-opencode-went-from-zero-to-titan-in-eight-months-dcdcd8ff5572)
