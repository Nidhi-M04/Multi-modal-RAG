# Multimodal RAG for Text and Image Retrieval

This project implements a **Multimodal Retrieval-Augmented Generation (RAG)** system for the automotive domain, integrating **text and image retrieval** with a generative language model to provide context-aware answers.

The approach is based on the architecture and methodology described in the paper *“Multi-modal RAG for Text and Image Retrieval”* :contentReference[oaicite:0]{index=0}.

---

## Overview

The system combines:
- **CLIP** for image–text embedding alignment
- **Sentence Transformers (MiniLM)** for textual embeddings
- **FAISS** for efficient similarity search
- **LLM-based generation** to synthesize grounded responses

User queries retrieve semantically relevant **vehicle images and specifications**, which are then used to generate coherent, brand-agnostic answers.

---

## Pipeline Stages

1. **Data Acquisition & Consolidation**  
   Standardizes and merges automotive metadata from multiple sources.

2. **Semantic Embedding & Indexing**  
   - Text embeddings via MiniLM  
   - Image embeddings via CLIP  
   - Indexed using FAISS for fast retrieval

3. **Query Processing & Retrieval**  
   User queries are embedded and matched against indexed vectors to retrieve top-K relevant items.

4. **Generative Answer Synthesis**  
   Retrieved context is passed to an LLM to generate natural-language responses grounded in retrieved data.

---

## Dataset

- Automotive data from **Hyundai, Tata, Mahindra, and Maruti Suzuki**
- ~150 car variants
- ~1,500 images with structured JSON metadata
- Stored in compressed format due to size constraints

---

## Results (Summary)

- **Top-1 Accuracy:** 82%  
- **Top-3 Accuracy:** 90%  
- **Top-5 Accuracy:** 94%  
- **Average Retrieval Time:** ~0.32 seconds per query  

These results demonstrate the effectiveness of multimodal fusion over unimodal retrieval :contentReference[oaicite:1]{index=1}.

---

## Notes

- Intended for research, learning, and experimentation.
- Large datasets are managed separately due to GitHub size limits.
- Ensure required models and dependencies are available before execution.


