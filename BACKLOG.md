# Backlog

<!-- Remove items from this list once completed. -->

## Architecture Decision Records (ADR)
- Research text-to-speech open source alternatives (fast, lightweight, low resource usage, voice quality secondary)

## Competitive Landscape
- Research competitive landscape for AI coding agents

## Tool Safety Classification
- Classify tools by risk level: readonly (safe), write+revertible (moderate), write+irreversible (risky)
- Use classification to drive permission defaults and user confirmation prompts

## Agent Design
- Design agents so users can leave their work without feeling guilty — if your agents can't survive without you, they're not agents. Agents should enable genuine free time, not anxiety-driven monitoring. (ref: https://www.linkedin.com/feed/update/urn:li:activity:7430247119317528578)
- Session-based pricing lets the tool dictate how you work — you hit your limit, you "have" to stop, regardless of your flow or intent
- Bad incentives from session resets: "the session resets at 2AM, I should wake up to maximize my weekly budget" — the tool's scheduling shouldn't override yours
- These two points correlate with the guilt-free design above: if the agent can work independently, session limits and reset schedules matter less because you're not the bottleneck

## Multi-Agent Sessions
- Enable multi-agent collaboration within a single session (e.g., Claude Opus + Devstral agents doing event storming together)

## Commit Workflow
- Allow agents to commit without human approval — other harnesses require per-commit confirmation, which blocks semantic commit workflows and contradicts the philosophy that code is agent-owned

## Notes
- Ensure numpad works properly (unlike Mistral's Vibe CLI)