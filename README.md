ChatBot — quick start (short)

What
- Small local RAG demo: ingest PDFs into a Chroma vector store and chat against them.

Setup (macOS)
1) Create and activate a venv:
   python3 -m venv .venv
   source .venv/bin/activate

2) Install deps:
   python -m pip install --upgrade pip
   python -m pip install langchain langchain-community langchain-openai langchain-chroma langchain-text-splitters chromadb openai tiktoken gradio python-dotenv pypdf

3) Add OpenAI key (DO NOT COMMIT):
   create a local .env with:
   OPENAI_API_KEY="sk-REPLACE_WITH_YOUR_KEY"
   ensure .env is listed in .gitignore

Populate DB (run once)
- Put PDFs into the data/ folder
- mkdir -p chroma_db
- python ingest_database.py

Run chat
- python chatbot.py

Security notes
- Rotate any leaked keys immediately.
- Never commit .env or API keys. Add .env to .gitignore and remove it from git history if accidentally
