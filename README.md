# Agentic RAG Arena

![Debate Hub Interface](https://raw.githubusercontent.com/VicoErv/agentic-rag-arena/main/image.png)

A sophisticated real-time debate platform where you can engage in multi-agent discussions with AI personalities.

## Infrastructure
This project is orchestrated via Docker Compose and consists of the following services:
- **[Backend](./backend)**: FastAPI, LangGraph, and RAG engine.
- **[Frontend](./frontend)**: React (Vite) + Tailwind CSS chat dashboard.
- **MongoDB**: Persistent chat history storage.
- **ChromaDB**: Vector search for agent memories.

## Setup & Running

1. **Environment**:
   Copy `.env.example` to `.env` and add your `OPENROUTER_API_KEY`.
   ```bash
   cp .env.example .env
   ```

2. **Launch**:
   ```bash
   docker-compose up --build
   ```

3. **Access**:
   - Web UI: http://localhost:3000
   - API Docs: http://localhost:8000/docs

## Features
- **Multi-Agent Debate**: Select multiple agents to discuss a topic.
- **Grace Period Timer**: Intelligent turn-taking orchestrated by the frontend.
- **RAG Memory**: Agents remember key facts across sessions via vector embeddings.
- **Persistence**: Database data is persisted to the local `./data` folder on the host.
