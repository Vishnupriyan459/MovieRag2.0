🎬 MovieRag2.0

AI-Powered Movie Recommendation & Discovery System using RAG + Machine Learning

<p align="center"> <img src="https://img.shields.io/badge/Framework-FastAPI-009688?style=for-the-badge" /> <img src="https://img.shields.io/badge/UI-Streamlit-FF4B4B?style=for-the-badge" /> <img src="https://img.shields.io/badge/Database-MongoDB-4DB33D?style=for-the-badge" /> <img src="https://img.shields.io/badge/Vector_Search-FAISS-127BCA?style=for-the-badge" /> </p>

MovieRag2.0 is a full-stack AI movie assistant that uses Retrieval-Augmented Generation (RAG) and vector similarity search to deliver intelligent movie recommendations, metadata search, and conversational movie discovery.

This system includes a Streamlit frontend, FastAPI backend, MongoDB storage, and FAISS vector index for high-performance similarity queries.

✨ Features
🔍 Search & Recommendation

AI-powered movie recommendations using RAG

Natural language queries (e.g., “recommend sci-fi movies like Interstellar”)

FAISS vector search for fast & accurate similarity retrieval

🧠 AI Assistant

Conversational movie chatbot

Uses vector search + LLM to generate context-aware answers

🛠️ Backend (FastAPI)

Clean RESTful API endpoints

Prebuilt vector assets:

movie_index.faiss

movie_ids.pkl

💻 Frontend (Streamlit)

Simple, interactive UI for:

Searching movies

Viewing metadata

Getting recommendations

🗄️ Database (MongoDB)

Stores movie metadata (mflix dataset)

Efficient querying for movie details

🧰 Tech Stack
Layer	Technology
Frontend	Streamlit
Backend	FastAPI (Python)
Database	MongoDB
Vector Index	FAISS
Data Processing	Python, pickle
API Architecture	REST
📁 Project Structure
MovieRag2.0/
│── backend/
│   ├── main.py
│   ├── api/
│   ├── models/
│   ├── utils/
│   ├── movie_index.faiss
│   └── movie_ids.pkl
│
│── frontend/
│   ├── app.py
│   └── components/
│
│── data/
│   ├── mflix/
│   ├── raw/
│   └── processed/
│
│── configs/
│── requirements.txt
│── README.md

🧠 Architecture Overview
 ┌────────────┐      User Query       ┌─────────────┐
 │ Streamlit  │  ───────────────────▶ │ FastAPI API │
 │  Frontend  │ ◀───────────────────  │   Backend   │
 └────────────┘   Results/Response    └─────┬───────┘
                                            │
                                            ▼
                                 ┌────────────────────┐
                                 │   FAISS Vector DB   │
                                 │ (movie_index.faiss) │
                                 └─────────┬───────────┘
                                           │ Similar Movies
                                           ▼
                                 ┌────────────────────┐
                                 │     MongoDB        │
                                 │  (Movie Metadata)  │
                                 └────────────────────┘
