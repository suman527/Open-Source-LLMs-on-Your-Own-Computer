# Open-Source-LLMs-on-Your-Own-Computer

Building and Deploying a Conversational Chatbot with Meta LLaMA
This repository presents an end-to-end pipeline for developing a Conversational AI Chatbot using the Meta-LLaMA-3.1-8B-Instruct model. The system is designed for low-resource environments, leverages WebAssembly (WasmEdge) for lightweight deployment, integrates a vector database for retrieval-augmented generation (RAG), and demonstrates fine-tuning for domain-specific knowledge using the Alpaca format.

 ## Project Overview
The project is divided into three major phases:

## Project 1: Deploying the LLaMA Model with WasmEdge
We set up the Meta-LLaMA-3.1-8B-Instruct-Q5_K_M.gguf model inside a Docker container using WasmEdge to enable lightweight, efficient, and portable inference via WebAssembly.

✅ Pulled WasmEdge Docker image

✅ Mounted model and runtime files

✅ Ran inference with llama-simple.wasm

✅ Enabled prompt-based completion generation

## Project 2: Enhancing the Chatbot with Retrieval-Augmented Generation (RAG)
We improved chatbot intelligence by integrating Qdrant (a vector database) to support Retrieval-Augmented Generation (RAG), allowing the model to utilize external structured knowledge for domain-specific queries.

✅ Created a vector store from chemistry.csv

✅ Queried the vector DB using an API

✅ Connected API responses to the chatbot UI

✅ Deployed the RAG-enhanced chatbot on the web and Discord

## Project 3: Fine-Tuning LLaMA for Political News
We customized the chatbot for the politics domain by fine-tuning the LLaMA model using news headline data. This demonstrated the model's adaptability to specific verticals.

✅ Created dataset: politics.txt, finetune.json

✅ Uploaded dataset to Hugging Face: suman50/Fine_tune_dataset

✅ Fine-tuned the model using Unsloth in Colab: Notebook Link

✅ Hosted the fine-tuned model with inference API + UI

Demonstrated the effectiveness of fine-tuning through chatbot screenshots and accessible endpoints.

 ## Key Features
✅ Lightweight deployment using WasmEdge and GGUF quantized LLaMA models.

✅ Interactive chat interface with prompt completion via LobeChat and Discord.

✅ Knowledge-aware answering using Qdrant-powered RAG APIs.

✅ Fine-tuned model trained on real-world political datasets for improved relevance.

✅ API-first design to facilitate flexible front-end integrations.

## Tech Stack
Meta LLaMA 3.1 8B Instruct (GGUF)

WasmEdge

Docker

Qdrant (Vector DB)

Python FastAPI for RAG API

LobeChat / Chatbot UI

Discord Bot Integration

Unsloth Fine-Tuning


## Conclusion
This project demonstrates how to develop a modular, intelligent conversational agent using Meta’s LLaMA model. It spans from deployment to customization, using cutting-edge tools like WasmEdge, Qdrant, and Hugging Face, with hands-on examples of prompt engineering, RAG, and fine-tuning. The approach is scalable, resource-efficient, and adaptable to diverse domains and interfaces.
