# Research Brief: AI Coding Agents as Products

## Executive Summary

The AI coding agent market is large ($3.5B) and growing fast, but developer trust is low and satisfaction is declining despite near-universal adoption. The clearest market gap is "open AND polished" — open-source tools offer freedom but lack workflow integration, while proprietary tools offer polish but create vendor lock-in through opaque pricing, proprietary sessions, and model restrictions. Libre-code can differentiate through session ownership, trust-calibrated permissions, BYOK model routing, and quality-first agent workflows.

## Key Findings

### 1. Developers want control, not autopilot

Professional developers explicitly reject "vibe coding" in favor of controlled agent orchestration — field studies show they accept less than 44% of AI suggestions and insist on retaining design authority. The top developer demands are fine-grained permissions, rollback checkpoints, and human-in-the-loop controls. A permission system that never interrupts for safe operations but always gates destructive ones would address the most visceral daily frustration.

### 2. Pricing has become a trust-breaker

The shift from flat subscriptions to usage-based hybrids has made costs unpredictable. Heavy users pay 2–5x advertised prices, session caps drop without notice, and credit systems create perverse incentives (scheduling work around reset times, self-censoring complex tasks). BYOK with direct API cost passthrough is the only transparent model currently available — and it's only offered by open-source tools.

### 3. AI speeds you up today and slows you down tomorrow

A Cursor study found short-term velocity gains but persistent long-term complexity increases. The METR RCT found AI made experienced developers 19% slower — while developers estimated they were 20% faster. Positive sentiment toward AI tools dropped from 70% to 60% in one year despite rising adoption. Quality-first tooling (spec-driven workflows, integrated quality gates) is an underserved positioning.

### 4. No tool owns the "open AND polished" position

Aider, Cline, and Gemini CLI offer BYOK flexibility and local-first operation but lag in persistent memory, background agents, multi-agent orchestration, and UX polish. Proprietary tools (Cursor, Claude Code, Copilot) have better workflows but lock you into their models, pricing, and data silos. Session portability between tools doesn't exist — libre-session's work is unique.

### 5. The aspirational wishlist aligns with libre-code's architecture

RedMonk's top-10 developer demands — background agents, persistent memory, predictable pricing, MCP integration, multi-agent orchestration, spec-driven development, reliability, human-in-the-loop controls, rollbacks, and reusable skills — map closely to capabilities already designed in the guidelines repo (skills, subagents, hooks, MCP).

| Positioning axis | Proprietary tools | Open-source tools | Libre-code opportunity |
|---|---|---|---|
| Pricing | Opaque, usage-based | BYOK (transparent) | BYOK + real-time cost visibility |
| Session data | Proprietary/cloud | Local but undocumented | Open format, portable (libre-session) |
| Model choice | Single-vendor | Multi-provider | Multi-provider + local models |
| Permissions | Coarse (allow/deny) | Minimal | Trust-calibrated (safe/moderate/dangerous) |
| Quality focus | Speed-first | Speed-first | Quality-first (specs, gates) |

## Next Steps

- **Write the domain vision** (`DOMAIN_VISION.md`) — the research provides clear inputs for problem, solution, and differentiation sections
- **ADR: permission model** — define the safe/moderate/dangerous action classification that drives the trust-calibrated permission system
- **ADR: session format** — decide whether to adopt, extend, or define an open standard for coding agent session data (builds on libre-session)
