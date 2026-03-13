# Goose

## Company Overview

Open-source AI agent by Block (Square, Cash App, Afterpay, TIDAL). Released Jan 2025 under Apache 2.0. Built by Block's Open Source Program Office (OSPO). 29K+ GitHub stars, 368+ contributors, 100+ releases as of early 2026. In Dec 2025, Block contributed Goose to the Linux Foundation's Agentic AI Foundation (AAIF) alongside Anthropic's MCP and OpenAI's AGENTS.md. Under AAIF, Goose transitions to neutral community governance while retaining its open-source, commercial-friendly license. Block also runs a Goose Grant Program offering $100K over 12 months to individuals or small teams building open agentic AI projects (milestone-based quarterly payouts, rolling applications, no fixed deadline).

## Product/Service Offering

Terminal CLI + desktop app + IDE integration (VS Code, Cursor, Windsurf, JetBrains via Agent Client Protocol). Model-agnostic: 25+ LLM providers including Claude, GPT-4, Gemini, and local models via Ollama. Hot-swap model switching mid-conversation. Native MCP support (3,000+ servers).

**Architecture.** Three components: interface (CLI or desktop GUI), agent (core loop managing reasoning and tool use), and extensions (MCP servers providing tools and capabilities). Local-first by design -- code stays on-device unless an external API is explicitly connected.

**Extension system.** Three types: built-in (e.g., Developer extension with shell access, .goosehints support), remote (HTTP/SSE connections to external MCP servers), and command-line (CLI-managed extensions). Configuration lives in `~/.config/goose/config.yaml`.

**Recipes.** YAML files bundling instructions, required extensions, parameters, and retry logic into shareable, reusable workflows. Support sub-recipes for composing multi-step automations. A "cookbook generator" can analyze past sessions and auto-generate recipes from common patterns.

**Distro model.** Organizations can fork and rebrand Goose with preconfigured providers, bundled extensions, custom branding, and tailored workflows -- creating a custom "distribution."

## Pricing Strategy

Entirely free. No subscription, no freemium, no markup. Strictly BYOK (bring your own key). Free LLM options available via Google Gemini free tier, Groq, and Ollama local models. Block funds development through its corporate OSPO. The grant program further funds ecosystem contributors.

## Marketing & Messaging

"Open source, extensible AI agent beyond code suggestions." "On-machine AI agent." Positioned as infrastructure layer rather than product -- something you build on, fork, and customize. Linux Foundation governance emphasized for institutional credibility and long-term neutrality. Cost narrative is prominent: "Claude Code costs $200/month; Goose does the same thing for free" has become a recurring community talking point that Block amplifies.

## Market Perception

### Strengths

- Genuinely free with zero markup; users report dropping from $200/month Claude Code Max to ~$30/month on API costs
- Model neutrality valued by multi-provider teams; hot-swap mid-session is a differentiator
- Recipes system praised as the standout feature separating Goose from competitors -- enables repeatable, shareable workflows
- AAIF governance gives institutional credibility beyond typical corporate open-source
- Strong community growth trajectory (0 to 29K stars in one year)
- Distro model enables enterprise adoption without vendor lock-in
- Desktop app + CLI + IDE integrations provide multiple entry points
- Grant program incentivizes ecosystem contributions ($100K/project)

### Weaknesses

- Poor benchmark performance: scored 5.2% on SWE-bench with 300K tokens and 587 seconds, far behind Claude Code and Codex
- Output quality entirely LLM-dependent; the harness adds no reasoning advantage of its own
- Setup complexity higher than any commercial alternative -- multiple config steps for providers, extensions, and keys
- Desktop/web UI less polished than CLI experience; described as "rough edges" rather than fundamental issues
- Safety risks with full autonomy mode (unrestricted file/shell access by default)
- No subsidized inference means cost savings depend on user's ability to negotiate API pricing
- Terminal-first friction limits adoption among less technical users

## Sources

- [GitHub repository](https://github.com/block/goose)
- [Block introduction](https://block.xyz/inside/block-open-source-introduces-codename-goose)
- [Architecture docs](https://block.github.io/goose/docs/goose-architecture/)
- [AAIF announcement](https://www.linuxfoundation.org/press/linux-foundation-announces-the-formation-of-the-agentic-ai-foundation)
- [Block on AAIF](https://block.xyz/inside/block-anthropic-and-openai-launch-the-agentic-ai-foundation)
- [Grant program](https://block.xyz/inside/introducing-the-goose-grant-program)
- [Grant details](https://block.github.io/goose/grants/)
- [Recipes system](https://block.github.io/goose/blog/2025/05/06/recipe-for-success.md/)
- [HN discussion (Feb 2025)](https://news.ycombinator.com/item?id=42879323)
- [CLI comparison (2026)](https://sanj.dev/post/comparing-ai-cli-coding-assistants)
- [VentureBeat: Goose vs Claude Code](https://venturebeat.com/infrastructure/claude-code-costs-up-to-usd200-a-month-goose-does-the-same-thing-for-free)
- [What makes Goose different](https://www.nickyt.co/blog/what-makes-goose-different-from-other-ai-coding-agents-2edc/)
