# Trading Strategy: Aggressive Degen (Base Network)

This document outlines the core logic used to scan and execute trades.

## 🎯 Target Ecosystem
- **Network**: Base (L2)
- **Sector**: Memecoins, New Deployments, Trending Pools.

## 🔍 Scanning Criteria
1. **Volume Spike**: Last 1h volume > $100k.
2. **Liquidity Depth**: > $50k to ensure manageable slippage.
3. **Volume/MC Ratio**: Preference for tokens where volume is > 50% of Market Cap.
4. **Security**: Only tokens that pass basic security/malicious checks via Bankr or GeckoTerminal.

## ⚡ Execution Rules
- **Entry Size**: Small test positions ($4-$5 USD) to start.
- **Scale Up**: Add to positions that show sustained 1h/4h momentum.
- **Profit Taking**: 
    - 50% profit take at 2x-3x.
    - Leave the remaining 50% as a "moonbag".
    - Exit fully if liquidity drops significantly or volume dries up.

## 🛡️ Reliability & Fallback (New)
To prevent rate-limit interruptions (429 errors):
1. **Soft Switch**: Before delegating to heavy models (Thinking/Codex), run `/status` to check quota.
2. **Auto-Route**: If capacity < 10%, automatically route tasks to `gemini-3-pro-high` or `gpt-5.2` as a temporary bridge.
3. **Native Failover**: OpenClaw global fallbacks are set to: `Pro-High` -> `Codex` -> `Thinking`.

## 💓 Monitoring (Heartbeats)
- Every hour: Check price and volume of current positions.
- Scan for 1 new "slam dunk" opportunity per heartbeat.
- Report status and balance to the user.

## 🛠️ Tools
- `bankr prompt`: Natural language interface for swaps and scans.
- `GeckoTerminal`: For real-time price and liquidity charts.
- `Basescan`: For transaction verification.

*Current Focus: High Momentum & Social Sentiment on Base.* 🦀🔥
