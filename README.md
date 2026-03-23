## Retrieval Augmented Generation based Q&A System

LLMs when asked highly specific subject matter based questions tend to be vague and hallucinate due to the excess of training corpus they are fed.
This project displays RAGs ability to help improve an LLMs answering capabilities on such queries by providing them with most relevant chunks from required documents, 

---

# Technologies

- `Python`
- `LangChain`
- `FAISS`
- `Hugging Face Transformers`
- `Hugging Face Embeddings`
- `PyPDF`
- `RecursiveCharacterSplitter` 

---

# STEPS TO OPERATE

1. Load required documents/corpus into `research/` folder as PDFs.
2. Execute `app.py` to launch the frontend.
3. Input a query pertaining to the loaded corpus.  
4. Receive a well phrased and context accurate response/explanation.

---

# HOW IT WORKS

- Ingests pdfs from the provided corpus. 
- Chunks the text and embeds it using `all-mpnet-base-v2`. 
- Stores chunks into `FAISS` wih `FLAT` indexing providing highly accurate retrieval. 
- Uses publicly available LLMSs (like `flan-t5-base`) to generate answers from retrieved chunks.
- Streamlit based frontend for easy interaction and prototyping.

---

# FILE OVERVIEW

- `app.py`: Frontend activation.
- `rag_chain.py`: Backend RAG pipeline.
- `research/`: Documents/Corpus to be queried.

---


