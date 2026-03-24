# Multi-Functional AI WhatsApp Assistant (Voice, Vision & Editing)

An advanced n8n workflow that transforms WhatsApp into a powerful AI workstation. This agent doesn't just chat; it sees, hears, and creates.

### 🚀 Advanced Features:
* **AI Image Manipulation:** Integrated with **Google Gemini Vision** to edit and modify uploaded images based on user text instructions.
* **Voice-First Experience:** Uses Text-to-Speech (TTS) to respond with high-quality audio messages, providing a more natural user experience.
* **Dynamic Personality Engine:** Programmed as "Wissam," a multilingual assistant that adjusts its tone and humor based on the user's input.
* **Complex Media Handling:** Expertly manages WhatsApp binary data (Photos, Audio, and Text) using n8n's internal buffers and HTTP requests for media downloading.
* **Context-Aware Responses:** Maintains a high level of tact and brevity, ensuring responses are concise (maximum 3 sentences) and relevant.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **Messaging:** WhatsApp Business API
* **AI Engine:** Google Gemini (Vision & Chat)
* **Media Processing:** Binary Data Handling & HTTP Request Nodes
* **Voice Synthesis:** OpenAI/Google TTS Integration