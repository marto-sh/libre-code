# Claude Code

## Company Overview

Anthropic, founded 2021 by Dario Amodei (former VP Research at OpenAI) and seven co-founders. Structured as a Public Benefit Corporation with approximately 1,097 employees. In February 2026, Anthropic closed a $30B Series G at a $380B valuation — the second-largest venture deal ever. The company reports $14B ARR with 10x+ year-over-year growth for three consecutive years. Google and Amazon are strategic investors.

## Product/Service Offering

Terminal-native agentic coding CLI. Released as beta in February 2025, reached general availability in May 2025.

**Surfaces:** Terminal, VS Code extension, JetBrains plugin, Desktop App, web browser (claude.ai/code), Slack, Chrome extension.

**Key capabilities:**

- 200K token context window (1M beta for Opus 4.6/Sonnet 4.6)
- Sub-agents: up to 10 concurrent, each with its own 200K context
- Full MCP (Model Context Protocol) support
- CLAUDE.md project-level instructions
- Auto-memory across sessions
- Custom skills and commands
- Hooks for workflow automation
- CI/CD integration (GitHub Actions, GitLab)
- Code review feature
- Agent Teams (research preview, February 2026)
- Backend support for Amazon Bedrock, Google Vertex AI, OpenRouter

**Benchmark:** SWE-bench score of 80.9% with Opus 4.6 (top score as of early 2026).

## Pricing Strategy

| Tier | Price | Notes |
|------|-------|-------|
| Free | $0 | No Claude Code access |
| Pro | $20/mo | 5x free tier usage, resets every 5-8 hours |
| Max 5x | $100/mo | — |
| Max 20x | $200/mo | Weekly caps |
| Team | $25-30/user/mo | — |
| Enterprise | Custom | — |

**API pricing (per 1M tokens):**

| Model | Input | Output |
|-------|-------|--------|
| Opus | $5 | $25 |
| Sonnet | $3 | $15 |
| Haiku | $1 | $5 |

Heavy users report $100-200/mo equivalent spend. Code Review costs $15-25 per PR. August 2025 introduction of weekly caps triggered user backlash.

## Marketing & Messaging

Positioned as an "agentic coding tool" emphasizing delegation over autocomplete. Terminal-native, Unix-composable philosophy. Safety-first brand identity. Key narrative: works everywhere with the same CLAUDE.md across all surfaces. Team multiplier messaging via sub-agents and the Agent SDK.

## Market Perception

### Strengths

- 67% win rate in blind preference tests
- SWE-bench leader
- Deep codebase understanding enabled by 200K+ context
- Terminal composability fits Unix workflows
- Growing MCP ecosystem
- Superior writing and reasoning quality

### Weaknesses

- Usage limits and surprise caps (August 2025 weekly caps drew significant backlash)
- Third-party harness lockdown (January 2026: blocked OAuth for OpenCode and similar tools)
- Cost unpredictability at API tier ($1,000+/mo reported)
- Security vulnerabilities (February 2026 RCE via malicious Hooks/MCP)
- Performance regressions reported by users
- Interruption behavior ("should I proceed?" prompts consuming message allotment)

## Sources

- Claude Code docs: https://code.claude.com/docs/en/overview
- Anthropic $30B Series G: https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation
- Claude pricing: https://claude.com/pricing
- API pricing: https://platform.claude.com/docs/en/about-claude/pricing
- Claude Code Reddit overview: https://www.aitooldiscovery.com/guides/claude-code-reddit
- CVE disclosure: https://thehackernews.com/2026/02/claude-code-flaws-allow-remote-code.html
- Usage limits backlash: https://www.theregister.com/2026/01/05/claude_devs_usage_limits/
- Third-party lockdown: https://venturebeat.com/technology/anthropic-cracks-down-on-unauthorized-claude-usage-by-third-party-harnesses
