# MovieLens Table Lineage Project

This repository demonstrates how to generate and analyze different versions of the MovieLens 100k dataset using various join operations. We apply Jaccard similarity and Locality-Sensitive Hashing (LSH) to trace the lineage of derived tables back to their original sources, illustrating an efficient approach for data provenance and reproducibility.

## Contents

1. **Introduction**  
   - The MovieLens 100k dataset is used as a case study to explore methods for tracking the provenance of derived tables.
   - We demonstrate how to systematically generate multiple table versions through different types of joins and then use similarity metrics to identify which source tables contributed to each derived table.

2. **Repository Structure**  
   - `benchmark_generation_clean.ipynb`:  
     Jupyter notebook for creating multiple derived tables from the original MovieLens 100k dataset. Various join operations (inner, outer, etc.) are performed to generate these new tables.
   - `analyzer_execution.ipynb`:  
     Jupyter notebook for analyzing the derived tables. Jaccard similarity and LSH are used here to detect table lineage.
   - `main.tex`:  
     LaTeX source file for the paper documenting the project’s motivation, methodology, experiments, results, and future work.

3. **Getting Started**

   ### Prerequisites
   - Python 3.8+  
   - [Pandas](https://pandas.pydata.org/)  
   - [NumPy](https://numpy.org/)  
   - [scikit-learn](https://scikit-learn.org/) (for certain hashing and similarity functions)  
   - [Jupyter Notebook](https://jupyter.org/) (if you want to run the `.ipynb` notebooks interactively)  

   ### Installation
   1. **Clone the repository**:
      ```bash
      git clone https://github.com/MarcoNapoleone/ATCS_HW_2.git
      cd ATCS_HW_2
      ```
   2. **Install required packages**:  
      Create and activate a virtual environment (optional but recommended), then install the dependencies:
      ```bash
      pip install -r requirements.txt
      ```

   ### Data
   - **MovieLens 100k Dataset**  
     Download from [GroupLens](https://grouplens.org/datasets/movielens/100k). Place the `u.data`, `u.user`, `u.item`, and any other required files in the appropriate directory (e.g., `data/`) as referenced by the notebooks.

4. **Usage**

   1. **Table Generation**  
      - Open `benchmark_generation_clean.ipynb` in Jupyter Notebook.  
      - Run each cell sequentially to create multiple derived tables using different join operations.  
      - The generated tables will be stored either in memory (Pandas DataFrames) or exported (if specified in the notebook).

   2. **Lineage Analysis**  
      - Open `analyzer_execution.ipynb`.  
      - Run through the cells to compute Jaccard similarity and apply LSH.  
      - Inspect the outputs to see which original tables were most likely used to produce each derived table.

5. **Project Roadmap**

   - **Extended Datasets**: We may integrate larger versions of MovieLens (e.g., 1M, 10M) to assess scalability.
   - **Additional Similarity Metrics**: Cosine similarity, MinHash, and other advanced techniques could be tested.
   - **Schema Evolution**: Future enhancements may include automatic handling of renamed columns or changed schemas.

6. **Contributing**
   - **Issues**: If you find any bugs or have suggestions, please open an issue.
   - **Pull Requests**: Contributions are welcome. Fork this repo and submit a pull request with your proposed changes.

7. **License**
   - This project is released under the [MIT License](LICENSE.md).  
   - The MovieLens 100k dataset is distributed separately under its own terms, described on the [GroupLens](https://grouplens.org/datasets/movielens/100k) website.

8. **Contact**
   - For any inquiries or further discussion, feel free to reach out via the repository's issue tracker or any contact method you prefer.

---

**Happy analyzing!**
