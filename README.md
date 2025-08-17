# Offline Notes Assistant

An **offline AI-powered PDF Q&A assistant** built using LangChain, HuggingFace LLMs, and FAISS.  
It allows you to query PDF notes and get answers instantly, completely offline.

---

## Features

- Load PDF notes and extract text automatically.  
- Split notes into chunks for efficient retrieval.  
- Convert chunks into embeddings using **HuggingFace embeddings**.  
- Store embeddings in **FAISS** for fast similarity search.  
- Use **Flan-T5 LLM** to generate answers based on retrieved chunks.  
- Command-line chat interface for interactive Q&A.  

---

## Installation  

### 1️⃣ Clone the repository

```bash
[git clone https://github.com/JaneKarunyaJ/Personal-Notes-Assistant
cd Personal-Notes-Assistant
```
---

### 2️⃣ Install required Python packages
```bash

python3 -m pip install faiss-cpu PyPDF2 langchain langchain-community langchain-huggingface transformers
```
---
Installs all dependencies for PDF processing, embeddings, FAISS, and the LLM.


### 3️⃣ Run the PDF Notes Assistant
```bash
Place your PDF notes in the project folder.

Update the pdf_path variable in pdf_chatbot.py:

pdf_path = "Your_Notes.pdf"


Run the assistant:

python3 pdf_chatbot.py


Chat in the terminal:

📘 Offline Notes Assistant is ready! Type 'exit' to quit.

You: What is cloud computing?
Bot: Cloud computing is ...

```
---

### 4️⃣ Clean Notebook Metadata for GitHub
```bash
If GitHub shows Invalid Notebook errors due to widgets:

python3 clean_notebooks.py
```
---

### 5️⃣ Optional: Save and Load FAISS Index
```bash
The script automatically saves embeddings to:

notes_index.faiss

notes_store.pkl

To load saved embeddings without recomputing:

python3


Inside Python REPL:

import pickle
from langchain_community.vectorstores import FAISS

with open("notes_store.pkl", "rb") as f:
    vectorstore = pickle.load(f)
```
---
