flowchart TD

A[Documents] --> B[Clean & Normalize Text]
B --> C[Extract Metadata]
C --> D[Create Document Embeddings]
D --> E[Document Classification]

E --> F[Build Indexes]

F --> G[BM25 Keyword Index]
F --> H[Vector Embedding Index]

Q[User Query] --> R[Run Searches in Parallel]

R --> G1[BM25 Search]
R --> H1[Semantic Vector Search]

G1 --> I[Ranked Results]
H1 --> I

I --> J[Reciprocal Rank Fusion (RRF)]

J --> K[Combined Ranked List]

K --> L[Optional Reranking Model]

L --> M[Select Top Documents]

M --> N[Send Context to LLM]

N --> O[Final Answer]
