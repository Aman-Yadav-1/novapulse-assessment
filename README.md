# **🌟 NovaPulse**  
## **Arbitrage Scanner for Financial Markets**  

NovaPulse is a **Django-based application** designed to **scan and analyze arbitrage opportunities** across financial markets. Featuring **real-time data processing**, **WebSocket integration** via Daphne, and **powerful utilities**, NovaPulse empowers traders with efficient tools for market insights.  

---

## **🚀 Key Features**  
- 📈 **Arbitrage Detection:** Identifies profitable trading opportunities in real-time.  
- 🔄 **Live WebSocket Feeds:** Streams market data dynamically using Daphne.  
- 🏗️ **Robust Backend Architecture:** Modular, scalable design with Django.  
- 🛠️ **Comprehensive Logging:** Tracks errors and activities for seamless debugging.  

---

## **📂 Project Structure**  
```plaintext  
novapulse/  
├── apps/  
│   └── arbitrage_scanner/     # Core backend for arbitrage detection and processing  
├── configurations/            # Django settings and configurations  
├── logs/                      # Logs for debugging and monitoring  
├── novapulse/                 # Core Django project files  
├── wrappers/                  # Utility functions and middleware  
├── manage.py                  # Django project manager  
├── requirements.txt           # Python dependencies  
└── .idea/                     # IDE-specific settings (optional)  
```  

---

## **🛠️ Backend Overview**  

### **Framework:** Django  
- **Core Purpose:** Real-time market analysis and arbitrage detection.  
- **Key Module:** `apps/arbitrage_scanner` handles backend logic for data processing.  
- **Database Models:** Designed for efficient storage of market data and detected opportunities.  
- **APIs:** Exposes actionable insights using Django REST Framework.  

### **WebSocket Feed**  
- **Server:** Daphne (ASGI Server).  
- **Functionality:** Streams live trading data to power arbitrage detection.  
- **Example Payload:**  
  ```json  
  {  
    "pair": ["WBTC", "WSOL"]  
  }  
  ```  

---

## **🌐 Frontend Insights**  

- **Framework:** Not explicitly specified (can integrate Django templates or separate UI).  
- **Key Features:**  
  - 🔄 Refresh button for manual updates.  
  - 📡 WebSocket integration for dynamic, live data streaming.  

---

## **📥 Installation Guide**  

### **Prerequisites**  
Ensure you have:  
- Python 3.x  
- `pip` (Python package manager)  

### **Steps to Run NovaPulse**  
1. **Clone the Repository:**  
   ```bash  
   git clone https://github.com/anshulrajput046/novapulse  
   cd novapulse  
   ```  

2. **Install Dependencies:**  
   ```bash  
   pip install -r requirements.txt  
   ```  

3. **Run Database Migrations:**  
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

5. **Start the Django Server:**  
   ```bash  
   python manage.py runserver  
   ```  

6. **Access the Application:**  
   Navigate to:  
   ```  
   http://127.0.0.1:8000/novapulse/scanner/  
   ```  

7. **Run WebSocket (Daphne):**  
   ```bash  
   daphne -p 8001 novapulse.asgi:application  
   ```  

---

## **📊 Assignment 2 - AI-Powered Price Predictor**  
1. Launch **Google Colab** or **Jupyter Notebook**.  
2. Upload the `.ipynb` file from the repository.  
3. Run all cells sequentially.  
4. Analyze the output for price prediction insights.  

---

## **📝 Additional Notes**  

### **WebSocket Integration**  
- Powered by Daphne, enabling live data streams for real-time arbitrage scanning.  
- Customizable payloads to subscribe to specific trading pairs.  

### **Logging**  
- Logs are saved in the `logs/` directory for easy debugging and performance monitoring.  

---

## **🌍 API Integration**  

### **API Exploration**  
- After extensive research, **CoinGecko** was identified as a free endpoint for fetching Solana and Base network price data.  
- Note: CoinGecko is not DEX-specific.  

---

## **📸 Project Screenshot**  
![NovaPulse Screenshot](https://github.com/user-attachments/assets/a82ee5fe-3d1d-4fa6-a064-efbc2fc7001c)  

---

## **👤 About the Author**  

**Aman Yadav**  
- **GitHub:** [Aman-Yadav-1](https://github.com/Aman-Yadav-1)  
- **Portfolio:** [aman-yadav.vercel.app](https://aman-yadav.vercel.app)  

---  

⭐ If you find NovaPulse helpful, please **star the repository** and consider contributing!  

---

Let me know if further improvements are required!