# Assignment 5:  Visualizing Data Veracity Challenges in Multi-Label Classification

- **Name:** Venkata Sarath Chandra Galla
- **Roll Number:** NS25Z287

## Folder Structure
```
DA5401_A5_Yeast_Assignment/
├── yeast.arff
├── yeast.xml
├── DA5401_A5_Yeast.ipynb
└── requirements.txt
```

## How to Run
1. Place the raw `yeast.arff` file in the same folder as the notebook.  
2. (Optional) Create a fresh environment and install dependencies:
   ```bash
   pip install -r requirements.txt
3. Open **DA5401_A5_Yeast.ipynb** in Jupyter (Notebook or Lab).
4. Run all cells sequentially (top → bottom). Plots and tables will render inline.  

## Notebook Contents
- **Part A:** Preprocessing and setup  
  - Data loading (Yeast dataset), dimensionality check, and feature scaling  
  - Label simplification for visualization (most frequent single/multi-labels + "Other")  

- **Part B:** t-SNE and data veracity inspection  
  - Applied t-SNE with different perplexities (5, 30, 50)  
  - Visualized clusters, outliers, and noisy/ambiguous labels  
  - Identified high-entropy regions as hard-to-learn samples  
  - Quantified embedding quality with KL divergence  

- **Part C:** Isomap and manifold learning  
  - Applied Isomap with different neighborhood sizes (k = 5, 15, 30)  
  - Compared embeddings and reconstruction errors  
  - Computed geodesic/Euclidean ratio to assess manifold curvature  
  - Compared t-SNE vs. Isomap (local vs. global structure) with side-by-side plots  
  - Discussed manifold complexity and its impact on classification difficulty  

- **Final Section:**  
  - Conclusion and recommendations for handling noisy labels, outliers, and complex manifolds  
  - Clear comparison of t-SNE (local clusters) vs. Isomap (global manifold)  
  - Biological interpretation of overlaps and classification challenges  

---

## Reproducibility
- **Random seeds fixed** (t-SNE with `random_state=42`) for consistent results  
- **StandardScaler applied** to ensure fair distance-based comparisons  
- **Multiple hyperparameter sweeps** (perplexity, n_neighbors) included for robustness  
- **Notebook outputs are reproducible** using `yeast dataset` + `requirements.txt`  
- **Cleaned codebase** with inline comments and consistent formatting for readability  
 

