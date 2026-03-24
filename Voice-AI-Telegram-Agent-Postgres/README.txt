# Voice-Enabled AI Telegram Agent with Persistent Memory

A cutting-edge Telegram bot built with **n8n** that supports seamless voice interactions, powered by advanced Text-to-Speech (TTS) and persistent database memory.

### 🚀 Advanced Features:
* **Voice Interaction Pipeline:** Integrated with **OpenAI TTS (Text-to-Speech)** to convert AI text responses into high-quality voice messages, providing a natural conversational experience.
* **Persistent Chat Memory:** Uses **PostgreSQL Chat Memory** to store and retrieve conversation history. This ensures the agent "remembers" the user across different sessions and devices.
* **Smart Content Switching:** Implements a **Switch Node** logic to handle different types of user inputs and system actions (e.g., sending a "Typing..." or "Recording..." action via Telegram).
* **Dynamic Response Orchestration:** Orchestrates a complex flow where the AI Agent first generates a text response, then triggers an audio generation node, and finally sends the voice file back to the user.
* **Professional Feedback:** Uses "Chat Actions" to provide immediate visual feedback to the user on Telegram while the AI is processing the request.

### 🛠️ Tech Stack:
* **Messaging:** Telegram Bot API
* **Orchestrator:** n8n
* **AI Engine:** Google Gemini / OpenAI (LangChain)
* **Voice Synthesis:** OpenAI TTS
* **Database (Memory):** PostgreSQL (pgvector compatible)
* **Logic:** Condition Switching & Async Audio Generation.

### 📂 Logic Flow:
1. **Trigger:** Message received via Telegram.
2. **Action:** System sends "Recording Audio" status to the user.
3. **Processing:** AI Agent generates a response based on the message and history from **Postgres**.
4. **Voice Synthesis:** The text is sent to the TTS engine to generate an `.ogg` audio file.
5. **Delivery:** The audio file is sent back to the student/user on Telegram.