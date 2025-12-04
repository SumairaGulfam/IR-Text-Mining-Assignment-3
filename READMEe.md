# Information Retrieval System – Evaluation Notebook

This notebook contains a small information-retrieval experiment where different retrieval approaches are tested and compared. The main focus is on building a simple search pipeline, running it on a text collection, and then evaluating how well the system returns relevant documents.

---

## Overview

The workflow in the notebook follows these steps:

1. **Load and prepare the dataset**  
   The dataset is read into memory using pandas. Documents are cleaned, tokenized, and formatted so they can be used by the retrieval models.

2. **Construct a baseline retrieval system (BM25)**  
   The notebook uses the `rank_bm25` package to build a BM25 index.  
   This serves as the baseline ranking method.

3. **Custom search class**  
   A small wrapper class is included that:
   - tokenizes queries  
   - retrieves top-k results  
   - wraps BM25 scoring  
   - returns ranked document IDs  

4. **Evaluation metrics**  
   The notebook computes common IR metrics such as:
   - Precision@k  
   - Recall@k  
   - Hit Rate  
   - Simple accuracy when relevant documents are known  

   The metrics are implemented directly in the notebook for clarity.

5. **Running experiments**  
   A set of queries is passed to the system, and the notebook records:
   - retrieval time  
   - memory usage  
   - ranking results  
   - metric scores  

---

## Requirements

The notebook uses a few basic packages:

```
pandas  
numpy  
rank_bm25  
psutil  
time
```

Install dependencies with:

```bash
pip install rank_bm25 pandas numpy
```

---

## How to Use

1. Open the notebook (in Jupyter or Colab).  
2. Run the installation cell to set up dependencies.  
3. Update the dataset path if needed.  
4. Execute cells from top to bottom.  
5. Review the evaluation results printed at the end.

---

## Output

At the end of the notebook, you will see:

- Overall retrieval performance  
- Per-query metrics  
- Timing information  
- Basic comparison of retrieval behavior  

These results give an idea of how well the retrieval system performs on the dataset.

---


