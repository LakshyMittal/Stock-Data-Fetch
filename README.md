# Unified Data Aggregation System - Stock Tracker

## 📌 Project Overview
The **Unified Data Aggregation System - Stock Tracker** is a Python-based project that fetches real-time stock market data using the **Finnhub API** and stores it in **MongoDB**. This allows users to track stock prices and volumes efficiently.

## 🚀 Features
- Fetches real-time stock data (closing price and volume) for any stock symbol.
- Stores stock data into a **MongoDB** database for future reference.
- Displays stock details fetched from the API.
- Uses **requests** for API calls and **pymongo** for database interaction.

---

## 🛠️ Setup Instructions

### 1️⃣ Prerequisites
Ensure you have the following installed on your system:
- **Python (3.x)**
- **MongoDB Database (Local or Cloud)**
- Required Python libraries: `requests`, `pymongo`

You can install the dependencies using:
```bash
pip install requests pymongo
```

### 2️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/Stock-Tracker.git
cd Stock-Tracker
```

### 3️⃣ Configure MongoDB Connection
- Create a **MongoDB Atlas account** or set up a **local MongoDB server**.
- Replace the `mongo_uri` inside the code with your **MongoDB Connection String**.
- Example connection setup inside `main.py`:
```python
mongo_uri = "your_mongodb_connection_string"
client = pymongo.MongoClient(mongo_uri)
```

### 4️⃣ Get an API Key from Finnhub
1. Sign up at [Finnhub](https://finnhub.io/).
2. Generate an API key.
3. Replace `token` inside the `fetch_stock_data()` function with your Finnhub API key.

```python
url = f'https://finnhub.io/api/v1/quote?symbol={stock_symbol}&token=your_api_key'
```

### 5️⃣ Run the Program
Execute the script using:
```bash
python main.py
```
Enter a stock symbol (e.g., `AAPL`, `TSLA`) and get real-time stock data!

---

## 📂 Project Structure
```
📁 Stock-Tracker
│── main.py  # Main script for fetching and storing stock data
│── README.md  # Project documentation
```

---

## 🖥️ How It Works
1. The user **enters a stock symbol** (e.g., AAPL for Apple).
2. The program **fetches real-time stock data** from Finnhub.
3. The stock's **closing price and volume** are extracted.
4. The data is **stored in MongoDB** for future reference.
5. The script **prints the stock data** on the console.

---

## 💡 Example Output
```
Connected to MongoDB!
Enter stock symbol (e.g., AAPL, TSLA): AAPL
Fetching data for AAPL...
API Response: {'c': 145.30, 'h': 146.0, 'l': 144.5, 'o': 145.0, 'pc': 144.2, 't': 1697500000, 'v': 2000000}
Inserting data for AAPL into MongoDB...
Data inserted successfully. ID: 6518fc0bdcba6a98a3b0b123
```

---

## 🔗 Future Enhancements
- 📊 Create a **dashboard** to visualize stock trends.
- 📈 Implement **historical data storage** for better analysis.
- 📡 Support multiple APIs for **better stock data accuracy**.

---

## 📜 License
This project is **open-source** under the **MIT License**.

---

## 🤝 Contributing
Feel free to **fork** this repo and make contributions! You can submit a **pull request** for improvements. 😊

---

## 📞 Support
For any issues, feel free to reach out via **GitHub Issues** or contact me on **LinkedIn**!

linkedin- https://www.linkedin.com/in/lakshy-mittal-501286285?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app
