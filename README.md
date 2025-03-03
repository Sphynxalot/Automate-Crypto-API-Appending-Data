# Automate-Crypto-API-Appending-Data

## 📌 Overview  
This project automates the retrieval of **real-time cryptocurrency data** from the **CoinMarketCap API**, appending the data to a dataset over time. The script timestamps each new data entry, enabling **time-series analysis** of cryptocurrency trends.  

The generated dataset can be used for **data visualization**, **trend analysis**, and **financial modeling** in Python.  

---

## 📂 Dataset & API Usage  

### 🔗 **API Source:**  
- **[CoinMarketCap API](https://pro.coinmarketcap.com/)**  

### 📊 **Data Fields Collected:**  
The API fetches data for the **top 15 cryptocurrencies**, returning fields such as:  
- `id` – Unique identifier for the cryptocurrency  
- `name` – Cryptocurrency name (e.g., Bitcoin, Ethereum)  
- `symbol` – Ticker symbol (e.g., BTC, ETH)  
- `quote.USD.price` – Current price in USD  
- `quote.USD.percent_change_1h` – Price change in the last 1 hour  
- `quote.USD.percent_change_24h` – Price change in the last 24 hours  
- `quote.USD.percent_change_7d` – Price change in the last 7 days  
- `timestamp` – **Timestamp of when the data was fetched**  

This dataset is stored in a **CSV file**, continuously updated with new API calls.  

---

## 🔧 How It Works  

### **1️⃣ API Data Retrieval**  
- The script **connects** to the CoinMarketCap API using `requests`.  
- It **fetches** the latest cryptocurrency listings.  
- The response is **converted** into a structured `Pandas DataFrame`.  

### **2️⃣ Data Normalization & Storage**  
- Data is **normalized** using `pd.json_normalize()`.  
- A **timestamp** is added to each API request.  
- Data is **appended** to a CSV file (`API.csv`) for historical tracking.  

### **3️⃣ Automated API Calls (Looped Requests)**  
- A loop runs **333 times**, making **API calls every 60 seconds**.  
- This ensures continuous data collection over time.
- This numbers used were done for testing purposes. More ideally it would run **24 times every 60 minutes** or even **30 times every 24 hours** if collecting long term data.

---

## 🚀 Features  

✅ **Real-time API Data Collection** – Automates the retrieval of **live crypto market data**.  
✅ **Historical Data Tracking** – Appends **timestamped** data for **trend analysis**.  
✅ **CSV Storage** – Saves all API responses in a structured format.  
✅ **Error Handling** – Manages `ConnectionError`, `Timeout`, and `TooManyRedirects` gracefully.  

---

# 📈 Use Cases  

- 📊 **Cryptocurrency Market Analysis** – Track price movements over time.  
- 📈 **Volatility & Trend Detection** – Identify bullish/bearish trends.  
- 🧮 **Data Visualization & Forecasting** – Use the dataset for graphs and predictive models.  
- 📉 **Historical Price Comparisons** – Compare current and past performance of top cryptocurrencies.  

---

## 🛠 Tools Used  

- **🐍 Python** – Core scripting language  
- **📡 CoinMarketCap API** – Cryptocurrency market data source  
- **📊 Pandas** – Data processing and structuring  
- **📁 CSV** – Data storage format  

---

## 🚀 Future Improvements  

- **Automate daily data collection** instead of running a manual loop.  
- **Store data in a SQL database** for better scalability.  
- **Create a Power BI dashboard** to visualize historical price trends.  
- **Implement Flask API** to allow dynamic retrieval of stored data.  

---

## 📞 Contact Information  
📌 **Created by:** *Kyron Holbrook*  
📧 **Email:** *holbrookkyron@gmail.com*  
🔗 **Portfolio/GitHub:** [Sphynxalot](https://github.com/Sphynxalot) 
🔗 **LinkedIn:** [Kyron Holbrook](https://www.linkedin.com/in/kyron-holbrook/) 
---
