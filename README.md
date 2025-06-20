# 🤖 RAGBot Lite – Local Chatbot for Document-Based Q&A

**RAGBot Lite** is a lightweight Retrieval-Augmented Generation (RAG) chatbot that allows you to chat with your documents using a local LLM powered by [Ollama](https://ollama.com/). It supports multiple file formats and provides accurate, context-only answers sourced from your content — ideal for use in product websites, documentation portals, or internal tools.

---

### 🚀 Features

- 📄 Supports PDF, DOCX, TXT, CSV, and Markdown files
- 🔍 Accurate answers using Retrieval-Augmented Generation (RAG)
- 🧠 Powered by local LLMs via Ollama (e.g., Mistral, Phi, LLaMA3)
- 💬 Gradio-based web interface with per-user chat sessions
- 🔒 Context-only prompt to avoid hallucinated answers
- ⚡ Fast, private, and runs locally (no external API calls)

---

### 📓 Run It Instantly on Google Colab

Click the badge below to launch the project on Google Colab:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1fV9i8GxMwB0fqaJvY7nL4po6uBn8jmS9?usp=sharing)

> Make sure you have a GPU runtime enabled (`Runtime > Change runtime type > GPU`) for optimal performance.

---

### 📂 Supported File Types

You can upload the following document types into the `/content/datas/` folder:

| File Type | Extension |
|-----------|-----------|
| PDF       | `.pdf`    |
| Word Doc  | `.docx`   |
| Text      | `.txt`    |
| CSV       | `.csv`    |
| Markdown  | `.md`     |

---

### 🛠️ Tech Stack

- **LLM Backend**: [Ollama](https://ollama.com/)
- **Vector Store**: ChromaDB
- **Embeddings**: `all-MiniLM-L6-v2` (via HuggingFace)
- **Framework**: LangChain
- **Frontend**: Gradio
- **Notebook Runtime**: Google Colab

---

### 💡 Use Case Ideas

- Product support chatbot (answers from manuals, docs)
- Internal document Q&A assistant
- FAQ bots for your website
- Lightweight local RAG prototype

---

### 📌 How It Works

1. Load your documents from `/content/datas/`
2. Vectorize and store them using Chroma + embeddings
3. Run a local Ollama model (like `mistral:7b`)
4. Ask questions — answers are generated **only from the relevant chunks** of your documents

---

### 🧰 Customization Tips

- Change the model in `MODEL_NAME = "mistral:7b"` to any supported by Ollama
- Add more file loaders in the `read_files_local()` function if needed
- Deploy the backend with `FastAPI` and use a custom chat UI for production

---

### 🙋‍♂️ Author

Built with ![AI](https://img.shields.io/badge/-AI%20Power-6f42c1?style=flat&logo=openai&logoColor=white) by [quick003]  
Feel free to star 🌟 the repo or contribute!

