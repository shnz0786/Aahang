# Aahang Search  
## Context-Aware Retrieval and Authenticity Verification for Low-Resource Indic Poetry

## Overview
**Aahang Search** is a context-aware information retrieval system designed for Urdu and other low-resource Indic poetry.  
The project addresses common challenges in poetic recall, where users remember only fragments of a verse, make spelling errors, or use transliterated forms. Traditional keyword-based search systems often fail in such scenarios.

Aahang employs vector-space–based text representations and similarity matching to retrieve semantically closer verses from a verified literary corpus, prioritizing authenticity and accuracy over noisy web sources.

---

## Motivation
Indic poetry traditions such as *Ghazal*, *Nazm*, and *Shayari* are largely transmitted through oral and memorized forms. In the digital space, this leads to two major problems:

1. **Fragmented Recall Problem** – Users remember only partial lines or rhyming patterns rather than exact wording.
2. **Authenticity Crisis** – Online poetry sources frequently contain misattributed, corrupted, or unverifiable content.

Aahang Search is motivated by the need to preserve literary heritage while enabling robust, typo-tolerant, and context-aware retrieval.

---

## Core Approach

The system replaces exact keyword matching with similarity-based retrieval:

- Text is normalized and vectorized using **TF-IDF**.
- Queries and documents are compared using **Cosine Similarity**.
- **Character-level N-grams (2–5)** are used to handle spelling errors, transliteration noise, and low-resource language variability.
- All retrieval is performed on a **verified corpus** sourced from trusted literary references.

---

## System Architecture

1. **Data Ingestion**
   - Verified poetry data is structured and stored in a local SQLite database.

2. **Preprocessing**
   - Unicode normalization
   - Text cleaning and tokenization
   - Character-level N-gram generation

3. **Vectorization**
   - TF-IDF vector space construction
   - Sparse matrix optimization

4. **Search & Retrieval**
   - Query normalization and vectorization
   - Cosine similarity scoring
   - Ranked retrieval of closest matches

---

## Key Features

- Context-aware verse retrieval  
- Typo-tolerant and transliteration-robust search  
- Fragmented memory recall support  
- Rhyme (Radif)–based matching  
- Authenticity-first corpus design  
- Fully offline, local execution  

---

## Technologies Used

- Python  
- Natural Language Processing (NLP)  
- TF-IDF Vectorization  
- Cosine Similarity  
- Character-level N-grams  
- SQLite  
- Unicode Normalization  

---

## Project Status

This project was developed as an **academic and research-oriented system**.  
Current limitations include:

- Lexical (non-semantic) similarity only  
- In-memory vector space constraints for very large corpora  
- Command-line interface (CLI) only  

---

## Future Work

Planned and proposed enhancements include:

- Integration of **semantic models (e.g., IndicBERT)** for meaning-based retrieval  
- Cross-lingual query support  
- Web-based or mobile user interface  
- Disk-based indexing for large-scale archives  

---

## Academic Context

This project is intended for academic use in areas such as:

- Natural Language Processing  
- Information Retrieval  
- Low-Resource Language Processing  
- Digital Humanities  

The repository is structured to support reproducibility, evaluation, and further research development.

---

## License
This project is shared for **academic and research purposes**.  
License information can be added as required.

---

## Author
**Serajul Haque**  
B.Sc. Data Science  
Interests: NLP, Information Retrieval, Low-Resource Languages
