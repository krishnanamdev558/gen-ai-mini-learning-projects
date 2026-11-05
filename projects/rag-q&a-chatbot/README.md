# RAG Document Q&A ChatBot

A Streamlit-based Retrieval-Augmented Generation (RAG) chatbot that enables question answering over PDF research papers using LangChain, Hugging Face embeddings, FAISS vector store, and Groq-hosted LLMs.

---

## 📌 Features

- **Document Ingestion**: Loads PDF documents from the `research_papers/` directory using `PyPDFDirectoryLoader`.
- **Text Chunking**: Splits text into manageable chunks using `RecursiveCharacterTextSplitter`.
- **Embeddings**: Uses `sentence-transformers/all-mpnet-base-v2` via Hugging Face.
- **Vector Search**: Stores and retrieves document embeddings efficiently with FAISS.
- **Fast Generation**: Uses Groq (`ChatGroq`) for rapid LLM inference.
- **Interactive UI**: Built with Streamlit for a simple, responsive web interface.

---

## 🛠️ Project Structure

```text
├── app.py               # Main Streamlit application
├── requirements.txt     # Python dependencies
├── .env                 # Environment variables (API keys)
├── research_papers/     # Directory to store PDF documents
└── README.md            # Project documentation
```

---

## ⚙️ Prerequisites

- Python 3.10 or higher
- A **Groq API Key** ([Groq Console](https://console.groq.com/))
- A **Hugging Face API Token** ([Hugging Face Settings](https://huggingface.co/settings/tokens))

---

## 🚀 Getting Started

### 1. Clone or Open the Repository
Navigate to the project directory:
```bash
cd "RAG QnA ChatBot"
```

### 2. Set Up a Virtual Environment
```bash
# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On Linux/macOS:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
pip install langchain-groq python-dotenv
```

### 4. Configure Environment Variables
Create a `.env` file in the root directory (if not already present) and configure your API keys:
```env
GROQ_API_KEY=your_groq_api_key_here
HUGGINGFACE_API_KEY=your_huggingface_api_key_here
```

### 5. Add Research Papers
Place your PDF files into the `research_papers/` directory.

---

## 💻 Running the Application

Launch the Streamlit app with:
```bash
streamlit run app.py
```

---

## 📖 How to Use

1. **Embed Documents**: Click the **"Document Embedding"** button in the Streamlit interface to process PDFs, create embeddings, and index them in the FAISS vector database.
2. **Ask Questions**: Type your question into the **"Enter your question:"** text input box and press Enter.
3. **View Answers**: The application retrieves the relevant document context and displays the generated answer.

