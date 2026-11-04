# Nauro

**Decision system for software built with AI**

You decide an approach. Three weeks later, a different agent on a different surface proposes the one you rejected. Connected agents can look up that decision and its reasoning before choosing an approach.

> **You:** Should we add a WebSocket endpoint for live task updates?
>
> **Agent (via Nauro):** Related prior decision: the team chose SSE over WebSocket because persistent connections weren't released during ECS rolling deploys.

Nauro stores decisions with the reasoning behind them: what you chose, what you ruled out, and why.

That reasoning matters. Without it, an agent cannot tell whether a past rejection still applies, so old ideas keep coming back as if they were new.

Decisions can be drafted with your agent, confirmed by you, and inherited by every connected agent across Claude, Perplexity, ChatGPT, Cursor, and any MCP client.

Your decisions stay yours, not your platform's.

---

Try it, no account: `uv tool install nauro && nauro init --demo`

**[Get started →](https://nauro.ai/decision-system)** · [GitHub](https://github.com/nauro-ai/nauro) · thomas@nauro.ai
