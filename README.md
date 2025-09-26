# DeFi Bot

A bot that monitors blockchain wallets, tracks USDT deposits/withdrawals, calculates fund performance using a Net Asset Value (NAV) and Shares system, and monitors investments across various DeFi protocols on multiple EVM chains.

## Features

- **Blockchain Monitoring**: Tracks wallet activity across multiple EVM chains (Ethereum, Base, Arbitrum, etc.)
- **NAV & Shares System**: Calculates fund performance using a Net Asset Value system
- **Protocol Tracking**: Monitors investments in various DeFi protocols (AAVE, Pendle, Morpho, etc.)
- **Weighted APY Calculation**: Calculates overall fund APY based on protocol allocations
- **Notification System**: Alerts administrators about withdrawal requests
- **Data Persistence**: Stores historical data in PostgreSQL database
- **API Access**: Provides RESTful API for data access

## Project Structure

```
defi-bot/
├── blockchain_monitor/      # Handles blockchain interactions
├── defi_protocols/          # Handles DeFi protocol interactions
├── core_logic/              # Central business logic
├── data_storage/            # Database interactions
├── api/                     # RESTful API
├── notifications/           # Handles sending notifications
├── config/                  # Configuration files
├── tests/                   # Unit and integration tests
└── main.py                  # Main application entry point
```

## Setup

### Prerequisites

- Python 3.8+
- PostgreSQL
- Access to blockchain node providers (Infura, Alchemy, etc.)

### Installation

1. Clone the repository
   ```
   git clone https://github.com/yourusername/defi-bot.git
   cd defi-bot
   ```

2. Create and activate a virtual environment
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies
   ```
   pip install -r requirements.txt
   ```

4. Set up the configuration
   ```
   cp config/example.env config/.env
   # Edit .env with your configuration details
   ```

5. Initialize the database
   ```
   python scripts/init_db.py
   ```

6. Run the application
   ```
   python main.py
   ```

## Documentation

See the `docs/` directory for detailed documentation on:

- API endpoints
- System architecture
- User guide
- Developer guide

## Development

See `tasks.md` for the current project roadmap and task status.

## License

[MIT License](LICENSE) 
