# Retrieval Augmented Generation based Q&A System

ask questions based on research papers using a simple retrieval-augmented generation (rag) system.

---

## FEATURES

- Loads pdfs from the `research/` folder  
- Splits and embeds text using `all-mpnet-base-v2`  
- Stores embeddings in a faiss vector store  
- Uses `flan-t5-base` to generate answers.
- Streamlit-based frontend for easy interaction.

---

## HOW IT WORKS

1. pdfs are loaded and split into chunks  
2. chunks are embedded and stored in faiss  
3. given a question, top-k relevant chunks are retrieved  
4. `flan-t5-base` generates an answer using only the retrieved context

---

## FILE OVERVIEW

- `app.py`: streamlit frontend  
- `rag_chain.py`: rag pipeline logic  
- `research/`: folder with pdf documents

---

## 🛠 built with

- hugging face transformers  
- langchain  
- faiss  
- streamlit
