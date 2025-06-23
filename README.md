# Real-Time-Crypto-Market-QA-Assistant

## Project Overview: Crypto-RAG System  
### Goal
- Develop a lightweight, efficient Retrieval-Augmented Generation (RAG) system tailored for real-time cryptocurrency data analysis and question answering.

## Key Features
- Live Data Ingestion (CoinGeckoAPI)
- Fetches up-to-date crypto market information including:
- Prices, Markey and other features of the top 10 cryptocurrency's
- Vector Database Storage
- Transforms and stores data embeddings using FAISS for fast semantic search.
- Local LLM Integration (Phi-3)
- Answers user queries using a locally-run, quantized large language model such as Phi-3
- Optimized for performance with quantization for resource efficiency. (GPU not always available, slower but saves on compute)


## Tech Stack
- LLMs: Phi-3 (Quantized)
- Embedding & Retrieval: FAISS
- Data Sources: Real-time APIs (CoinGecko)

## Use Cases
- On-demand crypto market insights
- Natural language search over live crypto news and metrics
- Local, private LLM-powered assistant for crypto analysis
