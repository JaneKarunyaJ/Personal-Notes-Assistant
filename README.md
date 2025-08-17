# Offline Notes Assistant

An **offline AI-powered PDF Q&A assistant** built using LangChain, HuggingFace LLMs, and FAISS vector search.  
It allows you to query your PDF notes and get answers instantly, without requiring an internet connection.

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

1. Clone the repository:

```bash
git clone <your-repo-url>
cd <your-repo-folder>
Install required Python packages:

bash
Copy
Edit
python3 -m pip install faiss-cpu PyPDF2 langchain langchain-community langchain-huggingface transformers
Usage
Place your PDF notes in the project folder and update the pdf_path variable in pdf_chatbot.py:

python
Copy
Edit
pdf_path = "Your_Notes.pdf"
Run the script:

bash
Copy
Edit
python3 pdf_chatbot.py
Chat with your assistant in the terminal:

vbnet
Copy
Edit
📘 Offline Notes Assistant is ready! Type 'exit' to quit.

You: What is cloud computing?
Bot: Cloud computing is ...
Type exit or quit to close the assistant.

