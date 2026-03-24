# AI Multi-Agent Orchestrator (Autonomous Delegation System)

This is the most advanced project in my portfolio—a hierarchical multi-agent system built on **n8n** that mimics a real-world company structure with a **Master Orchestrator** and specialized sub-agents.

### 🚀 Technical Superpowers:
* **Autonomous Delegation:** The system uses a "Master Agent" that acts as a router. It analyzes user intent and delegates tasks to specific sub-agents (Search, Vision, or Knowledge).
* **Live Web Access:** Integrated with **SerpAPI** and **Wikipedia Tools**, allowing the agents to browse the live web and provide real-time information.
* **Vision & Multi-modal Routing:** Automatically detects media types (images/voice) and routes them to specialized Vision models for analysis.
* **Recursive Reasoning:** The agent doesn't just give an answer; it follows a "Thought-Action-Observation" loop to ensure accuracy before responding.
* **Persistent PostgreSQL Memory:** Shared memory across all agents ensuring that context is never lost, regardless of which sub-agent is handling the request.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **LLM Engine:** Google Gemini 1.5 Pro & OpenAI GPT-4
* **Search Tools:** SerpAPI (Google Search), Wikipedia API
* **Database:** PostgreSQL (Persistent Chat Memory)
* **Messaging:** Telegram Bot API

### 📂 Why this project?
This project demonstrates **Architectural Thinking**. Instead of a simple Q&A bot, I built a scalable system where new "Specialists" can be added easily. It showcases mastery over **Agentic Workflows**, which is the future of AI automation.