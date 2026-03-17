# 🍔 Nutritional Profiling of Fast Food Chains
### DSA-609 Data Science Module — Case Study Mini Project

> **Research Question:** How do fast food nutritional profiles differ across restaurant chains, and can we accurately predict calorie content from other nutritional variables?

---

## 📁 Repository Structure

```
fast-food-nutrition-analysis/
│
├── fast_food_analysis.ipynb   ← Main Jupyter Notebook (all code + outputs)
├── README.md                  ← This file
└── figures/                   ← Auto-generated plots (created on notebook run)
    ├── fig1_calorie_distribution.png
    ├── fig2_avg_calories_by_chain.png
    ├── fig3_items_per_restaurant.png
    ├── fig4_restaurant_nutrients.png
    ├── fig5_correlation_analysis.png
    ├── fig6_scatter_plots.png
    ├── fig7_pca_scree.png
    ├── fig8_pca_loadings.png
    ├── fig9_pca_biplot.png
    ├── fig10_lr_results.png
    ├── fig11_rf_results.png
    ├── fig12_nn_results.png
    └── fig13_model_comparison.png
```

---

## 📊 Dataset

| Property | Details |
|---|---|
| **Source** | [Tidy Tuesday — Fast Food Calories](https://github.com/rfordatascience/tidytuesday/tree/master/data/2018/2018-09-04) |
| **Items** | 515 menu items (513 after cleaning) |
| **Restaurants** | McDonald's, Chick-fil-A, Arby's, Dairy Queen, Burger King, Subway, Taco Bell, Sonic |
| **Variables** | 18 columns: calories, fats, carbs, proteins, vitamins, sodium, etc. |

> **Note:** The notebook loads the dataset directly from GitHub — no manual download needed.

---

## 🔬 Methods Used

| Phase | Techniques |
|---|---|
| **Data Cleaning** | Missing value imputation, name standardisation, deduplication, type casting |
| **EDA** | Histograms, boxplots, bar charts, scatter plots, correlation heatmap |
| **Dimensionality Reduction** | Principal Component Analysis (PCA) with Scree plot and biplot |
| **ML Models** | Linear Regression, Random Forest Regressor, Neural Network (Keras) |
| **Evaluation** | R² Score, Mean Absolute Error (MAE), Mean Squared Error (MSE) |

---

## 📈 Model Results

| Model | R² Score | MAE (kcal) | MSE (kcal²) |
|---|---|---|---|
| **Linear Regression** | **0.992** | **11.73** | **689.83** |
| Neural Network | 0.980 | 23.09 | 1,298.94 |
| Random Forest | 0.960 | 28.50 | 3,626.15 |

✅ **Linear Regression** was the best performer across all metrics.

---

## 🗝️ Key Findings

- **McDonald's** has the highest average calorie count (~640 kcal) and leads in protein and sodium
- **Chick-fil-A** is the lowest-calorie chain (~384 kcal avg), offering the most nutritionally balanced menu
- **Total fat** is the strongest predictor of calorie content (r = 0.90)
- PCA shows that 3 components explain ~80% of nutritional variance, with macronutrients driving PC1

---

## ⚙️ Setup and Installation

### Option 1: Run on Google Colab (Recommended — no setup needed)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/fast-food-nutrition-analysis/blob/main/fast_food_analysis.ipynb)

> Replace `YOUR_USERNAME` with your GitHub username after uploading.

### Option 2: Run Locally

**Requirements:** Python 3.8+

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/fast-food-nutrition-analysis.git
cd fast-food-nutrition-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter

# 3. Launch Jupyter
jupyter notebook fast_food_analysis.ipynb
```

---

## 📚 References

- Chollet, F. (2018). *Deep Learning with Python*. Manning Publications.
- Géron, A. (2023). *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (3rd ed.). O'Reilly Media.
- IBM. (2023a). *Data Analysis with Python*. Coursera. https://coursera.org/verify/RYUZRMMCAC6Z
- IBM. (2023b). *Machine Learning with Python*. Coursera. https://coursera.org/verify/3JRM9Z4F6C24
- McKinney, W. (2022). *Python for Data Analysis* (3rd ed.). O'Reilly Media.
- VanderPlas, J. (2017). *Python Data Science Handbook*. O'Reilly Media.

---

*DSA-609 Data Science Module | March 2026*
