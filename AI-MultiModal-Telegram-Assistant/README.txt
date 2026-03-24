# Multi-modal AI Assistant (Vision + Weather + Location)

An advanced Telegram AI Agent built with **n8n** that can "see" images, track weather in real-time, and process geographical data to provide contextual assistance.

### 🚀 Advanced Features:
* **Computer Vision Integration:** Uses **Google Gemini Vision** (or OpenAI Vision) to analyze images uploaded by users and provide detailed descriptions or answer questions about them.
* **Real-time Weather Intelligence:** Integrated with **OpenWeatherMap API** via custom tools, allowing the agent to fetch live weather data based on user location or city names.
* **Dynamic Media Handling:** Engineered to distinguish between different input types (Text, Images, Voice, Location) using complex **Switch/Condition nodes**.
* **Persistent Memory:** Utilizes **PostgreSQL Chat Memory** to keep track of user preferences and conversation history across different media types.
* **Location-Aware Services:** Can process Telegram location shares to provide localized information instantly.

### 🛠️ Tech Stack:
* **Interface:** Telegram Bot API
* **Orchestration:** n8n
* **Vision & LLM:** Google Gemini 1.5 Pro / Flash
* **External APIs:** OpenWeatherMap API
* **Database/Memory:** PostgreSQL
* **Logic:** Conditional Branching & Tool-Augmented Generation (TAG)

### 📂 How it Works:
1. **Input Detection:** The bot receives a message and identifies if it's a photo, text, or location.
2. **Contextual Processing:** - If a **Photo**, it triggers the Vision model to "analyze" the image.
    - If a **Question about Weather**, it calls the Weather Tool.
3. **Response Generation:** The AI Agent synthesizes the information and responds via Telegram in a human-friendly format.