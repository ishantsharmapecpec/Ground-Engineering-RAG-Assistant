# Document Retrieval and Question Answering System

## Overview

Document Retrieval and Question Answering System is a Retrieval-Augmented Generation (RAG) application designed to search and query large collections of documents using Large Language Models (LLMs).

The system indexes PDF and Word documents, retrieves the most relevant content using vector similarity search, and generates context-aware responses grounded in the retrieved information.

The application supports searching within a single repository or across multiple repositories and provides traceability by displaying the source documents used to generate responses.

---

## Motivation

Organizations often maintain thousands of PDF and Word documents distributed across multiple projects and repositories. Locating relevant information can be time-consuming and highly dependent on individual knowledge of document storage locations.

This project explores how semantic search, vector databases and Large Language Models can be combined to create an intelligent document retrieval system capable of answering natural language questions over large document collections.

The objective is to improve information accessibility, reduce search time and enable efficient knowledge discovery.

---

## Key Features

### Multi-Repository Search

Search within a selected repository or across an entire document collection.

### Vector-Based Retrieval

Documents are embedded using Sentence Transformers and stored in a FAISS vector database for semantic similarity search.

### LLM-Powered Question Answering

Relevant document chunks are retrieved and provided as context to a Large Language Model to generate grounded responses.

### Multi-Format Document Support

Supports extraction of text from:

* PDF files
* Microsoft Word (.docx) files

### Source Traceability

Displays:

* Source document locations
* Retrieved document excerpts
* Context used to generate answers

### Fallback LLM Support

If the primary model is unavailable or rate-limited, the application automatically switches to an alternative provider.

---

## System Architecture

```text
User Query
    │
    ▼
Embedding Generation
    │
    ▼
FAISS Vector Search
    │
    ▼
Relevant Document Retrieval
    │
    ▼
Context Construction
    │
    ▼
Large Language Model
    │
    ▼
Answer Generation
    │
    ▼
Source Display
```

---

## Technology Stack

| Component       | Technology            |
| --------------- | --------------------- |
| Language        | Python                |
| Frontend        | Streamlit             |
| Vector Database | FAISS                 |
| Embeddings      | Sentence Transformers |
| LLM Framework   | LangChain             |
| PDF Processing  | PyPDF2                |
| Word Processing | python-docx           |
| LLM Providers   | Mistral AI, Groq      |

---

## Example Workflow

1. User selects a repository or searches across multiple repositories.
2. User enters a natural language query.
3. Relevant document sections are retrieved using semantic search.
4. Retrieved content is passed to a Large Language Model.
5. The model generates an answer based only on the retrieved context.
6. Supporting source documents are displayed to the user.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/Document-Retrieval-and-Question-Answering-System.git
cd Document-Retrieval-and-Question-Answering-System
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
streamlit run app.py
```

---

## Configuration

Create a local secrets file:

```toml
MISTRAL_API_KEY = "your_api_key"
GROQ_API_KEY = "your_api_key"
```

Do not commit API keys to GitHub.

---

## Repository Structure

```text
Document-Retrieval-and-Question-Answering-System/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
├── sample_data/
└── faiss_index/
```

---

## Future Enhancements

Planned improvements include:

* Hybrid keyword and vector search
* Metadata filtering
* Automated document ingestion
* Source citation generation
* User authentication
* Cloud deployment
* Multi-user support
* OCR support for scanned documents
* Analytics dashboard

---

## Key Skills Demonstrated

* Information Retrieval
* Retrieval-Augmented Generation (RAG)
* Semantic Search
* Vector Databases
* Large Language Models
* Natural Language Processing
* Python Development
* Streamlit Application Development
* Software Engineering
* AI Application Development

---

## Disclaimer

This repository contains demonstration code only.

No confidential project data, client information, proprietary documents or API credentials are included.

---

## Author

Ishant Sharma

Interests:

* Artificial Intelligence
* Information Retrieval
* Machine Learning
* Large Language Models
* Software Engineering
