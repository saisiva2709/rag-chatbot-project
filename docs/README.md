# 🌐 RAG-based FAQ Chatbot (n8n Cloud + Pinecone + OpenAI)

This project is a cloud-hosted Retrieval-Augmented Generation (RAG) chatbot built as part of an internship task for Altibbe Pvt Ltd. It processes uploaded documents and answers user questions with high relevance using Pinecone, OpenAI, and n8n Cloud.

---

## 🔗 Live System Flow (n8n Cloud)

### Document Ingestion Workflow:
1. Trigger: Google Drive → New file uploaded
2. Download + Chunk Split
3. Embed with OpenAI
4. Store in Pinecone vector DB

### Chat Workflow:
1. Trigger: Chat input (via HTTP or interface)
2. Embed query → Search Pinecone
3. Retrieve top-k chunks
4. Send prompt to GPT → Return answer

---

## 🔐 Credentials Used (via n8n Cloud UI)

- `OPENAI_API_KEY`
- `PINECONE_API_KEY`, `PINECONE_ENVIRONMENT`, `PINECONE_INDEX_NAME`
- Google Drive OAuth2 integration

Configured securely via **n8n Cloud Credential Manager**.

---

## 📎 Setup Instructions

No local installation required.

1. Log in to your n8n Cloud workspace.
2. Open the **Document Preprocessing Workflow**.
3. Connect Google Drive Trigger.
4. Open the **Chatbot RAG Workflow**.
5. Provide your question via webhook/chat input.
6. Receive accurate, context-aware response.









