# 💊 RAG Pharma Chatbot

A retrieval-augmented chatbot that answers domain-specific questions from uploaded pharmaceutical PDFs. Built with SentenceTransformer embeddings, FAISS for semantic search, and Groq LLM for grounded responses.

---

## 🚀 Features

- 📄 Upload pharma-related PDFs (e.g., drug leaflets, dosage guides)
- 🔍 Ask domain-specific questions (e.g., dosage, contraindications)
- 🧠 Uses semantic chunking + sentence embeddings for accurate retrieval
- 🗂️ FAISS index with cosine similarity for fast, relevant search
- 🤖 Groq LLM generates answers strictly based on retrieved context
- 🛡️ Rejects irrelevant queries with domain filtering
- 📊 Confidence scoring and source snippets for transparency
- 🧪 Gradio UI for interactive querying

---

## 🧱 Architecture

| Component        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `SentenceTransformer` | Embeds document chunks into semantic vectors                              |
| `FAISS IndexFlatIP`   | Stores normalized vectors for cosine similarity search                    |
| `GroqLLM`             | Handles chat completions with strict context grounding                    |
| `RAGPipeline`         | Orchestrates chunking, embedding, indexing, and querying                  |
| `Gradio UI`           | Provides upload + query interface with confidence feedback                |

---

## 📦 Installation

```bash
git clone https://github.com/Maaz-x14/pharma-chatbot-rag.git
cd pharma-chatbot-rag
pip install -r requirements.txt
