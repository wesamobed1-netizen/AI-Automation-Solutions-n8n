# Advanced RAG System with Dynamic Namespace & Automated Ingestion

This repository contains a high-accuracy Retrieval-Augmented Generation (RAG) system built on **n8n**. It is designed to handle enterprise-level document processing, offering a fully automated pipeline from document creation in Google Drive to intelligent querying via AI Agents.

### 🌟 Key Advanced Features:
* **Dynamic Namespace Logic:** Implements a custom logic to manage vector namespaces, allowing for segregated and organized data retrieval within the same index.
* **Automated Batch Ingestion:** Uses **Loop Nodes** to handle multiple documents efficiently, ensuring no data loss during the ingestion process.
* **High-Accuracy Processing:** Features a **Recursive Character Text Splitter** and **OpenAI Embeddings** for superior text chunking and semantic understanding.
* **Real-time Synchronization:** Monitored by a **Google Drive Trigger** that detects new files every minute and updates the **Pinecone Vector Store** automatically.

### 🏗️ System Architecture:
1. **Trigger:** Detects new files in specific Google Drive folders.
2. **Processor:** Downloads, cleans, and splits text into optimized chunks.
3. **Vectorization:** Generates embeddings via OpenAI and stores them in Pinecone with specific Namespaces.
4. **Interaction:** An AI Agent queries the Vector Store using a specialized tool to provide "very accurate" answers.

### 🛠️ Tech Stack:
* **Workflow Engine:** n8n
* **Vector Store:** Pinecone
* **AI Models:** OpenAI (Embeddings & GPT), Google Gemini (Optional)
* **Logic:** Custom JavaScript/Function logic for Namespace management.