#Gemma with RAG: A Coffee Shop Chatbot

This project demonstrates how to build an intelligent chatbot for a fictional coffee shop called CoffeeWorld using a Retrieval-Augmented Generation (RAG) architecture. The chatbot leverages the Gemma 3-1B-it language model to provide conversational responses, while using a pre-built knowledge base for accurate, factual information about the cafe.


Key Features:
Conversational AI: Uses the Gemma 3-1B-it model from Google to handle general conversation and provide engaging, human-like responses.


Retrieval-Augmented Generation (RAG): Implements a RAG pipeline to retrieve relevant, factual answers from a structured dataset of frequently asked questions (FAQs). This prevents the model from "hallucinating" and ensures the information provided is correct.


Efficient Vector Search: Utilizes the sentence-transformers library to create embeddings from the FAQ data and uses Faiss for fast and efficient similarity search to find the most relevant answer for a user's query.


Python Notebook: The entire project is contained within a single Jupyter notebook, making it easy to run, understand, and reproduce.


Bilingual Capability: The model can understand both English and other languages, which is useful for serving a diverse customer base.


How It Works:
Gemma Model Setup: The notebook first sets up the Gemma 3-1B-it model for causal language modeling and chat capabilities.


Dataset Loading: A .jsonl file containing a list of input (questions) and output (answers) is loaded into a Pandas DataFrame.


Embedding and Indexing: The input questions from the dataset are converted into numerical vectors (embeddings) using a SentenceTransformer model. These vectors are then stored in a Faiss index for rapid retrieval.


Chat Logic: When a user asks a question, the chatbot first searches the Faiss index to find the most similar question in the dataset. If a high-similarity match is found, the pre-written answer from the dataset is returned, ensuring accuracy. For general conversation or queries not found in the dataset, the Gemma model handles the response.


This project is an excellent example of combining a powerful large language model with an external knowledge base to create a more reliable and domain-specific AI assistant.
