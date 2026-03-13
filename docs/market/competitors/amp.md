# Amp

## Company Overview

Built by Sourcegraph (founded 2013 by Quinn Slack, CEO, and Beyang Liu, CTO). Spinning out as independent Amp Inc in late 2025, with Quinn Slack as CEO. Sourcegraph raised $223M total (including a $125M Series D in July 2021). Investors include Sequoia, a16z, and Redpoint. Sourcegraph reported $50M revenue in 2025 with 184 employees, indexing 54B lines of code for 800K+ developers. Amp replaces Cody, whose Free, Pro, and Enterprise Starter plans have been discontinued.

## Product/Service Offering

The most platform-flexible agent in the market: runs as a VS Code, Cursor, Windsurf, or VSCodium extension, as a JetBrains plugin (via CLI), as a terminal TUI, or as a standalone CLI.

**Key features:**

- **Persistent Threads:** Server-side stored, resumable from any device, shareable with team members
- **Subagent parallelization:** Independent contexts with full tool access
- **Unconstrained token usage** in paid tier
- **Code intelligence** from Sourcegraph heritage (54B lines indexed)
- **Model-agnostic:** Claude Sonnet 4, o3, Gemini
- **Team features:** Shared threads, shared context
- **Ad-supported free tier**

## Pricing Strategy

| Tier | Price | Notes |
|------|-------|-------|
| Amp Free | $0 | Ad-supported, open-source/pre-release models, tighter context |
| Amp Smart | Pay-as-you-use | Credits for premium models, unconstrained usage |
| Team/Enterprise | Not disclosed | — |

## Marketing & Messaging

"A coding agent built for teams — engineered for outcomes, with no token constraints." IDE agnostic (no editor switching required). Persistent threads positioned as team memory. Outcomes over tokens. "The Coding Agent Is Dead" — pushing toward a post-agent paradigm.

## Market Perception

### Strengths

- IDE agnosticism widely praised (works in VS Code, Cursor, Windsurf, VSCodium, JetBrains)
- Persistent threads are a genuinely novel feature (one user reported 6,000 threads in 4 months)
- Subagent parallelization for concurrent tasks
- Sourcegraph code intelligence provides strong codebase understanding
- Ad-supported free tier is a bold experiment in the market
- Cited as the most flexible agent available

### Weaknesses

- Subagents are isolated: they cannot communicate mid-task, lack access to the main context, and only return final summaries
- Code quality concerns at scale
- CLI lag with long-running threads
- Early-stage as an independent company (less enterprise infrastructure)
- Credit consumption can add up quickly
- Sourcegraph Cody's reputation casts a shadow
- Ad-supported model is unproven for enterprise adoption

## Sources

- Amp: https://ampcode.com/
- Sourcegraph: https://sourcegraph.com/amp
- Spinout announcement: https://sourcegraph.com/blog/why-sourcegraph-and-amp-are-becoming-independent-companies
- Amp Free: https://ampcode.com/news/amp-free
- 6,000 threads case study: https://medium.com/@steph.jarmak/how-i-use-amp-after-4-months-and-6000-threads-b4058204e9de
