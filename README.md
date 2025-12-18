# AI-Assisted Lead Intelligence System

This project demonstrates an AI-assisted pipeline to identify, enrich, and rank life-science professionals based on their likelihood to adopt 3D in-vitro models for drug safety and therapy development.

The focus is on **AI reasoning and ranking logic**, not live web scraping.

---

## Problem Statement
Business development teams need a way to prioritize researchers and decision-makers who are most likely to benefit from advanced 3D in-vitro and liver toxicity models.

This project builds a small, explainable system that:
- Identifies relevant leads
- Extracts intent from unstructured text
- Ranks leads by probability to engage

---

## Approach

### 1. Lead Identification
A curated dataset of professional profiles is used, containing:
- Name
- Title
- Company
- Location
- Descriptive text (bio / research focus)

Mock data is intentionally used to focus on logic rather than scraping constraints.

---

### 2. AI-Based Enrichment
Two relevance approaches are demonstrated:
- **Keyword-based matching** (baseline)
- **Embedding-based semantic similarity** using sentence-transformers

Embeddings allow the system to understand meaning beyond exact keywords.

---

### 3. Propensity Scoring
Each lead is scored using a weighted combination of:
- Semantic relevance (AI)
- Role seniority
- Location signal

Scores are normalized into a **0–100 probability** and ranked.

---

### 4. Output
The final output is a business-ready ranked table exported as CSV.

Main submission file:
- `ranked_leads(embeddings_matching).csv`

---

## Files in this Repository

lead_intelligence.ipynb # Main notebook (end-to-end pipeline)
ranked_leads(embeddings_matching).csv
ranked_leads(keywords_matching).csv
linkedin_data.csv # Reference dataset
requirements.txt


---

## Notes
- No supervised ML is used due to lack of labeled intent data.
- LLM-based extraction is demonstrated conceptually for explainability.
- The system is designed to be easily extendable to real APIs.
