# Autonomous WhatsApp AI Commerce Agent

A full-scale automated storefront built with **n8n**, transforming WhatsApp into a smart sales channel. This agent manages the entire customer journey—from product inquiry to order placement and status tracking.

### 🚀 High-Level Features:
* **End-to-End Order Management:** Equipped with custom AI tools to create, retrieve, and update customer orders in real-time.
* **Official WhatsApp Integration:** Built using the **WhatsApp Business API**, ensuring professional and reliable communication with customers.
* **Persistent Customer Sessions:** Uses **PostgreSQL Chat Memory** indexed by phone number to maintain individual shopping carts and interaction history.
* **RAG-Powered Product Discovery:** Integrated with **Supabase Vector Store** to allow customers to search for products using natural language.
* **Smart Intent Switching:** A complex **Switch Logic** handles different message types (Text, Location, Media) and routes them to the correct processing node.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **Messaging Platform:** WhatsApp Business API
* **AI Engine:** OpenAI / Google Gemini
* **Vector Database:** Supabase (pgvector)
* **Transactional Memory:** PostgreSQL
* **Tooling:** Custom LangChain tools for Order CRUD operations.

### 📂 Logic Flow:
1. **Trigger:** Customer sends a WhatsApp message.
2. **Identification:** System identifies the customer via their phone number and fetches their active session from **Postgres**.
3. **Reasoning:** The AI Agent decides whether to search for a product (RAG) or manage an order (Tools).
4. **Execution:** If the customer wants to buy, the `Create Order` tool is triggered.
5. **Confirmation:** A structured WhatsApp message is sent back to the customer with order details.