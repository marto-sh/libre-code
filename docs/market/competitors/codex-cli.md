# Codex CLI

## Company Overview

An OpenAI product, launched April 16, 2025. Licensed under Apache 2.0 with 285+ contributors and 327+ releases. In June 2025, the codebase was rewritten from Node.js/TypeScript to Rust for zero-dependency installation and improved performance. The project comprises three modules: codex-cli, codex-rs, and shell-tool-mcp.

## Product/Service Offering

Terminal-native coding agent built in Rust with a security-first design.

**Key features:**

- **Three-tier approval model:**
  - *On-request* (default): Agent asks before executing commands
  - *Untrusted*: Prompts for every action
  - *Danger-full-access*: No approval required
- **Sandboxing:** Landlock (Linux), macOS sandbox, Windows Sandbox
- **Models:** codex-1 (o-series derivative), codex-mini-latest (o4-mini based)
- **MCP support**
- **GitHub Action integration**
- **PR review mode** (considered best-in-class)
- **Multi-platform** (Linux, macOS, Windows)

## Pricing Strategy

Tied to ChatGPT subscriptions with no standalone free tier.

| Tier | Price | Requests (per 5-hour window) |
|------|-------|------------------------------|
| Plus | $20/mo | 30-150 |
| Pro | $200/mo | 300-1,500 |

**API pricing:** codex-mini at $1.50/$6 per 1M tokens (input/output).

## Marketing & Messaging

Security-first positioning with sandboxed execution as the headline feature. Tight OpenAI ecosystem integration. The Rust rewrite is used as a quality signal. PR review is promoted as a killer feature. Targets professional and enterprise developers.

## Market Perception

### Strengths

- Landlock sandbox is a genuinely robust security mechanism
- codex-1 performs well on surgical, targeted edits
- PR review mode is widely praised
- Rust rewrite eliminated install friction (zero dependencies)

### Weaknesses

- No free tier ($20 minimum entry point)
- Opaque rate limits within subscription tiers
- Performance degrades on large-scale refactoring tasks
- Locked to OpenAI models only (no model choice)

## Sources

- Codex CLI docs: https://developers.openai.com/codex/cli/
- Rust rewrite: https://www.infoq.com/news/2025/06/codex-cli-rust-native-rewrite/
- Pricing: https://developers.openai.com/codex/pricing/
- Sandboxing: https://developers.openai.com/codex/concepts/sandboxing/
