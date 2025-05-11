# ✉️ Cold Mail Generator using LangChain, Groq, and ChromaDB

An end-to-end GenAI-powered application that generates tailored, high-quality cold emails based on any company or website URL. It uses a **Retrieval-Augmented Generation (RAG)** pipeline with real-time web scraping, semantic search, and LLaMA3-70B (via Groq) to write context-aware outreach emails.

---

## 🚀 Features

| Capability                        | Description                                              |
|----------------------------------|----------------------------------------------------------|
| 🔗 URL Input                     | Accepts a company or personal website URL               |
| 🌐 Live Scraping                 | Extracts & parses text from real-time web pages         |
| 🧠 RAG Pipeline                  | Combines embeddings + retrieval + LLM generation        |
| ✍️ Email Generation             | Uses Groq’s LLaMA3-70B to write personalized emails     |
| ⚡ Fast Inference                | Near-instant response via Groq API                      |
| 💬 Web UI                        | Clean Streamlit interface for user interaction          |

---

## 🛠️ Tech Stack

| Component     | Tool/Service                     |
|---------------|----------------------------------|
| Frontend      | Streamlit                        |
| LLM           | Groq Cloud – LLaMA3-70B          |
| Embedding     | LangChain                        |
| Vector Store  | ChromaDB (persistent storage)    |
| Scraping      | `requests`, `BeautifulSoup`      |
| Language      | Python 3.10+                     |
| Deployment    | Local / Streamlit Cloud          |

---

## 📁 Project Structure

``text
cold-email-project/
│
├── app/
│   ├── main.py         # Streamlit app entry point
│   ├── chains.py       # LangChain logic + Groq configuration
│   └── utils.py        # Web scraping and parsing
│
├── .env                # Contains GROQ_API_KEY
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation


System Architecture

[User Input: Streamlit UI]
           │
           ▼
[Web Scraper (utils.py)]
           ▼
[Text Chunking + Embedding: LangChain]
           ▼
[ChromaDB: Vector Store]
           ▼
[Retriever: Relevant Context]
           ▼
[Prompt Injection + RAG Logic]
           ▼
[Groq API: LLaMA3-70B]
           ▼
[Email Output to Streamlit UI]
🚀 Getting Started

Clone the repository
git clone https://github.com/Nithishkaranam2002/cold-email-generator.git
cd cold-email-generator
Setup environment
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
Add your Groq API key
# .env file
GROQ_API_KEY=your_groq_api_key_here
Run the Streamlit app
streamlit run app/main.py
🔐 Notes

You must have a valid Groq API key to access the LLaMA3-70B model.
ChromaDB stores vectors locally with persistence by default.
Website content is scraped and chunked dynamically per request.
🙋‍♂️ Author

Nithish Karanam
💼 GitHub • LinkedIn

📄 License

This project is licensed for educational and demo purposes only.


---

Would you like me to:
- Save this directly as `README.md` in your project folder?
- Help you deploy it to **Streamlit Cloud** for easy sharing?

