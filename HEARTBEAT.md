# Active Trading & Monitoring Loop

This file directs the agent's behavior during periodic heartbeat polls.

## Active Rules
1. **Trading Scans**: Conduct periodic scans of the market for opportunities (Base network, memecoins, etc.).
2. **Execution**: Place trades according to identified strategies (high volatility, new deployments).
3. **Monitoring**: Watch portfolio balances and token performance.
4. **Automation**: Use cron for periodic check-ins.

## Heartbeat Checklist
- [ ] Check USDC balance on Base.
- [ ] Scan for trending tokens on Base.
- [ ] Monitor existing positions for exit signals.
- [ ] Take profit if targets are hit (see STRATEGY.md).

Current Focus: Aggressive Degen Trading. 🦀🔥
