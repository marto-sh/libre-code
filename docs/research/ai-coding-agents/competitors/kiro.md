# Kiro

## Company Overview

An AWS product (not a startup). Launched in preview on July 15, 2025 at AWS Summit NYC; reached general availability on November 17, 2025. Backed by AWS/Amazon (~$620B annual revenue). During preview, Kiro attracted 250,000+ developers, handled 300M+ requests, and processed trillions of tokens. Powered by Anthropic's Claude. Branded independently from Amazon Q Developer.

## Product/Service Offering

VS Code fork built around a spec-driven development workflow.

**Core concept — Spec-Driven Development:** Converts natural language into EARS-syntax user stories, technical design documents, and task lists before generating any code.

**Two request types:**

- **Vibe requests:** Chat-style interactions
- **Spec requests:** Structured spec-driven workflow (5x more expensive than vibe)

**Key features:**

- **Agent Hooks:** Event-driven automation — filesystem events trigger AI actions (security scans, test regeneration, etc.)
- **Auto agent** for persistent background automation
- **Kiro CLI** for terminal workflows
- **Cloud-agnostic:** No AWS account required; AWS integrations are optional

## Pricing Strategy

| Tier | Price | Vibe Requests | Spec Requests |
|------|-------|---------------|---------------|
| Free | $0 | 50/mo | 0 |
| Pro | $20/mo | 225 | 125 |
| Pro+ | ~$40/mo | 450 | 250 |
| Power | $200/mo | 2,250 | 1,250 |

Overage rates: $0.04/vibe request, $0.20/spec request.

**Pricing controversy:** Kiro consumes 4-6 internal vibe requests per visible user request, a behavior not clearly documented. Critics have described the pricing as a "wallet-wrecking tragedy."

## Marketing & Messaging

"Beyond vibe coding." Positions spec-driven development as the antidote to unmaintainable AI-generated code. Cloud-agnostic messaging to counter AWS lock-in perception. Agent Hooks promoted as a team quality enforcement mechanism. Deliberately non-corporate brand identity with a ghost mascot.

## Market Perception

### Strengths

- Spec-driven workflow is a genuine differentiator in the market
- Agent Hooks receive strong praise for automation capabilities
- AWS backing provides enterprise credibility
- Cloud-agnostic design lowers the adoption barrier
- 250K+ preview developers signal strong initial interest
- Startup program offers one year of free Pro+

### Weaknesses

- Pricing opacity from hidden internal request multiplication
- Steep learning curve for the spec-driven workflow
- Session timeouts and context loss reported
- Described as "brilliant, broken, and frustrating" by early adopters
- Limited language support at launch
- AWS association creates lock-in perception despite cloud-agnostic design

## Sources

- Beyond Vibe Coding: https://www.infoq.com/news/2025/08/aws-kiro-spec-driven-agent/
- GA announcement: https://kiro.dev/blog/general-availability/
- Pricing controversy: https://www.theregister.com/2025/08/18/aws_updated_kiro_pricing/
- Deep dive review: https://medium.com/@francoisdexemple/brilliant-broken-and-frustrating-my-deep-dive-into-amazons-kiro-ai-ide-the-flawed-junior-83e38024f40d
