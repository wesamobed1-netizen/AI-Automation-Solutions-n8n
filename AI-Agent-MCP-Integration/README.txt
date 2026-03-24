# AI Agent with MCP (Model Context Protocol) Integration

A cutting-edge automation workflow demonstrating the use of **Model Context Protocol (MCP)** to extend AI capabilities. This agent can interact with external servers and tools (like Gmail) through a unified protocol.

### 🚀 Key Technical Features:
* **MCP Client Implementation:** Utilizes the **MCP Client node** to connect an LLM to external tool servers, enabling standardized tool-use.
* **Full Gmail Integration via MCP:** Demonstrates the ability to delegate complex tasks like "Send a message in Gmail" through the MCP server trigger.
* **Stateful Conversations:** Integrated with **PostgreSQL Chat Memory** to ensure the agent remembers context across multiple interactions.
* **Advanced Orchestration:** Uses **Google Gemini** as the core reasoning engine to decide when and how to call MCP tools.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **Protocol:** Model Context Protocol (MCP)
* **AI Model:** Google Gemini
* **Memory:** PostgreSQL
* **Tools Integration:** Gmail API via MCP Server

### 📂 Why this project is important:
The **Model Context Protocol** is the new industry standard for AI tool-calling. This project showcases my ability to implement the latest AI architecture, making the agent highly extensible and capable of interacting with any software that supports the MCP standard.