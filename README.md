# 🧠 Second Brain – A Local Knowledge Retrieval Engine Built for Humans, Not Servers

> A fast, secure, offline-first memory system that only answers what *you* know. No cloud. No hallucinations. Just your ideas, structured and retrieved intelligently.

---

## 👋 About This Project

This project began with a simple question:  
**"What if my brain had an API?"**

I wanted a local, private system that lets me:
- Save anything I learn (notes, thoughts, insights, articles)
- Retrieve the *exact context* later, with reasoning
- Operate fully offline—no cloud, no vendor lock-in
- Scale my thinking without sacrificing my autonomy

So I built this.

It's a minimal, self-contained **second brain** powered by:
- **Embeddings + FAISS** for semantic chunk retrieval
- **Local LLMs** (via Ollama) for contextual synthesis
- An optional **Knowledge Graph layer** for reasoning paths
- **FastAPI + React** for usability with zero distraction

---

## ✨ Key Features

| Capability                         | Description |
|-----------------------------------|-------------|
| 🔍 Smart Search                   | Semantic search using vector embeddings (MiniLM) |
| 🤖 Local Reasoning                | On-device LLM (DeepSeek, Phi, etc.) via Ollama |
| 🧠 Knowledge Graph Ready          | Relationship reasoning using lightweight graphs |
| 📝 Markdown Ingestion             | Save raw thoughts, articles, logs from anywhere |
| 🛠️ Fully Local Stack              | No data leaves your machine |
| 🔄 Continuous Learning            | Add new thoughts anytime, reindex instantly |
| 🎛️ Simple UI                     | Minimal React interface with Tailwind |
| 📜 Audit Log                     | Queries, answers, and edits all logged for traceability |

---

## 🧩 Stack Used

- **Backend:** Python, FastAPI, SQLite, FAISS, SentenceTransformers  
- **LLM Integration:** [Ollama](https://ollama.com), DeepSeek or Phi  
- **Frontend:** React (Vite), Tailwind CSS  
- **KG Logic (Optional):** NetworkX, graph triples, custom relationship mapping  
- **Deployment Mode:** Local-first (no cloud or Docker required)

---

## 🤔 Why I Built This

Most tools either:
- Focus too much on UI, not enough on *thinking*, or  
- Store your thoughts but don’t help you **retrieve and reason over them**

I built this as a bridge between memory and cognition—a way to make personal knowledge **accessible, explainable, and connected**.

It's also an exploration of:
- **How LLMs can enhance, not replace, reasoning**
- **Where vector retrieval fails—and how KGs fill that gap**
- **How to ship usable tools without overengineering**

---

## 📁 Project Structure

```

secondbrain-mvp/
├── backend/       # FastAPI app, embedding, DB, LLM logic
├── frontend/      # Vite + React minimalist UI
├── data/          # Your thoughts, in plain text or markdown
├── graph/         # (Optional) Knowledge graph edges
├── query\_log.txt  # Tracks what you asked, and when

````

---

## 🚀 Try It Locally (10-Min Quick Start)

```bash
# 1. Clone repo
git clone https://github.com/yourusername/secondbrain-mvp

# 2. Setup backend
cd backend
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
python embed_and_store.py  # Embeds your notes

# 3. Start server
uvicorn app:app --reload

# 4. Frontend
cd frontend
npm install && npm run dev
````

Make sure you have [Ollama](https://ollama.com) installed and models pulled (`ollama pull deepseek-coder`).

---

## 📌 Real-World Applications

* 💬 Answering personal questions using only *your* knowledge
* ✍️ Synthesizing past journal entries into insights
* 🧠 Mapping conceptual growth over time
* 🔒 Creating an AI assistant with *zero risk* of leaking thoughts

---

## 🧪 Sample Query

> “What is the Lindy Effect and how did I apply it to my side projects?”

This tool:

* Retrieves your original notes about Lindy Effect
* Adds your reflections across time (from journal entries)
* Uses an LLM to synthesize a 6th-grade explanation
* All without touching the internet

---

## 🙌 Future Directions

* Integrate voice notes & transcription (Whisper)
* Add concept evolution timeline
* Enable belief contradiction detection
* Real-time KG visualization

---

## 💡 Reflections

This project pushed me to:

* Think deeper about **human-AI collaboration**
* Explore **semantic retrieval beyond similarity**
* Prioritize **execution over perfection**

It’s not perfect. But it works. And it’s **mine**.

---
