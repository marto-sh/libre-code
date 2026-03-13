# Plandex

## Company Overview

Created by Dane Schneider. MIT license. 15,100 GitHub stars. Oct 2025: Plandex Cloud began winding down after Schneider joined Promptfoo (subsequently acquired by OpenAI, Mar 2026). Schneider acknowledged that Claude Code "executed masterfully on the original vision of Plandex." Cloud shut down Nov 7, 2025. The open-source repository remains available.

## Product/Service Offering

Terminal-based client-server architecture. 2M token context (100K per file, 20M via tree-sitter project maps). Key innovation: cumulative diff sandbox -- changes are staged separately and applied only after review, described as "git for AI edits." Step-by-step rollback/rewind. Multi-model support (Anthropic, OpenAI, Google, open-source). Git-like CLI UX (`plandex new/tell/review/apply/rewind`). Full autonomy mode or step-by-step execution.

## Pricing Strategy

| Tier | Cost | Details |
|------|------|---------|
| Self-hosted | Free (MIT, BYOK) | Full functionality |
| Cloud (defunct) | Was $20/mo + credits | Shut down Nov 7, 2025 |

Competed on price but couldn't match Anthropic's subsidized token pricing for Claude Code.

## Marketing & Messaging

"Designed for large projects and real world tasks." Terminal-native. Correctness-first philosophy. Trust-but-verify approach via sandbox and rewind capabilities.

## Market Perception

### Strengths

- Git-like CLI UX praised as novel and intuitive
- Sandbox + rewind was the cleanest approach to AI diff management
- 2M token context was ahead of competitors at launch
- Tree-sitter project maps for intelligent code navigation
- MIT license

### Weaknesses

- Solo founder risk materialized (maintainer left for Promptfoo/OpenAI)
- Cloud shutdown gave users only 3 days notice
- Windows support limited to WSL
- Outcompeted on price by Claude Code's subsidized model
- Maintenance status uncertain
- Demoted to "honorable mention" in 2026 roundups

## Sources

- [GitHub repository](https://github.com/plandex-ai/plandex)
- [Winding down announcement](https://plandex.ai/blog/winding-down)
- [MarkTechPost coverage](https://www.marktechpost.com/2024/04/04/meet-plandex-an-open-source-terminal-based-ai-coding-engine-for-complex-tasks/)
