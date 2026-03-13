# IQ & GPA Statistical Analysis

A comprehensive exploratory and inferential statistical analysis investigating the relationship between cognitive ability (IQ) and academic performance (GPA).

---

## Dataset Overview

| Column | Description |
|--------|-------------|
| `obs` | Observation ID |
| `gpa` | Grade Point Average (0–4.5 scale) |
| `iq` | IQ score (range: ~70–135) |
| `gender` | Gender (1 = male, 2 = female) |
| `concept` | Conceptual understanding score |

**Sample size:** 78 students

---

## Analyses Performed

1. **Exploratory Data Analysis (EDA)**
   - Distribution analysis
   - Scatter plots and correlations
   - Gender-based comparisons

2. **Correlation Analysis**
   - Pearson correlation between all variable pairs
   - Key finding: IQ–GPA correlation r = 0.6483

3. **Linear Regression — IQ → GPA**
   - Simple OLS regression
   - R² = 0.4203 (IQ explains ~42% of GPA variance)

4. **Residual Analysis**
   - Normality testing
   - Heteroscedasticity assessment

---

## Visualizations

<p align="center">
  <img src="images/Combined_SS.png" alt="EDA Dashboard" width="900">
</p>

### Interpretation

**Distribution of GPA** (Top Left)
- Approximately normal distribution centered at μ ≈ 3.0
- KDE overlay confirms normality assumption

**Relationship between IQ and GPA** (Top Right)
- Strong positive correlation (r = 0.65, p < 0.001)
- Gender shows minimal impact on the relationship
- Linear pattern validates regression approach

**Variable Correlation Heatmap** (Bottom Left)
- IQ is the strongest predictor of GPA (r = 0.65)
- Gender shows near-zero correlation with GPA (r = -0.10)
- Concept score moderately correlates with both IQ and GPA

**GPA Spread by Gender** (Bottom Right)
- Similar median values (~3.0) for both groups
- Comparable variance suggests gender is not a significant factor
- Supports finding that gender correlation is negligible

---

## Key Results

| Metric | Value |
|--------|-------|
| **Pearson r (IQ–GPA)** | 0.6483 |
| **R²** | 0.4203 |
| **p-value** | < 0.001 |
| **Sample size** | 78 |
| **Residual std. dev.** | 0.68 |

---

## Conclusions

The analysis provides strong statistical evidence that **IQ is a significant positive predictor of GPA** (p < 0.001). The linear model is valid:

✅ Residuals are approximately normal and centered at zero  
✅ No strong heteroscedasticity detected  
✅ R² = 0.42 indicates moderate explanatory power

However, with ~58% of GPA variance remaining unexplained by IQ alone, other factors such as study habits, motivation, and conceptual understanding play important roles in academic success.

---

## How to Reproduce
```bash
# Clone the repository
git clone https://github.com/21hanny/EDA_Statistical_analysis.git

# Install dependencies
pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn

# Run the analysis
jupyter notebook analysis.ipynb
```

---

## Files

- `analysis.ipynb` — Main analysis notebook
- `gpa_iq_cleaned.csv` — Dataset
- `images/Combined_SS.png` — Exploratory data analysis visualization

---

## Author

**Sourabh Saini** ([@21hanny](https://github.com/21hanny))
