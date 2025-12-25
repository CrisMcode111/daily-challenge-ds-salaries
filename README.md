# daily-challenge-ds-salaries
This repository contains a **daily learning challenge completed during an AI bootcamp**, focused on data preprocessing and exploratory analysis techniques.

Data handling, normalization, PCA and aggregation on DS job salaries dataset.

# Daily Challenge: Data Handling and Analysis in Python

This repository contains my solution to the **Daily Challenge** on data handling and analysis using the *Data Science Job Salaries* dataset.  
The goal was to practice advanced techniques for **normalization, dimensionality reduction, and aggregation** in Python using Pandas and scikit-learn.

---

## Files
- `week2_day3_challenge.ipynb` → Jupyter/Colab notebook with full code and analysis  
- `processed_ds_salaries.csv` (optional) → cleaned and transformed dataset  
- `README.md` → project documentation  

---

## Steps Implemented
1. **Dataset loading**  
   - Imported the dataset (synthetic fallback generated when the original file was unavailable).  

2. **Normalization**  
   - Applied Min-Max scaling to `salary_in_usd`, rescaling all salaries to [0,1].  
   - Ensured fair comparison across different salary ranges.  

3. **Dimensionality Reduction (PCA)**  
   - Performed PCA with 2 components after one-hot encoding categorical variables and standardizing features.  
   - PC1 explained ~42% of variance, PC2 ~21%, together ~63%.  

4. **Aggregation**  
   - Grouped by `experience_level` and computed **mean** and **median** salaries.  
   - Visualized distributions with boxplots.  

---

## Results & Insights
- **Normalization:** Most salaries fell between 40k–120k USD, with a few outliers up to 200k+. After Min-Max scaling, values lie within [0,1].  
- **PCA:** Two components retained ~63% of total variance. Clusters appeared driven by job title and experience level.  
- **Aggregation:**  
  - Entry-level (EN): median ≈ 48,000 USD  
  - Mid-level (MI): median ≈ 80,000 USD  
  - Senior (SE): median ≈ 120,000 USD  
  - Executive (EX): median ≈ 180,000 USD  
  → Salaries increase almost linearly with experience, with Executives earning about double compared to Seniors.  

---

## Tools Used
- Python  
- Pandas, NumPy  
- scikit-learn (MinMaxScaler, PCA)  
- Matplotlib  

---

## Conclusion
This challenge demonstrated how **data preprocessing** (normalization, encoding, outlier handling) and **dimensionality reduction** can simplify analysis while preserving essential patterns.  
Experience level is clearly the strongest driver of salary in this dataset.

