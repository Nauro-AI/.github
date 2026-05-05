# Nauro

**Set the vision once. Every agent inherits it.**

You decide an architectural approach. Three weeks later, a different agent on a different surface proposes the rejected one. Nauro catches it before it ships.

> **You:** Should we add a WebSocket endpoint for live task updates?
>
> **Agent (via Nauro):** Conflict with a prior decision — the team already chose SSE over WebSocket because persistent connections weren't released during ECS rolling deploys. Proceed only with new evidence.

Decisions are stored with the reasoning behind them. Without that reasoning, an agent can’t tell whether a rejection still applies when circumstances change, and proposes something you ruled out months ago for reasons it can’t see.

Decisional, not observational — what you chose, what you ruled out, and why. Drafted with your agent, confirmed by you, then inherited by every connected agent across Claude, Perplexity, ChatGPT, Cursor, and any MCP client. Your decisions stay yours, not your platform’s.

---

Try it — no account: `pip install nauro && nauro init --demo`

**[Get started →](https://github.com/nauro-ai/nauro)** · thomas@nauro.ai
