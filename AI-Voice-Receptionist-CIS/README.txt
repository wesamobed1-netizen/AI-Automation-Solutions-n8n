# AI Voice Receptionist (CIS College Voice Interface)

An advanced voice-enabled AI agent built with **n8n** and **ElevenLabs**, designed to provide students with a hands-free way to interact with college data.

### 🚀 Technical Highlights:
* **Voice-to-Text & Text-to-Voice Pipeline:** Seamlessly handles audio-based queries by leveraging high-fidelity TTS (ElevenLabs) and LLM reasoning.
* **Real-time Data Retrieval:** Integrated with **Google Sheets API** as a dynamic database to fetch student information and schedules on the fly.
* **Localized Multilingual Logic:** Specialized system prompts to handle **English and Sorani Kurdish** dialects, ensuring culturally and linguistically accurate responses.
* **Stateful Interaction:** Uses **PostgreSQL Chat Memory** to keep track of the conversation context, allowing for natural, follow-up voice questions.
* **Webhook Orchestration:** Uses a high-performance Webhook trigger to act as a backend for mobile or web-based voice applications.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **Voice Engine:** ElevenLabs (via API)
* **AI Model:** Google Gemini (Reasoning & Data Extraction)
* **Database:** Google Sheets (Knowledge Base) & PostgreSQL (Memory)
* **Communication:** Webhook Response Nodes