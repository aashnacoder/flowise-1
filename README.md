RAG Chatbot using Flowise (AI Ethics Document QA)

##  Overview

This project demonstrates a **Retrieval-Augmented Generation (RAG) Chatbot** built using **Flowise**. The chatbot is designed to answer user queries based on a provided document (PDF) related to **AI Ethics**, ensuring context-aware and meaningful responses.

The system combines **document retrieval** with **LLM generation**, allowing accurate and explainable answers grounded in the uploaded data.

---

##  Architecture (Workflow)

The pipeline follows these steps:

1. **File Loader**

   * Loads the PDF document (*Attention is All You Need* in this case).

2. **Recursive Character Text Splitter**

   * Splits the document into smaller chunks
   * Chunk Size: 1000
   * Overlap: 200

3. **Google Gemini Embeddings**

   * Converts text chunks into vector embeddings
   * Model: `gemini-embedding-001`

4. **In-Memory Vector Store**

   * Stores embeddings for fast semantic retrieval
   * Uses Top-K retrieval for relevant chunks

5. **Mistral AI (LLM)**

   * Generates responses using retrieved context
   * Model: `mistral-tiny`
   * Temperature: 0.9

6. **Buffer Memory**

   * Maintains conversational context for better interactions

---
<img width="1830" height="804" alt="Screenshot 2026-04-08 212407" src="https://github.com/user-attachments/assets/41fae6d0-8f82-4c71-bfce-d06b24ce1791" />


##  Features

*  Upload and process PDF documents
*  Semantic search using embeddings
* Context-aware AI responses
*  Conversational memory support
*  Fast in-memory vector retrieval
*  Clean visual pipeline using Flowise

---

##  Tech Stack

* **Flowise AI**
* **Google Gemini Embeddings**
* **Mistral AI**
* **Vector Database (In-Memory)**
* **JavaScript (Flowise backend)**

---

##  Use Case

This chatbot is ideal for:

* AI Ethics document analysis
* Research paper Q&A
* Knowledge base assistants
* Educational tools

---

##  Setup Instructions

1. Install Flowise:

   ```bash
   npm install -g flowise
   ```

2. Start Flowise:

   ```bash
   flowise start
   ```

3. Open in browser:

   ```
   http://localhost:3000
   ```

4. Create a new Chatflow and configure:

   * Upload your PDF
   * Connect embedding model (Gemini)
   * Connect LLM (Mistral)
   * Link vector store and memory

5. Run the chatbot and start asking questions 

---

##  Pipeline Preview

*(Refer to the uploaded image for full visual workflow)*

---

## Future Improvements

* Add persistent vector database (e.g., Pinecone, FAISS)
* Improve citation-based responses
* Enhance UI/UX for chatbot
* Deploy as a web app

---

## Author

**Aashna**
AI & Data Enthusiast 🚀

---


