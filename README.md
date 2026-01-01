# Project Overview: AI Document Assistant (RAG System)
This project focuses on building an advanced Natural Language Processing (NLP) pipeline that acts as an intelligent assistant for document analysis. By implementing a Retrieval-Augmented Generation (RAG) architecture, the system can answer complex questions based on specific external PDF documents, providing accurate and context-aware responses.

# Part 1 – Document Processing & Vector Search
Objectives:

- Data Ingestion: Implementing a pipeline to load and process unstructured data from PDF files using PyPDFLoader.

- Text Chunking: Utilizing RecursiveCharacterTextSplitter to break down large documents into smaller, semantically meaningful chunks, ensuring the LLM stays within its context window.

- Embeddings Generation: Leveraging pre-trained models from Hugging Face (e.g., sentence-transformers) to convert text chunks into high-dimensional vector representations.

- Vector Database: Implementing FAISS (Facebook AI Similarity Search) as a vector store to enable efficient, high-speed similarity searches across the document's content.

# Part 2 – LLM Integration & RAG Pipeline
Objectives:

- Large Language Model (LLM) Setup: Integrating open-source LLMs through the HuggingFacePipeline (using models such as LaMini-T5 or similar) to generate human-like responses.

- Retrieval-Augmented Generation: Building a RetrievalQA chain that connects the FAISS vector database with the LLM. This ensures the model "reads" the relevant parts of the document before answering.

- Prompt Engineering: Designing custom PromptTemplates to define the assistant's behavior, ensuring it stays focused on the provided context and maintains a helpful, professional tone.

- Inference Pipeline: Creating a seamless flow where a user query triggers a similarity search, retrieves relevant context, and generates a refined answer.
