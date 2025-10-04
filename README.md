# RAG System Implementation

A Retrieval-Augmented Generation (RAG) system with advanced features including query rewriting and document reranking.

## Implementation

### Basic RAG Pipeline
1. **Data Loading**: Wikipedia passages → embeddings using SentenceTransformers
2. **Vector Storage**: Milvus database with schema (id, passage, embedding)
3. **Query Processing**: Question → embedding → vector search
4. **Answer Generation**: Context + question → LLM → answer

### Advanced RAG Features
- **Query Rewriting**: Generates multiple query variations for better retrieval
- **Document Reranking**: CrossEncoder model for relevance-based ranking

### Evaluation
- **F1 Score & EM**: Token-level and exact match evaluation
- **RAGAs Metrics**: Faithfulness, Answer Relevancy, Context Precision

## Setup

```bash
pip install -r requirements.txt
```

Set environment variable:
```bash
export OPENAI_API_KEY="your_api_key"
```

## Usage

Run the Jupyter notebook:
```bash
jupyter notebook rag-Starter-Code.ipynb
```

## Key Components

- **Embedding Model**: `all-MiniLM-L6-v2`
- **Vector Database**: Milvus Lite
- **LLM**: GPT5-nano
- **Reranking**: CrossEncoder `ms-marco-MiniLM-L-6-v2`

## Files

- `Data Exploration.ipynb` - Main implementation
- `rag-Starter-Code.ipynb` - Main implementation
- `requirements.txt` - Dependencies
- `rag_wikipedia_mini.db` - Milvus database