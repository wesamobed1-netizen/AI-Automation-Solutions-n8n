# AI-Powered Algorithmic Trading Analyzer

A high-performance automated system built with **n8n** that monitors financial markets, analyzes technical indicators, and delivers AI-synthesized trading insights directly to Telegram.

### 🚀 Key Technical Capabilities:
* **Real-time Market Data Integration:** Connects to the **Twelve Data API** to fetch live time-series data for multiple financial symbols.
* **Technical Analysis Pipeline:** Implements automated technical analysis (Volunacci/Fibonacci & Volume patterns) on a 30-minute interval.
* **Automated Watchlist Management:** Uses a **Static Loop** to iterate through a predefined list of assets, ensuring constant monitoring without manual intervention.
* **RSS Sentiment Integration:** Scrapes and processes financial news via **RSS Feeds** to correlate price action with market sentiment.
* **AI Synthesis:** Uses Large Language Models (LLMs) to analyze the raw technical data and generate a human-readable summary of the market condition.
* **Instant Alerting System:** Triggers Telegram notifications only when specific market conditions (If-Node logic) are met, reducing noise and focusing on high-probability setups.

### 🛠️ Tech Stack:
* **Orchestration:** n8n
* **Financial Data:** Twelve Data API (REST)
* **AI Engine:** Google Gemini / OpenAI
* **Communication:** Telegram Bot API
* **Logic:** Schedule Triggers, HTTP Request handling, and Conditional Branching.

### 📂 Workflow Architecture:
1. **Schedule:** Runs every 30 minutes to capture new candle closes.
2. **Fetch:** Pulls technical data (Open, High, Low, Close, Volume).
3. **Filter:** The system checks for specific patterns (Volume spikes or Fibonacci levels).
4. **AI Analysis:** If a pattern is found, the AI interprets the data.
5. **Notify:** Sends a formatted trade alert to the user.