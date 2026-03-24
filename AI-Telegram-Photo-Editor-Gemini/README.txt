# AI-Powered Telegram Photo Editor (Background Manipulation)

An advanced automation workflow built with **n8n** that uses **Google Gemini (Nano Banana Pro)** to perform intelligent image editing. This bot allows users to upload a photo and request background changes via text, maintaining 100% subject consistency.

### 🚀 Key Technical Features:
* **Subject-Consistent AI Editing:** Utilizes Gemini's advanced image-to-image capabilities to modify environments while preserving the person's face, features, and clothing exactly as the original.
* **Dynamic Prompt Engineering:** Implements a custom prompt logic that takes the user's Telegram caption and converts it into high-fidelity AI instructions for the image model.
* **Telegram Binary Handling:** Efficiently manages binary data streams—receiving photos via Telegram Bot API, downloading them for processing, and re-uploading the edited version.
* **Smart Content Routing:** Uses a **Switch Node** to ensure the workflow only triggers when a photo is present, preventing errors from text-only messages.
* **Photorealistic Output:** Engineered to maintain consistent lighting and shadows between the original subject and the new AI-generated background.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **AI Model:** Google Gemini 3 Flash Image (Nano Banana Pro)
* **Messaging Interface:** Telegram Bot API
* **Data Handling:** n8n Binary Data & File ID matching

### 📂 Logic Flow:
1. **Trigger:** User sends a photo with a caption (e.g., "Put me on Mars").
2. **Data Extraction:** The bot fetches the `file_id` and the caption from the Telegram JSON.
3. **AI Processing:** The original image is sent to Gemini Pro with specific instructions: "Modify ONLY the background; keep the subject unchanged."
4. **Delivery:** The edited high-resolution photo is sent back to the user's Telegram chat.