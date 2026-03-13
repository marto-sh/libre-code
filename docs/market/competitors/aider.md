# Aider

## Company Overview

Created by Paul Gauthier (former CTO of Groupon, VP Engineering at Geomagical Labs/IKEA). Licensed under Apache 2.0. Solo founder with community contributors. GitHub metrics: 41,900 stars, 4,000 forks, 169 contributors. 5.3M PyPI installs. Processes 15B tokens/week across its user base. Ranks in the top 20 on OpenRouter. Self-codes 88% of its own releases.

## Product/Service Offering

Terminal-based AI pair programming tool with deep Git integration.

**Key features:**

- **Git-native workflow:** Auto-stages changes, creates commits with descriptive messages
- **Repo map:** Uses tree-sitter to index repository structure without loading full files
- **Chat modes:** `/code` (edits), `/ask` (Q&A), `/architect` (two-model: one reasons, one edits — achieves 85% on editing benchmark)
- **Model-agnostic:** Claude, GPT-4o, o1, DeepSeek, local models via Ollama
- **100+ language support**
- **Voice input, image and webpage attachment**
- **LLM Leaderboard:** Maintains its own public benchmarks for coding models

SWE-Bench Lite: 26.3% (May 2024 state-of-the-art at time of publication).

## Pricing Strategy

Free and open source (Apache 2.0). Pure bring-your-own-key (BYOK) model.

Practical daily API costs vary by model:

| Model | Estimated Daily Cost |
|-------|---------------------|
| Claude Sonnet | $5-15 |
| Claude Opus | $15-40 |
| DeepSeek | Significantly cheaper |

## Marketing & Messaging

"AI pair programming in your terminal." Targets experienced, terminal-native developers. Core messaging pillars: freedom of model choice, Git-native workflow, transparent costs, and self-dogfooding (the "singularity rate" — percentage of commits authored by Aider itself). Blog content regularly reaches the Hacker News front page.

## Market Perception

### Strengths

- Universal praise for Git integration and diff-first editing (reduces error anxiety)
- Model flexibility as a competitive advantage over locked-in alternatives
- Architect mode (two-model reasoning + editing) is innovative
- Benchmark transparency builds community trust
- Repo map scales effectively to large codebases
- Active founder engagement with the community

### Weaknesses

- Terminal-only interface is a hard filter for many developers
- Manual context management (add/remove files, `/clear` only resets chat)
- Weaker agentic planning compared to Claude Code or Cursor
- Accuracy is task-dependent (40-85% completion range)
- Single-repo constraint
- No in-session cost tracking
- Feature discoverability limited by CLI interface
- Auto-commit behavior is divisive among users

## Sources

- Aider website: https://aider.chat/
- GitHub: https://github.com/Aider-AI/aider
- LLM Leaderboards: https://aider.chat/docs/leaderboards/
- Self-assembly: https://aider.chat/2024/05/24/self-assembly.html
- Architect mode: https://aider.chat/2024/09/26/architect.html
- Context management issue: https://github.com/Aider-AI/aider/issues/3607
