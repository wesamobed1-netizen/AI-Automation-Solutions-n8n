# Enterprise RAG System with Supabase & Postgres Vector Store

A robust Retrieval-Augmented Generation (RAG) pipeline built with **n8n**, utilizing **Supabase (PostgreSQL)** as a high-performance vector database for semantic search and AI-driven insights.

## 📁 Project Structure
This system consists of two core workflows that work in tandem:
1. **The Ingestion Pipeline (`supdata-base.json`):** Handles document uploading, chunking, and embedding.
2. **The Query Engine (`supdata-pro.json`):** An AI Agent that retrieves relevant data to answer user queries accurately.

---

## 🚀 Key Features
* **PostgreSQL Vector Storage:** Leverages `pgvector` via Supabase for efficient storage and retrieval of high-dimensional embeddings.
* **Smart Document Ingestion:** Automated flow to process, chunk, and upsert data into the database using **Recursive Character Text Splitting**.
* **Hybrid AI Architecture:** Combines **OpenAI Embeddings** for data representation and **Google Gemini** for natural language generation.
* **Zero-Hallucination Retrieval:** The AI agent is strictly grounded in the vector store, ensuring it only answers based on provided documentation.
* **Loop-Based Processing:** Implements item looping to ensure reliable batch uploads of document chunks without system timeouts.

---

## 🏗️ How it Works

### 1. Ingestion Phase (The Indexer)
- **Trigger:** Initiated via form submission or manual upload.
- **Processing:** Documents are split into optimized segments (chunks) to maintain semantic context.
- **Embedding:** Text chunks are converted into vectors via OpenAI's embedding models.
- **Storage:** Vectors are stored and indexed in Supabase for lightning-fast similarity searches.

### 2. Retrieval Phase (The AI Agent)
- **User Query:** The user asks a question via the chat interface.
- **Semantic Search:** The system converts the query into a vector and searches the Supabase store for the most relevant "context."
- **Response Generation:** The AI Agent receives the context and generates a precise, fact-based answer.

---

## 🛠️ Tech Stack
* **Orchestrator:** n8n
* **Database:** Supabase (Postgres + pgvector)
* **Embeddings:** OpenAI Embeddings (text-embedding-3-small)
* **LLM:** Google Gemini 1.5 Pro / OpenAI GPT-4
* **Logic:** LangChain Integration within n8n