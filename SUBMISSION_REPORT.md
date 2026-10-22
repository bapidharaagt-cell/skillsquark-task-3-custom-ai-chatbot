# SKILLSQUARK – TASK 3
## Custom AI Chatbot

### Objective
Develop a specialized chatbot using LangChain that can process user-uploaded documents and answer questions based on their content.

### Technologies
- Python
- Streamlit
- LangChain
- OpenAI API
- OpenAI embeddings
- FAISS vector database
- PyPDF
- pandas
- python-docx

### Key features
1. Upload PDF, TXT, CSV, and DOCX files.
2. Extract document content.
3. Split content into smaller chunks.
4. Generate semantic embeddings.
5. Store embeddings in FAISS.
6. Retrieve relevant document passages for each question.
7. Generate an answer using only retrieved context.
8. Display retrieved passages and source/page information.
9. Refuse to invent information that is not present in the uploaded documents.

### Architecture
Upload → Text Extraction → Chunking → Embeddings → FAISS → Question → Similarity Retrieval → LangChain Prompt → LLM → Grounded Answer

### Validation
Four test cases are supplied in `test_cases.md`. They cover:
- direct factual questions,
- multi-part questions,
- questions about missing information,
- questions based on an actual PDF.

The learner should execute these tests on the college PC and record the actual outputs.

### Conclusion
The project demonstrates a practical retrieval-augmented document chatbot. Instead of asking the language model to answer from general knowledge alone, the application first retrieves relevant passages from the uploaded documents and uses those passages as the context for the answer.
