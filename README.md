#  RAG-Based Customer Support Assistant (LangGraph + HITL)

##  Project Overview

This project implements a **Retrieval-Augmented Generation (RAG)** based Customer Support Assistant that allows users to upload PDF documents dynamically and ask context-aware questions.

Unlike static systems, this solution processes user-uploaded documents in real-time and generates accurate answers using retrieved context.

##  Key Features

*  **Dynamic PDF Upload**

  * Users can upload documents at runtime
  * No dependency on preloaded files

*  **Context-Aware Retrieval**

  * Uses embeddings to fetch relevant content
  * Ensures answers are grounded in documents

*  **Vector Storage (ChromaDB)**

  * Stores embeddings efficiently
  * Enables fast similarity search

*  **Session-Based Isolation**

  * Each upload session has its own document context
  * Prevents mixing of unrelated data

*  **LangGraph Workflow**

  * Controls decision flow using graph-based logic
  * Supports routing: Answer / Clarify / Fallback / Escalate

*  **Human-in-the-Loop (HITL)**

  * Handles complex or unclear queries
  * Supports escalation scenarios

*  **Streamlit Interface**

  * Simple and interactive UI
  * Easy PDF upload and querying

##  System Architecture

User → Upload PDF → Text Extraction → Chunking → Embeddings → ChromaDB → Retrieval → LLM → Response

##  Tech Stack

* Python
* LangChain
* LangGraph
* ChromaDB
* Streamlit
* HuggingFace / Groq LLM
* PyPDF

##  How to Run

pip install -r requirements.txt
streamlit run app/main.py

## Sample Workflow

1. User uploads a PDF
2. System extracts and chunks text
3. Embeddings are created and stored in ChromaDB
4. User asks a query
5. Relevant chunks are retrieved
6. LLM generates a contextual response

## Example Queries

* What is this document about?
* Summarize the document
* What are the key points?

##  Limitations

* Performance depends on document size
* Requires embeddings setup for real-world usage

##  Future Improvements

* Multi-document querying
* Chat memory support
* Cloud deployment
* Improved UI/UX

##  Use Case

* Customer Support Automation
* Document-Based Question Answering
* Knowledge Assistant Systems

##  Conclusion

This project demonstrates how RAG systems can be used to build intelligent, context-aware assistants capable of handling real-world document-based queries efficiently.
