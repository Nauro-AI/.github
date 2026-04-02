# Nauro

Your project context, accessible in every AI tool you use.

## The problem

AI tools don't remember your project between sessions. Open a new conversation in Claude Code and it doesn't know what you decided last week or why. Close a Cursor session and the next one starts from scratch.

If you also use multiple tools, it's worse. None of them share context. No platform vendor is going to fix that. They will never serve your context to a competitor's tool.

Nauro is the neutral layer that fixes both problems.

## How it works

Nauro maintains a structured store of your project's decisions, state, and open questions. Every decision includes rationale and rejected alternatives. New proposals are validated against what you've already decided, so agents don't contradict earlier choices.

This isn't a context dump. Agents query what they need through MCP tools, like a database, not a giant system prompt. The default is a compact summary. Deeper context is available on demand.

**Persists across sessions.** Even on a single tool, Nauro is valuable. Your project context carries forward from session to session, not just within a conversation.

**Cross-surface, same context.** One project store, readable from Claude, Perplexity, Claude Code, Cursor, Cline, and any MCP-connected tool. Log a decision in Claude Code, reference it seconds later in Perplexity.

**Passive capture.** Context builds up automatically from git commits and coding sessions. You don't maintain it. It maintains itself.

**Works offline.** The local CLI and MCP server have zero cloud dependency. Cloud sync is optional.

## What it's not

Nauro is not a code indexer. It doesn't parse ASTs or build dependency graphs.

It's not a project management tool. No task tracking, no sprints, no workflows.

It's not a replacement for git history. It captures the *why* behind your project, not the *what*.

## Contact

**thomas@nauro.ai**
