# Open-Source-LLMs-on-Your-Own-Computer

Building and Deploying a Conversational Chatbot with Meta LLaMA
This repository presents an end-to-end pipeline for developing a Conversational AI Chatbot using the Meta-LLaMA-3.1-8B-Instruct model. The system is designed for low-resource environments, leverages WebAssembly (WasmEdge) for lightweight deployment, integrates a vector database for retrieval-augmented generation (RAG), and demonstrates fine-tuning for domain-specific knowledge using the Alpaca format.

 ## Project Overview
The project is divided into three major phases:

## Project 1: LLaMA Deployment using WasmEdge and Docker
Focus: Model setup, prompt-based inference, and integration with chatbot UI.

Deployed the Meta-LLaMA-3.1-8B-Instruct-Q5_K_M.gguf model using a WebAssembly runtime (llama-simple.wasm) inside a Docker container powered by WasmEdge.

Ran inference with a command-line prompt to test text generation.

Configured LobeChat to act as a UI frontend using an OpenAI-compatible local API endpoint.

Enabled real-time interaction with the model through a minimalistic chat interface.

Key tools: Docker, WasmEdge, llama-simple.wasm, Meta-LLaMA-3.1-8B, LobeChat.

## Project 2: Augmenting the Chatbot with External Knowledge (RAG)
Focus: Integrating a vector database to enhance factual accuracy.

Created a vector store using Qdrant, and ingested external domain-specific data (e.g., chemistry concepts).

Converted structured data (chemistry.csv) into embeddings and stored it in a vector database for similarity search.

Developed a RAG API server to respond to user questions by combining retrieval and generation.

Built a public-facing web chatbot and a Discord bot, both capable of producing informed answers using the vector knowledge base.

Submitted screenshots of conversations and vector collection API results for validation.

## Project 3: Fine-Tuning the Model with Domain-Specific Data
Focus: Specializing the chatbot for political news content.

Curated a training dataset (politics.txt) with political news headlines.

Formatted the dataset into Alpaca-style JSON (finetune.json) for instruction tuning.

Uploaded the dataset to Hugging Face Datasets.

Fine-tuned the model on Google Colab using the Unsloth framework and shared the training notebook.

Hosted the fine-tuned model on Hugging Face and deployed a public inference API.

Demonstrated the effectiveness of fine-tuning through chatbot screenshots and accessible endpoints.

 ## Deliverables and Artifacts

## Component	Link / Info
🗃️ Dataset (Alpaca-style)	Hugging Face Dataset
📓 Fine-tuning Notebook	Colab Link
🌐 Hosted Fine-Tuned Chatbot	Chatbot URL
📦 Chemistry Vector Snapshot	Included in repo (/snapshots/chemistry.zip)
🤖 Discord Bot	Invite link and screenshots included in documentation

 ## Key Features
✅ Lightweight deployment using WasmEdge and GGUF quantized LLaMA models.

✅ Interactive chat interface with prompt completion via LobeChat and Discord.

✅ Knowledge-aware answering using Qdrant-powered RAG APIs.

✅ Fine-tuned model trained on real-world political datasets for improved relevance.

✅ API-first design to facilitate flexible front-end integrations.

## Use Cases
💬 Education bots that can answer science, history, and current affairs questions.

🧪 Research assistants for querying domain-specific databases.

📰 News summarizers or commentators trained on political data.

💻 Offline/local chatbots for low-infrastructure environments (schools, rural areas).

## Conclusion
This project demonstrates how to develop a modular, intelligent conversational agent using Meta’s LLaMA model. It spans from deployment to customization, using cutting-edge tools like WasmEdge, Qdrant, and Hugging Face, with hands-on examples of prompt engineering, RAG, and fine-tuning. The approach is scalable, resource-efficient, and adaptable to diverse domains and interfaces.
