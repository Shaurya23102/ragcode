# 📘 Research Paper RAG System

## 🧩 Overview

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline designed to extract, process, and query information from uploaded **research papers (PDFs)**. It uses **Gemini embeddings**, **ChromaDB** as a vector store, and the **Groq LLM API** for intelligent question-answering.

---

## ⚙️ Workflow

1. **Upload Research Papers**

   * Multiple PDFs are uploaded to the system.

2. **Text Extraction & Cleaning**

   * Text is extracted from PDFs.
   * Unnecessary symbols, line breaks, and references are cleaned to ensure high-quality data.

3. **Chunking**

   * Pymypdf library is used to split text into smaller **overlapping chunks** for better semantic retrieval.

4. **Embedding Generation**

   * Each chunk is embedded using **Gemini embeddings**.
   * The resulting vectors represent the semantic meaning of each chunk.

5. **Vector Storage**

   * Embeddings are stored in a **ChromaDB** database for efficient similarity search.

6. **Query & Retrieval**

   * A user query is embedded and compared against stored vectors.
   * Top relevant chunks are retrieved from ChromaDB.

7. **Response Generation**

   * Retrieved context is passed to the **Groq LLM API**, which generates a context-aware answer.

---

## 🧠 Tech Stack

| Component          | Description                                                                    |
| ------------------ | ------------------------------------------------------------------------------ |
| **Language**       | Python                                                                         |
| **Embeddings**     | Gemini                                                                         |
| **Vector Store**   | ChromaDB                                                                       |
| **LLM**            | Groq API                                                                       |
| **Libraries Used** | `langchain`, `chromadb`, `pdfminer`/`PyPDF2`, `tiktoken`, `requests`, `dotenv` |

---





