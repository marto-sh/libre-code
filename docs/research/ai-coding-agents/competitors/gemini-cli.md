# Gemini CLI

## Company Overview

Google product, launched Jun 25, 2025. Apache 2.0 license. Built in TypeScript/Node.js, distributed via npm. Gained 17,000 GitHub stars within the first 24 hours. Follows a weekly preview + stable release cadence.

## Product/Service Offering

Terminal-native agent wrapping Gemini 2.5 Pro with a 1M token context window. Capabilities include file operations, shell commands, web fetching, MCP support, headless/scripting mode, and GitHub Actions integration. Google Search grounding is a unique differentiator -- live web search during coding sessions, unavailable in other terminal agents.

## Pricing Strategy

| Tier | Cost | Limits |
|------|------|--------|
| Free | $0 (personal Google account) | 60 req/min, 1,000 req/day, full 1M context |
| Paid | Standard Gemini API rates | Per-token billing |

Dec 2025: quota tightening caused widespread 429 errors. Reports emerged of silent fallback from 2.5 Pro to Flash after 10-15 prompts per session.

## Marketing & Messaging

"Developers live in the terminal, not chat windows." The free tier is framed as "actually free, not artificially limited." The 1M context window is positioned as "entire repository in a single prompt." Targets developers wanting maximum capability at zero cost. Apache 2.0 license emphasized for auditability and trust.

## Market Perception

### Strengths

- Most generous free tier in the market
- 1M token context is a genuine technical differentiator
- Google Search grounding is unique among terminal agents
- Apache 2.0 license
- Fastest zero-to-running path of any competitor

### Weaknesses

- No autonomous multi-file workflow capabilities
- Weaker complex reasoning (8-13 point SWE-bench gap vs Claude Code)
- Reports of silent model degradation (Pro to Flash fallback)
- Dec 2025 quota tightening eroded trust in free tier stability
- Requires Node.js runtime
- Latency issues on large projects

## Sources

- [GitHub repository](https://github.com/google-gemini/gemini-cli)
- [Google Blog announcement](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemini-cli-open-source-ai-agent/)
- [InfoQ coverage](https://www.infoq.com/news/2025/07/google-gemini-cli/)
- [17K stars overnight](https://aisecret.us/google-drops-a-terminal-bomb-gemini-cli-hits-17k-github-stars-overnight/)
