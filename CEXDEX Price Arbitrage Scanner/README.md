# NovaPulse - Arbitrage Scanner

NovaPulse is a Django-based application designed to scan and analyze arbitrage opportunities across financial markets. The project includes backend logic for real-time data processing, a WebSocket service for live market feeds running on a Daphne server, and utilities to support efficient trading strategies.

## Project Structure

```plaintext
novapulse/
├── apps/
│   └── arbitrage_scanner/     # Core backend logic for arbitrage detection and data processing
├── configurations/            # Django settings and configurations
├── logs/                      # Application logs
├── novapulse/                 # Core Django project files
├── wrappers/                  # Utility functions or middleware
├── manage.py                  # Django project manager
├── requirements.txt           # Python dependencies
└── .idea/                     # IDE settings (PyCharm)
```

## Backend

- **Framework**: Django
- **Purpose**: Scans financial markets for arbitrage opportunities.
- **Core Logic**: Implemented in `apps/arbitrage_scanner`, handling real-time data processing and arbitrage detection algorithms.
- **Database Models**: Designed to store market data and detected opportunities.
- **APIs**: Django REST Framework (assumed) for exposing arbitrage data and actionable insights.
- **Logging**: Configured under the `logs/` directory for tracking system activity and errors.

## Frontend

- **Framework**: Not specified, likely Django templates or a separate UI service.
- **Features**:
  - Refresh button to update data according to the live feed.
  - Potential enhancement with Daphne server for WebSocket support to enable automatic data pushes.

![NovaPulse](https://github.com/user-attachments/assets/a82ee5fe-3d1d-4fa6-a064-efbc2fc7001c)

## WebSocket Feed

- **Server**: Daphne (ASGI server)
- **Purpose**: Provides real-time market data feeds to support arbitrage scanning.
- **Usage**: Can be utilized to subscribe to live trading data and market updates for arbitrage detection.

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/anshulrajput046/novapulse
   cd novapulse
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Migrations:**
   ```bash
   python manage.py migrate
   ```

4. **Set Environment Variables:**
   ```bash
   export BINANCE_API_KEY=<your_binance_api_key>
   export BINANCE_SECRET=<your_binance_secret>
   export BITQUERY_API_URL=<your_bitquery_api_url>
   export BITQUERY_AUTH_TOKEN=<your_bitquery_auth_token>
   ```

5. **Run the Server:**
   ```bash
   python manage.py runserver
   ```

6. **Access the Scanner:**
   ```
   http://127.0.0.1:8000/novapulse/scanner/
   ```

7. **Run Daphne for WebSockets:**
   ```bash
   daphne -p 8001 novapulse.asgi:application
   ```

## Notes

- **WebSocket Integration**:
  - The WebSocket runs on Daphne and can be integrated for live market data feeds to power arbitrage detection.
  - WebSocket payload example: `{"pair": ["WBTC", "WSOL"]}`
- **Logs**: Application logs are stored in the `logs/` directory for monitoring and debugging.

---

**Author:** Aman Yadav