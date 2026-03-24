# AI Telegram Agent with Structured Output Parsing

A high-precision automation workflow that demonstrates how to extract structured JSON data from unstructured natural language inputs using **n8n** and **LangChain Output Parsers**.

### 🚀 Advanced Features:
* **Structured Data Extraction:** Implements a **Structured Output Parser** to force the LLM to return data in a strictly defined JSON schema, ensuring seamless integration with databases.
* **Reliable Data Pipeline:** Prevents formatting errors when writing to **Google Sheets** by validating the AI's output before the final execution.
* **Tool-Augmented Retrieval:** Automatically queries a Google Sheets database based on the structured parameters extracted from the user's Telegram message.
* **Dynamic Feedback Loop:** Uses a **Switch Node** to provide real-time chat actions (typing indicators) while the AI processes complex data extraction tasks.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **AI Framework:** LangChain (Structured Output Parser)
* **LLM:** OpenAI (GPT Models)
* **Database:** Google Sheets API
* **Interface:** Telegram Bot API

### 📂 Why this matters:
In enterprise automation, AI must talk to traditional databases. This project solves the "unstructured data" problem by transforming human conversation into machine-readable JSON formats, making it ideal for automated booking, ticketing, or inventory systems.