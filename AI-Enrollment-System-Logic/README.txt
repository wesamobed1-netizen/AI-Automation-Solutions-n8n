# AI-Driven University Enrollment & Inquiry System

A sophisticated automation workflow built with **n8n** to manage university registration and student inquiries. This system uses AI to parse incoming requests, validate data, and interact with a live database.

### 🚀 Key Features:
* **Intelligent Request Parsing:** Uses an AI Agent (powered by **Groq**) to classify student requests into "New Registration" or "General Inquiry."
* **Data Validation Logic:** Features complex **If-Else nodes** to ensure all required student information (Name, Phone, Email, Major) is present before processing.
* **Live CRM Integration:** Reads and writes data to **Google Sheets** in real-time to check major availability and store student records.
* **Multi-Outcome Responses:** * Confirms successful registrations.
    * Identifies missing information.
    * Informs students if a specific major is unavailable.
* **Webhook Triggered:** Built to receive data from external forms or web applications via a secure **Webhook**.

### 🛠️ Tech Stack:
* **Orchestrator:** n8n
* **AI Model:** Groq (Large Language Model)
* **Database:** Google Sheets API
* **Logic Flow:** Conditional If Nodes, AI Tool Integration.

### 📂 Logic Flow Summary:
1. **Trigger:** Webhook receives student data.
2. **Decision:** The system checks if the major exists in the Google Sheet.
3. **AI Processing:** If the major exists, the AI Agent formats the response and confirms registration.
4. **Action:** Data is appended to the student database if all conditions are met.