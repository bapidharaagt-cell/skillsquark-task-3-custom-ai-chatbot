# SkillsQuark Task 3 – Custom AI Chatbot

## Project objective

This project implements a specialized document-question-answering chatbot using **LangChain**. Users can upload PDFs or other supported documents, build a searchable knowledge base, and ask questions about the uploaded material.

The system uses:
- LangChain for the document/retrieval workflow
- OpenAI embeddings for semantic search
- FAISS as the local vector store
- OpenAI chat model for answer generation
- Streamlit for the user interface

## Supported files

- PDF
- TXT
- CSV
- DOCX

## Workflow

```text
Upload Document
      ↓
Extract Text
      ↓
Split Text into Chunks
      ↓
Create Embeddings
      ↓
Store Vectors in FAISS
      ↓
User Question
      ↓
Retrieve Relevant Chunks
      ↓
Send Context to LLM
      ↓
Answer + Source Information
```

## Setup on the college PC

Use Python 3.10+ if available.

Open the terminal in this folder and run:

```bash
pip install -r requirements.txt
```

Create `.env` from `.env.example`.

Windows:

```bash
copy .env.example .env
```

Linux/macOS:

```bash
cp .env.example .env
```

Put your own OpenAI API key in `.env`.

**Do not share your API key or upload it to GitHub.**

## Start the chatbot

```bash
streamlit run app.py
```

A browser page should open automatically. If it does not, Streamlit will display a local URL in the terminal.

## How to test

1. Upload the included `data/sample_knowledge.txt`, or use your own PDF.
2. Click **Build Knowledge Base**.
3. Ask a question whose answer is contained in the document.
4. Check the answer and retrieved passages.
5. Ask a question whose answer is NOT in the document.
6. The chatbot should say that it could not find the information instead of inventing an answer.

## Example questions for the sample file

- What is the purpose of the project?
- What are the three main features?
- Who are the target users?
- What is the proposed technology stack?
- What should be done during testing?

## Task requirement mapping

**Requirement:** Develop a specialized chatbot using LangChain or LlamaIndex.  
**Implementation:** LangChain is used for document objects, text splitting, embeddings/retrieval workflow, and prompt/model integration.

**Requirement:** Process custom uploaded datasets or PDFs.  
**Implementation:** The Streamlit uploader accepts PDF, TXT, CSV, and DOCX files.

**Requirement:** Answer complex questions based on uploaded content.  
**Implementation:** The chatbot retrieves relevant chunks from FAISS and supplies them as context to the language model.

## Limitations

- An OpenAI API key and internet connection are required.
- Scanned/image-only PDFs may not contain extractable text unless OCR is added.
- The vector index is created during the current session and is not designed as a permanent database.
- API usage may incur charges depending on the user's account and current provider pricing.

## Security

Never put your real API key inside `app.py`, screenshots, README files, GitHub, or the submission ZIP.
