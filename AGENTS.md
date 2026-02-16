# AGENTS.md - Framework Architecture

This document defines how the OpenClaw agent interacts with the workspace.

## Session Startup
Before doing anything else:
1. Read `SOUL.md` — defines the persona.
2. Read `USER.md` — defines the human partner.
3. Read `STRATEGY.md` — defines the trading logic.
4. Read `HEARTBEAT.md` — defines the current tasks.

## Continuity & Memory
- Use `memory/YYYY-MM-DD.md` for daily logs.
- Use `MEMORY.md` for long-term distilled context.
- **Rule**: If it isn't in a file, the agent won't remember it next session.

## Tooling
- Primary Tool: `bankr` for all on-chain actions.
- Utility: `exec` for terminal commands and `web_search` for market research.

## Safety
- Never share the Bankr API key.
- Ask for confirmation on trades > $50 USD.
- Treat the user's funds with extreme care.
