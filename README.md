# Real-Time-Crypto-Market-QA-Assistant

## Project Overview: Crypto-RAG System  
### Goal
- Develop a lightweight, efficient Retrieval-Augmented Generation (RAG) system tailored for real-time cryptocurrency data analysis and question answering.

## Key Features
### Live Data Ingestion (CoinGecko API)
### Fetches real-time crypto market information for the top 10 cryptocurrencies, including:
- Prices
- Market data
- Other relevant metrics   

### Vector Database Storage (FAISS)
- Converts ingested data into vector embeddings and stores them in FAISS for fast, semantic retrieval.

### Local LLM Integration (Phi-3)
- Answers user queries using a locally-run, quantized large language model (starting with Phi-3).
- Designed to run efficiently on low-resource setups (no GPU)
- Tradeoff: Slower response time, but more compute- and cost-efficient   

### Modular & Flexible LLM Backend
- Swap out Phi-3 with ***Mistral-7B or LLaMA2**, depending on computational resources and task requirements.


## Tech Stack
- LLMs: Phi-3 (Quantized), 
- Embedding & Retrieval: FAISS
- Data Source: CoinGecko API (live market data)

## Use Cases
- On-demand, natural-language insights into current crypto markets
- Fast search and retrieval over real-time market metrics
- Private, local LLM-powered assistant for crypto research and monitoring


## Project Challenges

### Challenges Faced Using Phi-3 for Crypto QA
- ***Prompt Engineering:*** Phi-3 requires clear, consistent prompts. I experimented with multiple prompt formats to improve factual accuracy.
- ***Financial Data Accuracy***: Phi-3 can misinterpret numeric data. I solved this by structuring documents clearly (Market Cap: $...).
- ***No Native Knowledge Retrieval:*** I built a full FAISS-based RAG pipeline using sentence-transformers to feed Phi-3 accurate, live crypto data.
- ***Quantization vs Quality Trade-off:*** Running quantized models improved speed and reduced memory usage in Colab, but required tighter prompt control to maintain answer quality.
