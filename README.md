# RAG Architecture
> [!WARNING]
> Draft version

* Component 1: Data Preparation & Data Ingestion
  * There can be multiple sources for the data: organizational internal systems and external sources (PDF, CSV, etc.), which may be in structured or unstructured formats.
  * The initial step is to retrieve the data from different sources, clean and format it, and then store it into a database (Oracle, MongoDB, etc).
  * Technologies can include ETL tools, Messaging/Streaming systems (like Kafka), or Custom application loaders, etc.

* Component 2: Data Embedding and Storage
  * Convert the data to embeddings using an LLM's embedding model.
  * Store it into a Vector Database ( Index it (e.g., LlamaIndex) for large-scale systems).
  * Tools or Frameworks: LlamaIndex, LLMs (OpenAI/other vendors), Vector Stores (ChromaDB, etc.)

* Component 3: Data Retrieval (Augmented Generation)
  * Retrieve the data based on semantic search.
  * Generate the content by passing the retrieved context and the query to the LLMs.

* Component 4: UI & Application
  * Identity Providers for storing user data (like OKTA/Organizational IDP).
  * Gateways for Authentication, Authorization, Rate Limiting, etc.
  * Server-Sent Events or WebSockets for the Chat application.
    
![RAG Architecture.](https://github.com/tva04/gen-ai-rag/blob/main/RAG_Architecture.jpg)


# RAG Topics

| Feature | Details |
| :--- | :--- |
| [RAG Basics](https://github.com/tva04/gen-ai-rag/blob/main/rag_basics.ipynb) | OpenAI, Embedding, Cosine Similiarity |
| [RAG Using Chroma DB](https://github.com/tva04/gen-ai-rag/blob/main/rag_chromadb.ipynb) | Chroma DB, Embedding, Vector Search |
| [RAG using Chroma DB, LlmaIndex, OpenAI](https://github.com/tva04/gen-ai-rag/blob/main/rag_llamaindex_chromadb_openai.ipynb) | Chroma DB, LLamaIndexing, Vector Search |
