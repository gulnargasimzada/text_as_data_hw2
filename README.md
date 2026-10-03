#  Raw-Count vs. TF-IDF-Weighted Sentiment Analysis



## Project Overview
This repository contains the replication code and comparative analysis for Homework Assignment Two. The study investigates how transitioning from a conventional raw-count sentiment approach to a document-distinctiveness weighting model (TF-IDF) alters the measured sentiment polarity of two 17th-century economic texts:
* **Text A:** *The Circle of Commerce* by Edward Misselden (1623)
* **Text B:** *Free Trade* by Gerard Malynes (1622)
* An additional 17th-century baseline treatise (`A06785.txt`) is incorporated strictly to calculate the Inverse Document Frequency (IDF) weights across the corpus.

---

## Key Results Summary

| Document | Raw Negative | Raw Positive | Net Sentiment (Raw) | TF-IDF Negative | TF-IDF Positive | Net Sentiment (TF-IDF) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **A07594: Circle of Commerce** | 423 | 491 | **+68** | 86.35 | 63.04 | **-23.31** |
| **B14801: Free Trade** | 281 | 344 | **+63** | 44.19 | 32.70 | **-11.50** |

### Core Finding
Under the raw-count method, both texts evaluate as distinctly positive due to frequent usage of conventional polite markers and broad trade vocabulary (*good*, *great*, *wealth*). However, once words are weighted by TF-IDF, pervasive shared vocabulary is discounted, and unique dispute-related polemical words (*impertinent*, *imperfect*, *meddle*, *imposition*, *disorderly*) drive the net sentiment firmly into negative territory for both treatises.

---

## Repository Contents
* `HW_2.qmd`: Complete Quarto document containing data intake, text tokenization, "long s" normalization, lexicon joins, and matrix computation.
* `final_sentiment_comparison.csv`: Exported summary table containing both raw-count and TF-IDF weighted metrics.
* `*.txt`: Plaintext corpus files used for the assignment.
