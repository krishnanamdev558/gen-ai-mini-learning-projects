[![Live Demo](https://shields.io)](https://gen-ai-mini-learning-projects-5rth6ccotqhkjme8zb5ntz.streamlit.app
# Q&A Chatbot

A simple AI-powered question-answering chatbot built using
**Streamlit**, **LangChain**, and **Groq**. It allows users to interact
with large language models through a clean web interface.

## Features

-   Interactive chatbot interface built with Streamlit.
-   Integration with Groq-hosted language models using LangChain.
-   Option to select different models:
    -   `openai/gpt-oss-120b`
    -   `openai/gpt-oss-20b`
    -   `llama-3.1-8b-instant`
-   Adjustable temperature and maximum response tokens.
-   LangSmith tracing for monitoring and debugging LLM calls.
-   Secure API key input through the Streamlit sidebar.

## Tech Stack

-   Python
-   Streamlit
-   LangChain
-   LangChain-Groq
-   Groq API
-   LangSmith
-   python-dotenv

## Project Structure

``` text
QnA-ChatBot/
├── app.py
├── .env
├── requirements.txt
├── README.md
└── venv/
```

## Getting Started

### 1. Clone the repository

``` bash
git clone <your-repository-url>
cd QnA-ChatBot
```

### 2. Create and activate a virtual environment

``` bash
python -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

``` bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root:

``` env
LANGCHAIN_API_KEY=your_langsmith_api_key
```

LangSmith tracing is enabled in the application. Add a valid LangSmith
API key to use tracing.

You will also need a Groq API key. Get one from [Groq
Console](https://console.groq.com/keys) and enter it in the API key
field in the Streamlit sidebar.

### 5. Run the application

``` bash
streamlit run app.py
```

The application will open in your browser, usually at:

``` text
http://localhost:8501
```

## Usage

1.  Start the application.
2.  Enter your Groq API key in the sidebar.
3.  Select a language model.
4.  Adjust the temperature and maximum token settings if needed.
5.  Enter your question in the chat input.
6.  View the generated response.

## Environment Variables

  Variable              Purpose
  --------------------- ---------------------------
  `LANGCHAIN_API_KEY`   Enables LangSmith tracing

**Note:** Keep your API keys private. Never commit your `.env` file or
expose API keys in a public repository.

## Future Improvements

-   Add conversation history and multi-turn chat.
-   Improve the chatbot UI.
-   Add support for document-based Q&A using RAG.
-   Add streaming responses.
-   Deploy the application online.

------------------------------------------------------------------------

Built with Python, LangChain, Streamlit, and Groq.
