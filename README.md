# CSL7110 — Assignment 4: Clustering and PageRank

**Name:** Sandesh Suman | **Roll:** M25CSA034

---

## Structure

```
├── Part1_Clustering.ipynb     # Farthest First + K-Means++ on UCI Spambase
├── Part2_WebSearch.ipynb      # Inverted Index + Search Engine + TFIDF
├── Part3_PageRank.ipynb       # PageRank on Spark (small.txt + whole.txt)
└── M25CSA034_CSL7110_Assignment4.pdf   # Report
```

## Parts

**Part 1 — Clustering** (UCI Spambase, 4601 pts, 57 features)
- `readVectorsSeq`, `kcenter` (Farthest First, O(|P|×k)), `kmeansPP` (D² seeding + Lloyd's), `kmeansObj`
- Experiments: KMeans++ on full data vs coreset approach (k1 = 5×k)

**Part 2 — Web Search**
- Built full inverted index: `MySet`, `Position`, `WordEntry`, `PageIndex`, `MyHashTable`, `InvertedPageIndex`, `SearchEngine`
- TFIDF scoring for query ranking; validated against `answers.txt`

**Part 3 — PageRank on Spark**
- Iterative PageRank on RDDs, β = 0.8, 40 iterations
- Validated on `small.txt` (top score ≈ 0.036); ran on `whole.txt` (1000 nodes, 8192 edges)
- Top node: 263 (score 0.00202), Bottom node: 558 (score 0.00003)

## Dependencies

```bash
pip install pyspark numpy matplotlib
```

## Dataset Sources
- Part 1: UCI Spambase (`spambase.data`)
- Part 3: https://github.com/pnijhara/PySpark-PageRank/tree/main/graph
