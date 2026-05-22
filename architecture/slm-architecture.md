# BankingSLM – Core Architecture

This document provides a detailed breakdown of the Banking Small Language Model (SLM) architecture, including:

- Data ingestion and preprocessing
- Domain tokenization
- Semantic embedding layers
- Banking ontology graph
- Retrieval-Augmented Generation (RAG)
- SML core model
- Guardrails and compliance filters
- Evaluation and governance layers

## 1. Domain Tokenization
- Banking vocabulary
- ISO 20022 dictionary
- SWIFT/ACH/FedNow fields
- Fraud patterns
- COBOL/Assembler keywords

## 2. Semantic Embeddings
- ISO 20022 → vector embeddings
- Payment flows → graph embeddings
- Legacy code → semantic mapping

## 3. Ontology Graph
Defines relationships across:
- Accounts
- Customers
- Transactions
- Ledgers
- Events
- Exceptions
- Risk indicators

## 4. RAG Layer
- Vector store
- Banking knowledge base
- Exception rules
- Fraud heuristics

## 5. SML Core
- 1B–3B parameter model
- Deterministic decoding
- Explainability layer

## 6. Guardrails
- PII masking
- Compliance filters
- Risk scoring
- Model lineage

## 7. Evaluation
- Domain accuracy
- Semantic alignment
- Regulatory correctness

