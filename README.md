# Trusted Enterprise Knowledge Agent

> Ask internal documents anything; get a cited answer, or an honest “I don't know”.

![status](https://img.shields.io/badge/status-planned-lightgrey) ![phase](https://img.shields.io/badge/sprint-Weeks%207--8-blue)

**Category:** RAG & AI Agents · **Domain:** Enterprise · **Stack:** Python · LangGraph · Qdrant · FastAPI · Docker · Cloud

Project 04/08 of my *Data & AI × Business Consulting* portfolio. 🚧 **Design stage, no implementation yet.**

## Overview

A production-grade assistant over company documents (policies, procedures, manuals). The focus is not on “another chatbot” but on what most RAG demos skip: hybrid search with reranking, a proper evaluation benchmark, access control, and monitoring of cost and latency.

## Business problem

Company knowledge is scattered across PDFs, policies, procedures and slide decks. Employees waste time searching, and naive chatbots give confident but unsupported answers.

## Key points

- Ingestion pipeline: parsing PDFs/slides, chunking strategy compared on real metrics
- Hybrid retrieval (vector + keyword) with a reranker, versus a plain vector baseline
- Agent tools: search, fetch document, summarise, compare two policies
- Benchmark of 50–100 questions scoring retrieval precision/recall, groundedness, citation accuracy
- Production layer: authentication, role-based document access, logging, cost and latency tracking
- Deployed demo with a web interface and user feedback (thumbs up/down)

## Planned architecture

```text
Documents
   ↓
Parsing & chunking
   ↓
Embeddings → vector DB  +  keyword index
   ↓
Hybrid retrieval + reranker
   ↓
Agent (search, fetch, summarise, compare)
   ↓
Answer with citations (or "I don't know")
```

## Planned deliverables

- [ ] Ingestion and RAG pipeline
- [ ] Agent with tools
- [ ] Web interface with feedback
- [ ] Evaluation dataset (50–100 questions) and report
- [ ] Auth, role-based access, logging, cost & latency tracking
- [ ] Deployment documentation and architecture diagram

## Success metrics

- Retrieval precision / recall
- Groundedness, citation accuracy, hallucination rate
- Latency and cost per query

## Planned structure

```text
src/{ingestion,retrieval,agent,api}  app/  eval/  deploy/  docs/
```

## Status

- [x] Scope and README
- [ ] Data
- [ ] Implementation
- [ ] Evaluation & business impact
- [ ] Demo and write-up

---

*Author: Amine Charrou · Final-year Data Science & AI engineering student, ENSA Agadir*
