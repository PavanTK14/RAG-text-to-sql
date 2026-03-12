# RAG-text-to-sql
Natural Language to SQL, Generator using Claude 3.5 Sonnet, Titan embeddings, and RAG with guardrails for safe and accurate queries.

NL2SQL RAG SQL Generator

Convert natural language queries into valid SQL using Retrieval-Augmented Generation (RAG), hybrid prompting, and guardrails.

Features

Multi-source database support: S3 Excel/CSV + PostgreSQL/MySQL/MSSQL

DuckDB in-memory execution for fast queries

Schema chunking for large datasets to optimize LLM context

RAG with Titan embeddings + FAISS for relevant schema retrieval

Claude 3.5 Sonnet for SQL generation with reflection and assumption handling

Guardrails to prevent destructive or invalid SQL

Streamlit UI for interactive query input and results visualization

Maintains query history and similarity search

ARCHITECTURE

User Query
    │
    ▼
Claude Sonnet 3.5  ───► Generates SQL
    ▲
    │
RAG Retrieval ──► FAISS + Titan Embeddings ──► Relevant Schema Chunks
    │
Multi-source DBs (S3 Excel + SQL DB)
    │
DuckDB Execution
    │
    ▼
Query Result & Similar History

Why This Project

This project demonstrates how LLMs can assist SQL generation in real-world scenarios with:

Large, multi-source datasets

Schema retrieval via embeddings

Safe, accurate query generation


RAG ensures only the most relevant schema chunks are used.

Guardrails block destructive SQL.

Chunking handles large schemas and token limits.
