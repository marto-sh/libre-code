# Cursor

## Company Overview

Anysphere Inc, founded 2022 by four MIT students (Michael Truell, CEO). Approximately 150-300 employees. Total raised ~$3.4B across multiple rounds: Seed $8M (October 2023), Series C $900M at $9.9B (June 2025), Series D $2.3B at $29.3B (November 2025, co-invested by Google and NVIDIA).

Revenue grew from $0 to $500M ARR in approximately 2.5 years, exceeding $1B by late 2025. Jensen Huang named it his "favorite enterprise AI service." Holds 18% market share (#2 behind Copilot) with 1M+ daily active users.

## Product/Service Offering

Hard fork of VS Code with integrated AI capabilities.

**Key features:**

- **Tab autocomplete:** Predicts next edit, not just next token
- **Codebase Chat:** Semantic search via @codebase, @file, @symbol, @docs references
- **Agent Mode** (formerly Composer): Autonomous multi-file editing agent
- **Cursor 2.0** (October 2025): Up to 8 parallel agents running in isolated git worktrees
- **In-house Composer model:** 4x faster than comparable third-party models
- **Background Agents:** Run on cloud VMs
- **Multi-model support:** Claude, GPT-4o, Gemini, Composer

G2 rating: 4.7/5 from 180+ reviews.

## Pricing Strategy

| Tier | Price | Notes |
|------|-------|-------|
| Hobby | Free | Unlimited slow requests |
| Pro | $20/mo | $20 credit pool |
| Pro Plus | ~$60/mo | — |
| Ultra | $200/mo | — |
| Business | $40/user/mo | — |
| Enterprise | Custom | — |

In June 2025, Cursor migrated from a flat request-cap model to a dollar-credit pool. This triggered 10-20x effective price increases for some users. A public apology and retroactive refunds followed on July 4, 2025.

## Marketing & Messaging

"The best way to code with AI." Positioned as AI-native (built around AI), not AI-added (bolted onto an existing editor). Reached $200M ARR with zero marketing spend — growth was purely organic and word-of-mouth. Over 14,000 paying companies adopted via bottom-up developer adoption.

## Market Perception

### Strengths

- Codebase chat via embeddings enables strong contextual understanding
- Zero migration friction from VS Code
- Agent Mode ahead of competitors on multi-file editing tasks
- Tab autocomplete widely praised
- Cursor 2.0 multi-agent parallelism is a novel capability
- 4.7/5 G2 rating

### Weaknesses

- Pricing opacity and June 2025 pricing change damaged trust
- Poor customer support responsiveness
- Inconsistent AI output quality across sessions
- Stability issues following updates
- Five high-severity RCE CVEs (v1.7 and below)
- All AI requests route through Cursor's AWS infrastructure (no on-prem option)
- Closed-source VS Code fork creates vendor lock-in risk
- Credit system complexity confuses users

## Sources

- Anysphere Wikipedia: https://en.wikipedia.org/wiki/Anysphere
- Contrary Research: https://research.contrary.com/company/cursor
- Series D: https://www.cnbc.com/2025/11/13/cursor-ai-startup-funding-round-valuation.html
- Cursor pricing: https://cursor.com/pricing
- June 2025 pricing change: https://cursor.com/blog/june-2025-pricing
- Security: https://www.geordie.ai/resources/technical-advisory-multiple-vulnerabilities-in-cursor-ai-code-editor
- G2 reviews: https://www.g2.com/products/cursor/reviews
