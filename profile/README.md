# Nauro

**Set the doctrine once. Every agent inherits it.**

You decide an approach. Three weeks later, a different agent on a different surface proposes the one you rejected. Nauro catches the conflict in the session, before it ships.

> **You:** Should we add a WebSocket endpoint for live task updates?
>
> **Agent (via Nauro):** Conflict with a prior decision — the team already chose SSE over WebSocket because persistent connections weren't released during ECS rolling deploys. Proceed only with new evidence.

Nauro stores decisions with the reasoning behind them: what you chose, what you ruled out, and why.

That reasoning matters. Without it, an agent cannot tell whether a past rejection still applies, so old ideas keep coming back as if they were new.

Decisions can be drafted with your agent, confirmed by you, and inherited by every connected agent across Claude, Perplexity, ChatGPT, Cursor, and any MCP client.

Your decisions stay yours, not your platform's.

---

Try it — no account: `pipx install nauro && nauro init --demo`

**[Get started →](https://github.com/nauro-ai/nauro)** · thomas@nauro.ai
