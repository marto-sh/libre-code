# Plandex

## Company Overview

Created by Dane Schneider. Written in Go (client-server). MIT license. 15,100 GitHub stars, 1,095 forks, 45 open issues. Last push: Oct 3, 2025. Latest release: server/v2.2.1 (Jul 16, 2025). On Oct 3, 2025, Schneider announced he had accepted an engineering position at Promptfoo and would wind down Plandex as a company. Cloud shut down Nov 7, 2025. Promptfoo was subsequently acquired by OpenAI (Mar 2026), meaning Schneider is now effectively at OpenAI. The open-source repository remains available but has seen no commits since the wind-down announcement. Schneider explicitly acknowledged that Claude Code "executed masterfully on the original vision of Plandex."

## Product/Service Offering

Terminal-based client-server architecture with a plan-first workflow. The core innovation is the **cumulative diff sandbox**: all AI-generated changes accumulate in a version-controlled sandbox separate from project files. Users review diffs (`plandex diff` or `plandex diff --ui` for browser view), then explicitly apply them. The sandbox is itself version-controlled, supporting rewind to any previous state and branching to explore alternatives -- described as "git for AI edits."

**Context handling:** Up to 2M tokens directly (~100K per file). Directories exceeding this are indexed via tree-sitter project maps (up to 20M tokens). Plandex loads only relevant files per step, keeping active context within limits. Context caching is used across OpenAI, Anthropic, and Google models to reduce cost and latency.

**Plan-based workflow:** The REPL defaults to chat mode for ideation. When ready, the user switches to `tell` mode; Plandex breaks the task into steps, plans each one, and implements sequentially. Full autonomy mode completes tasks end-to-end (planning, context loading, implementation, command execution, debugging). Alternatively, step-by-step mode gives fine-grained control at each stage.

**v2 additions (May 2025):** Full auto mode, JSON-based model configuration with IDE schema support, multi-provider failover (direct API to OpenRouter fallback), built-in Ollama support for local models, and CLI scripting flags (`--yes`, `--skip-menu`). Multi-model support spans Anthropic, OpenAI, Google, and open-source models.

**CLI UX:** Git-like command vocabulary -- `plandex new`, `tell`, `continue`, `build`, `review`, `apply`, `rewind`, `checkout`.

## Pricing Strategy

| Tier | Cost | Details |
|------|------|---------|
| Self-hosted | Free (MIT, BYOK) | Full functionality, requires running the Go server |
| Cloud (defunct) | Was $20/mo + credits | Shut down Nov 7, 2025; 35-day notice |

Cloud offered an "Integrated Models" mode with reduced pricing (e.g., OpenAI o3 at $2/M input, $8/M output -- 80% below list). Competed on price but couldn't match Anthropic's subsidized token pricing for Claude Code.

## Marketing & Messaging

Positioned as "designed for large projects and real world tasks." Terminal-native, correctness-first philosophy. Trust-but-verify approach: the sandbox ensures no AI change touches project files without explicit approval. Emphasized that other tools "leave behind a mess" while Plandex's sandbox keeps things clean. Targeted developers working on complex, multi-step tasks spanning many files -- distinct from Aider's single-change focus.

## Market Perception

### Strengths

- Sandbox + rewind remains the cleanest approach to AI diff management; no competitor has replicated this exact model
- Plan-then-execute workflow gives structure that free-form agents lack
- 2M token context with tree-sitter maps was ahead of competitors at v2 launch
- Multi-provider failover with automatic OpenRouter fallback is genuinely useful
- MIT license, fully self-hostable
- Git-like CLI UX praised as intuitive by terminal-oriented developers

### Weaknesses

- **Solo founder risk materialized:** maintainer left; no commits since Oct 2025
- **Cloud shutdown gave only 35 days notice** (Oct 3 to Nov 7), frustrating paying users
- **Onboarding friction:** HN users reported sign-in issues with v2 (PIN flow broken), and the client-server setup adds complexity vs. single-binary tools like Aider
- **Windows support limited to WSL**
- **Outcompeted on DX:** Claude Code and Cursor offer more polished, lower-friction experiences; Plandex's steeper learning curve and opinionated workflow narrowed its audience
- **Effectively unmaintained:** 45 open issues, no new releases since Jul 2025, no roadmap. Demoted to "honorable mention" in 2026 AI coding roundups
- **Written in Go** while the ecosystem trend (Aider/Python, Claude Code/TypeScript) has moved elsewhere; contributor base stayed small

## Sources

- [GitHub repository](https://github.com/plandex-ai/plandex) -- 15.1K stars, last push Oct 2025
- [Winding down announcement](https://plandex.ai/blog/winding-down)
- [Show HN: Plandex v2](https://news.ycombinator.com/item?id=43710576)
- [Show HN: Plandex v1](https://news.ycombinator.com/item?id=39918500)
- [MarkTechPost coverage](https://www.marktechpost.com/2024/04/04/meet-plandex-an-open-source-terminal-based-ai-coding-engine-for-complex-tasks/)
- [Geeky Gadgets: Plandex for large codebases](https://www.geeky-gadgets.com/plandex-vibe-code-large-scale-projects/)
- [DEV Community: Terminal AI agents comparison](https://dev.to/skeptrune/beyond-the-hype-a-look-at-5-ai-coding-agents-for-your-terminal-e0m)
- [OpenAI acquires Promptfoo](https://openai.com/index/openai-to-acquire-promptfoo/)
