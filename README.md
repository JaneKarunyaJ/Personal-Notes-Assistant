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
git clone <your-repo-url>
cd <your-repo-folder>
2️⃣ Install required Python packages
bash
Copy
Edit
python3 -m pip install faiss-cpu PyPDF2 langchain langchain-community langchain-huggingface transformers
This installs all dependencies needed for PDF processing, embeddings, FAISS, and the LLM.

Usage
3️⃣ Run the PDF Notes Assistant
Place your PDF notes in the project folder.

Update the pdf_path variable in pdf_chatbot.py:

python
Copy
Edit
pdf_path = "Your_Notes.pdf"
Run the script:

bash
Copy
Edit
python3 pdf_chatbot.py
Chat with your assistant:

vbnet
Copy
Edit
📘 Offline Notes Assistant is ready! Type 'exit' to quit.

You: What is cloud computing?
Bot: Cloud computing is ...
Type exit or quit to close the assistant.

4️⃣ Clean Notebook Metadata for GitHub
If GitHub shows Invalid Notebook errors due to widgets:

bash
Copy
Edit
python3 clean_notebooks.py
Removes problematic metadata.widgets from all .ipynb files in the folder.

After running, notebooks should render correctly on GitHub.

5️⃣ Optional: Save and Load FAISS Index
The script automatically saves embeddings to notes_index.faiss and notes_store.pkl.

To load saved embeddings instead of recomputing:

bash
Copy
Edit
python3
python
Copy
Edit
import pickle
from langchain_community.vectorstores import FAISS

with open("notes_store.pkl", "rb") as f:
    vectorstore = pickle.load(f)
