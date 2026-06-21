# Ground Engineering RAG Assistant

## Overview

Ground Engineering RAG Assistant is a Retrieval-Augmented Generation (RAG) application designed to search and query engineering documentation using Large Language Models (LLMs).

The system indexes engineering reports, specifications, investigation records, and technical documents, retrieves the most relevant content using vector similarity search, and generates answers grounded in the retrieved information.

The application supports searching within a single project or across multiple projects and provides traceability by displaying the source files used to generate responses.

---

## Motivation

Engineering organizations often maintain thousands of PDF and Word documents distributed across multiple projects. Locating relevant technical information can be time-consuming and highly dependent on individual knowledge of project archives.

This project explores how modern retrieval techniques and Large Language Models can be combined to create a searchable knowledge base for engineering documentation.

The objective is to reduce the time required to locate information while improving accessibility and knowledge sharing across projects.

---

## Key Features

### Multi-Project Search

Search within a selected project or across an entire document repository.

### Vector-Based Retrieval

Documents are embedded using Sentence Transformers and stored in a FAISS vector database for semantic similarity search.

### LLM-Powered Question Answering

Relevant document chunks are retrieved and provided as context to a Large Language Model to generate grounded responses.

### PDF and Word Document Support

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

User Query

↓

Embedding Generation

↓

FAISS Vector Search

↓

Relevant Document Retrieval

↓

Context Construction

↓

Large Language Model

↓

Answer Generation

↓

Source Display

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

1. User selects a project or searches across all projects.
2. User enters a natural language query.
3. Relevant document sections are retrieved using semantic search.
4. Retrieved content is passed to a Large Language Model.
5. The model generates an answer based only on the retrieved context.
6. Supporting source documents are displayed to the user.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/Ground-Engineering-RAG-Assistant.git
cd Ground-Engineering-RAG-Assistant
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
Ground-Engineering-RAG-Assistant/
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
* Engineering drawing indexing
* Project analytics dashboard

---

## Disclaimer

This repository contains demonstration code only.

No confidential project data, client information, proprietary documents, or API credentials are included.

---

## Author

Ishant Sharma

Civil Engineer transitioning into Computer Science with interests in:

* Information Retrieval
* Artificial Intelligence
* Large Language Models
* Software Engineering
* Engineering Automation
