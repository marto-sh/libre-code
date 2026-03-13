# GitHub Copilot

## Company Overview

Built by GitHub (Microsoft subsidiary, acquired 2018 for $7.5B). Part of Microsoft's CoreAI division. Holds ~42% market share of paid AI coding tools. 20M+ all-time users (Jul 2025) with 400% YoY growth. Used by 90% of Fortune 100 and 50K+ organizations.

## Product/Service Offering

**Inline completions:** 46% of code written by active users in 2025.

**Copilot Chat:** Available in VS Code, JetBrains, Eclipse, Xcode, and GitHub.com.

**Agent Mode:** Autonomous multi-file editing within the IDE.

**Coding Agent:** Asynchronous -- takes GitHub issues, creates branches, writes code, runs CI, and opens PRs.

**Agent HQ (Oct 2025):** Multi-agent orchestration control plane for agents from Anthropic, OpenAI, Google, Cognition, and xAI. Configured via AGENTS.md.

**Multi-model:** Claude Opus, o3, GPT-5 mini, Grok 3. Chat source code open-sourced.

## Pricing Strategy

| Tier | Cost | Premium Requests | Other |
|------|------|-----------------|-------|
| Free | $0 | 50 | 2,000 completions |
| Pro | $10/mo | 300 | - |
| Pro+ | $39/mo | 1,500 | Frontier models |
| Business | $19/user/mo | - | Team features |
| Enterprise | $39/user/mo | - | SSO, audit, compliance |
| Overage | $0.04/request | - | - |

## Marketing & Messaging

"AI coding built your way." Agent HQ: "Any agent, any way you work." Messaging has shifted from "AI pair programmer" to "agentic DevOps." Ecosystem play -- a marketplace for agents governed through GitHub's enterprise relationships.

## Market Perception

### Strengths

- Dominant market share (~42%)
- Unmatched GitHub platform integration (issues, PRs, CI)
- Model agnosticism via multi-provider support
- Accenture study: 55% faster task completion
- Free tier positions it as the default first AI coding tool

### Weaknesses

- Shallow codebase understanding (~10% analyzed, rest based on assumptions)
- Agent mode cannot wait for long-running commands
- Security concerns: 29.1% Python and 24.2% JS generated code contained weaknesses
- 6.4% secret leakage rate (40% above baseline)
- Forced UI injection caused user backlash
- Recurring quality regression reports

## Sources

- [Plans and pricing](https://github.com/features/copilot/plans)
- [20M users milestone](https://techcrunch.com/2025/07/30/github-copilot-crosses-20-million-all-time-users/)
- [Agent HQ announcement](https://github.blog/news-insights/company-news/welcome-home-agents/)
- [Quality complaints](https://www.theregister.com/2025/09/05/github_copilot_complaints/)
