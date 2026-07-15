CodeAssist - An AI assistant that understands an entire software repository and helps developers navigate, debug, explain, and modify code using Hybrid RAG.

High-Level Architecture:

                    GitHub Repository
                           │
                Clone / Fetch Repository
                           │
        ┌──────────────────┴──────────────────┐
        │                                     │
 Parse Code                         Parse Documentation
(AST, symbols)                      (README, docs)
        │                                     │
        └──────────────────┬──────────────────┘
                           │
                 Intelligent Chunking
                           │
          ┌────────────────┴───────────────┐
          │                                │
     BM25 Index                    Vector Database
          │                                │
          └──────────────┬─────────────────┘
                         │
                   Hybrid Retrieval
                         │
                    Cross-Encoder
                       Reranker
                         │
                    Context Builder
                         │
                        LLM
                         │
                    Final Answer

Technology Stack
Backend:
1. Python
2. FastAPI
Embeddings:
1. BAAI/bge-large-en-v1.5
2. NVIDIA NV-Embed
3. Jina embeddings
Vector DB:
1. FAISS 
Keyword Search:
1. BM25
2. Elasticsearch
3. OpenSearch
4. Whoosh (simpler)
LLM:
1. Qwen
2. Llama
3. DeepSeek
4. Mistral
Parsing:

Supported languages:

Python
Java
C++
JavaScript
TypeScript
Go