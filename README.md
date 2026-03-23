## Retrieval Augmented Generation based Q&A System

Ask queries related to dense documents like research papers and get targeted context aware responses.

---

## Technologies

- `Python`
- `LangChain`
- `Hugging Face Transformers`
- `FAISS`
- `SentenceTransformers / OpenAI Embeddings`
- `PyPDF` 

---

## STEPS TO OPERATE

1. Load required documents/corpus into `research/` folder as PDFs.
2. Execute `app.py` to launch the frontend.
3. Input a query pertaining to the loaded corpus.  
4. Receive a well phrased and context accurate response/explanation.

---

## HOW IT WORKS

- Ingests pdfs from the provided corpus. 
- Splits and embeds text using `all-mpnet-base-v2`  
- Stores chunks into `FAISS` wih `FLAT` indexing providing highly accurate retrieval. 
- Uses publicly available LLMSs (like `flan-t5-base`) to generate answers from retrieved chunks.
- Streamlit based frontend for easy interaction and prototyping.

---

## FILE OVERVIEW

- `app.py`: Frontend activation.
- `rag_chain.py`: Backend RAG pipeline.
- `research/`: Documents to be queried

---


