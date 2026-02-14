# 🤖 RAG-Based Document Question Answering Chatbot

A **Retrieval-Augmented Generation (RAG) Chatbot** that allows users to ask questions from their documents and get **accurate, context-based answers** along with **source references**.  
The system uses **vector search + Large Language Models (LLMs)** to ensure answers are generated strictly from the provided documents.

---

## 📌 Problem Statement

Traditional chatbots often generate answers without verifying the source, leading to **hallucinations** or incorrect information.  
This project solves that problem by:
- Retrieving **relevant document chunks** using vector similarity search
- Generating answers **only from retrieved context**
- Displaying **source references** for transparency

---

## 🚀 Features

- 🔍 Semantic document search using **FAISS**
- 🧠 Context-aware answers using **Mistral LLM**
- 📄 Source citation with page numbers
- ⚡ Caching for repeated questions
- 📝 Automatic MCQ generation from documents
- 🖥️ User-friendly web interface using **Streamlit**

---

## 🛠️ Tech Stack

| Category | Technologies |
|--------|-------------|
| Programming Language | Python |
| LLM | Ollama (Mistral) |
| Embeddings | HuggingFace (all-MiniLM-L6-v2) |
| Vector Database | FAISS |
| Framework | LangChain |
| Frontend | Streamlit |
| Deployment | Local (Ollama) |

---

## 📂 Project Structure

├── Main code.ipynb # Notebook for experimentation and setup
├── Backend code.py # RAG pipeline, retrieval & LLM logic
├── UI code.py # Streamlit-based frontend
├── vectorstore/ # FAISS vector database
└── README.md



---

## ⚙️ How the System Works (Architecture)

1. **Document Embedding**
   - Documents are converted into vector embeddings using HuggingFace models
2. **Vector Storage**
   - Embeddings are stored locally using FAISS
3. **Query Processing**
   - User question is converted into an embedding
4. **Retrieval**
   - Top-k most relevant document chunks are retrieved
5. **Answer Generation**
   - LLM generates answers strictly using retrieved context
6. **Source Display**
   - Metadata (file & page number) shown as references

---

## 🧠 Backend Logic

The backend handles:
- Loading vector database
- Performing similarity search
- Prompt engineering for controlled LLM responses
- Caching repeated questions
- MCQ generation from documents  

📌 Implemented in: `Backend code.py`

---

## 🖥️ User Interface

The frontend is built using **Streamlit** and provides:
- Text input for questions
- Answer display section
- Source references
- Loading spinner for better UX  

📌 Implemented in: `UI code.py`

---

## ▶️ How to Run the Project

### 1️⃣ Prerequisites
- Python 3.9+
- Ollama installed
- Mistral model pulled:
```bash
ollama pull mistral


