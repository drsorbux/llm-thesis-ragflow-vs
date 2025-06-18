# 🧠 RAGFlowBench: Benchmarking LangFlow with RAG and Multi-RAG using LLMs

> Comparative study on traditional LLMs, RAG, and Multi-RAG pipelines implemented with LangFlow, ChromaDB, and LangWatch.

## 📚 Abstract

This project supports the thesis "*Benchmark and Evaluation of Retrieval-Augmented Generation Models with LangFlow*", which compares the effectiveness of three natural language generation architectures:
- 🔹 **No-RAG** (standard LLM),
- 🔸 **Simple-RAG** (retrieval from ChromaDB),
- 🔺 **Multi-RAG** (multi-query retrieval pipelines).

Two language models are evaluated:
- `ChatGPT-4o-mini` (OpenAI)
- `Gemini-1.0-pro` (Google DeepMind)

Experiments are conducted using the **SQuAD v2.0** dataset and analyzed with **LangWatch** and **RAGAS** metrics.

---

## 🧪 Architecture Overview

| Approach     | Retrieval | LLM Used         | Tools                      |
|--------------|-----------|------------------|----------------------------|
| No-RAG       | ❌        | GPT4o-mini / Gemini-1.0-pro | LangFlow (no retriever) |
| Simple-RAG   | ✅ (1x)   | GPT4o-mini / Gemini-1.0-pro | ChromaDB + LangFlow     |
| Multi-RAG    | ✅ (3x)   | GPT4o-mini / Gemini-1.0-pro | Multi-query JSON, ChromaDB, LangFlow |

---

## 🔧 Technologies

- **LangFlow**: No-code environment to build LLM pipelines
- **ChromaDB**: Vector database to store document embeddings
- **LangWatch**: Monitor latency, cost, tokens, and performance
- **OpenAI Embedding 3-Small**: For vectorization
- **RAGAS**: For evaluating correctness and relevancy of answers

---

## 📊 Evaluation Metrics

- **RAGAS Answer Correctness** (F1 Score)
- **RAGAS Answer Relevancy** (cosine similarity of question embeddings)
- **Response Time** (in seconds, per model)
- **LangWatch Logs**: used to debug and validate pipeline steps

---

## 📁 Folder Structure

