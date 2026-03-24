# Multilingual Telegram AI Agent for Academic Support

An automated student support system that integrates **Telegram Bot API** with **Google Workspace**. This AI-driven assistant manages course inquiries and registrations autonomously, providing a seamless experience for students in the Kurdistan region and beyond.

### 🚀 Key Capabilities:
* **Telegram Interface:** Fully conversational interface allowing students to interact with the college database via Telegram.
* **Smart Tool-Calling:** The agent dynamically decides when to fetch data from **Google Sheets** or trigger the **Gmail API** to notify the registrar.
* **Multilingual Support (Sorani/English):** Engineered with specific prompt logic to detect and respond in **Sorani Kurdish** (primary) and English, ensuring local accessibility.
* **Autonomous Registration:** Handles the end-to-end enrollment flow—from collecting student details to sending a structured registration email to the administration.
* **Zero-Hallucination Guardrails:** Strictly limited to the college’s official "Sheet1" data to ensure information accuracy regarding fees and schedules.

### 🛠️ Tech Stack:
* **Messaging:** Telegram Bot API
* **Orchestration:** n8n
* **AI Model:** Google Gemini / OpenAI (via LangChain)
* **Storage:** Google Sheets API
* **Notifications:** Gmail API
* **Memory:** Window Buffer Memory (for tracking conversation history)

### 📂 Workflow Logic:
1. **Trigger:** User sends a message on Telegram.
2. **Analysis:** The AI Agent identifies the intent (Inquiry vs. Registration).
3. **Database Check:** If inquiry, it queries the Google Sheet for course availability.
4. **Action:** If registration, it collects user info and sends a formatted email to the registrar.
5. **Response:** The student receives an instant confirmation or answer directly on Telegram.