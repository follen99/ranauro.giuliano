# RAG Chatbot Pipeline

> Automated pipeline to turn any website into a context-aware AI chatbot.

## Overview

This project was developed during my M.Sc. internship at **TycheLab**. The goal was to build a fully automated pipeline that, given any website URL, produces a functioning RAG (Retrieval-Augmented Generation) chatbot without manual data preparation.

## How it works

1. **Scraping** — the pipeline crawls the target website and extracts raw HTML content
2. **Cleaning** — an LLM-based cleaning step removes boilerplate, navigation noise and irrelevant content
3. **Chunking & Embedding** — text is split into semantic chunks and embedded using a sentence-transformer model
4. **Vector Store** — embeddings are stored and indexed for efficient similarity search
5. **Chat Interface** — user queries are matched against the vector store and passed to an LLM with retrieved context

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Scraping | BeautifulSoup / Playwright |
| Cleaning | OpenAI GPT / local LLM |
| Embeddings | sentence-transformers |
| Vector Store | FAISS / Chroma |
| Chat | LangChain + OpenAI |

## Key Features

- **Zero-configuration** — point at any URL and get a chatbot
- **Modular** — each pipeline stage is swappable
- **Quality filtering** — LLM-based deduplication and noise removal before indexing

## Status

Completed as part of M.Sc. internship at TycheLab (2024–2025).
