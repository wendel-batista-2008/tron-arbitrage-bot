**Tron Arbitrage Bot** is a .NET application designed to automatically detect and exploit arbitrage opportunities on the TRON blockchain. The bot monitors  decentralized exchange [SunSwap](https://sunswap.com/) for price discrepancies between trading pairs and executes trades to profit from arbitrage opportunities.

## Features

- Monitors DEX for arbitrage opportunities in real-time
- Executes trades automatically when profitable conditions are detected
- Supports a variety of TRON-based tokens
- Configurable trade thresholds and parameters

## Setup and Configuration

### RPC Node Setup

To connect to the TRON blockchain, you need access to an RPC node. You can use a public or private TRON node. One public RPC endpoint is:

```
https://api.trongrid.io
```
Alternatively, you can host your own TRON full node.

### API Tokens

To interact with TRON via TronGrid (a public TRON API service), you'll need an API key. You can obtain one by signing up on TronGrid.

Once you have the API key, update your .env with the following:
```
TRON_RPC_URL=https://api.trongrid.io
TRONGRID_API_KEY=your_api_key_here
```

### Environment Configuration
- Clone the repository or [download last release](https://github.com/wendel-batista-2008/tron-arbitrage-bot/archive/refs/heads/main.zip):

```
git clone https://github.com/wendel-batista-2008/tron-arbitrage-bot.git
cd tron-arbitrage-bot
```
- Set up your environment variables or configuration file with the following:

```
TRON_RPC_URL=https://api.trongrid.io
TRONGRID_API_KEY=your_api_key_here
TRADE_THRESHOLD=0.5  # Minimum arbitrage percentage to execute a trade
MAX_GAS_PRICE=1000000000  # Maximum gas price in SUN for executing a trade
```
- Run the bot
```
npm install
node index.js
```

### How It Works

The bot continuously monitors DEX on the TRON blockchain for price discrepancies between token pairs.
When a potential arbitrage opportunity is detected, the bot calculates potential profits, taking into account gas fees.
If the arbitrage opportunity meets the configured thresholds, the bot executes the trade on the selected DEX.
The bot logs all activities and trades for review.

### Contributing

Feel free to contribute to the project by creating a pull request. Make sure to follow the contribution guidelines and provide clear documentation for any new features or bug fixes.

### License

This project is licensed under the MIT License - see the LICENSE file for details.
