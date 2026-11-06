# Canopic

We're building a place to trade tokenized stocks on Robinhood Chain without handing your assets to anyone.

Most on-chain pools work out a price from the balance of their reserves. That's fine for tokens whose price is formed on-chain, but a stock's real price is set on an exchange, and that exchange closes at night and on weekends. So we started from the other end. Every Canopic market has a vault that quotes around a Chainlink price and adds a spread based on the market hours and how balanced the vault is.

A few things follow from that:

- When the underlying market is closed, spreads get wider and maximum trade sizes get smaller. The ticket tells you so before you trade.
- Larger orders go out to professional market makers, who sign quotes off-chain. The router compares those quotes with the vault and takes whichever pays you more.
- Trades settle in USDG within a single transaction, so your funds never sit with us.
- Quotes, fills and fees all land on-chain, where anyone can check them.

## What's here

| Repository | What it holds |
| --- | --- |
| `canopic-platform` | The website and the trading app, built with Next.js |
| `canopic-smart-contracts` | The Solidity contracts, tests and deployment scripts, built with Foundry |
| `canopic-docs` | The documentation, published through GitBook |

## Get in touch

The best place to start is [usecanopic.com](https://usecanopic.com). We also post updates on X at [@usecanopic](https://x.com/usecanopic), and you can reach the team at [hello@usecanopic.com](mailto:hello@usecanopic.com).

If you think you've found a security issue, please don't open a public issue. Email [security@usecanopic.com](mailto:security@usecanopic.com) instead and we'll pick it up from there.
