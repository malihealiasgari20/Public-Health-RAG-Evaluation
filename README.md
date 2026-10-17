# Query-Formulation Sensitivity in Public-Health RAG

**LLM Evaluation | Retrieval-Augmented Generation | Information Retrieval | Statistical Validation**

> **Research status:** Under review at *Discover Artificial Intelligence* (Springer Nature). This is a research portfolio overview, not a published article, clinical system, or public release of the original research materials.

## Research team

- **Malihe Aliasgari** — Kean University (first and corresponding author)
- **Yousef Nejatbakhsh** — Rutgers University
- **Parsa Safaee** — Eindhoven University of Technology

**Manuscript:** *Query-Formulation Sensitivity in Citizen-Facing Public-Health RAG: A Five-Retriever Retrieval Comparison and a Single-Configuration End-to-End Study*

**Journal:** *Discover Artificial Intelligence* (Springer Nature)  
**Status:** Under review (not yet accepted or published)

## Overview

This project studies how question wording and imperfections in a document corpus affect evidence retrieval in a public-health retrieval-augmented generation (RAG) system, and how a single end-to-end RAG configuration handles answer correctness, evidence support, and abstention.

The focus is **reliability measurement and controlled evaluation**, not foundation-model training or clinical deployment.

## Research design

- **Question benchmark:** 108 questions spanning nine public-health topics.
- **Query formulations:** Direct questions, keyword queries, and composite non-expert/underspecified questions.
- **Corpus conditions:** A clean corpus and nine controlled variants involving OCR character substitutions, word deletion, or distractor contamination.
- **Retrieval comparison:** Five configurations, evaluated on all question–formulation–condition combinations (16,200 retrieval observations).
- **End-to-end evaluation:** 3,240 generated answers using one deterministic lexical hash retrieval configuration and one LLM-generation configuration.
- **Human evaluation:** A stratified panel of 1,080 double-rated responses, with adjudication of substantive disagreements.

## Retrieval configurations

| Retrieval configuration | Approach |
| --- | --- |
| Hash384 | Deterministic signed lexical hashing |
| BM25 | Sparse term-based retrieval |
| MedCPT | Biomedical dense retrieval |
| MPNET | General-purpose dense retrieval |
| BM25–MedCPT hybrid | Rank fusion of sparse and biomedical retrieval |

**Study boundary:** The five-retriever comparison measures **retrieval outcomes only**. Answer accuracy, faithfulness, and abstention were evaluated for the **hash-retriever end-to-end pipeline**, not for all five retrievers.

## Evaluation framework

**Retrieval metrics:** Hit@1, Hit@3, and mean reciprocal rank (MRR).

**Answer and evidence metrics:** Human-rated correctness, faithfulness to retrieved passages, and standardized insufficient-evidence abstention.

**Decision-quality measures:** Answer coverage, selective accuracy, selective risk, appropriate/unnecessary abstention, and joint retrieval–answer states.

**Statistical validation:** Repeated-measures analysis with question-level clustering, multiple-comparison control, inter-rater reliability, and sensitivity analyses.

## Research takeaways

- Retrieval performance can depend strongly on the way a question is phrased, with the observed pattern differing across retrieval configurations.
- Measuring answer accuracy alone omits important questions about evidence support and when the system declines to answer.
- Document-damage evaluation should test whether **relevant evidence survives within a retrieved passage**, not merely whether a passage retains the identity of an acceptable source paragraph.

The manuscript discusses these findings as properties of the tested benchmark and systems; it does **not** establish clinical safety or general robustness to corpus degradation.

## Skills illustrated

RAG evaluation, sparse and dense information retrieval, benchmarking, controlled experiments, data-quality testing, human-evaluation protocols, statistical modeling, reproducibility, and evidence-grounded AI assessment.

## Code, data, and release policy

The original benchmark materials, third-party document text, model-run outputs, ratings, and analysis scripts are **not included** in this public portfolio overview. The manuscript describes access during peer review on reasonable request and a version-controlled public repository with an immutable release **upon acceptance**, subject to redistribution restrictions.

This README is a project overview; it is not an executable reproduction package. Public demonstrations or figures will be considered only after coauthor approval, disclosure review, and appropriate licensing/provenance checks. Any future demonstration should be clearly identified as an independent educational example, not the original study implementation.

## Research website

[Malihe Aliasgari — Research Website](https://malihealiasgari20.github.io/)

## Intended use

Research and evaluation only. No medical advice, diagnosis, or clinical decision support is provided.
