# 🗺️ Customer Persona Map

**Visualize and segment mall customers using K‑Means + PCA for actionable persona insights**

---

## 🚀 Overview

**Customer Persona Map** is an intuitive, unsupervised machine learning project that uncovers meaningful customer groups from mall demographic and spending data. By combining **PCA** (for dimensionality reduction and visualization) with **K-Means clustering**, you’ll generate clear, interpretable customer personas—perfect for targeted marketing, product prioritization, or personalization strategies.

---

## 🔍 Why This Project Matters

- **Business-Driven**: Reveals segments like “Young High-Spenders” or “Budget-Conscious Seniors” for data-driven decision-making.  
- **Clear Visuals**: Easy-to-understand 2D persona maps using PCA.  
- **Unsupervised Mastery**: Practical implementation of clustering techniques without labels.  
- **Beginner → Advanced**: Covers preprocessing, scaling, model evaluation, profiling, and result export.

---

## 🗄️ Dataset

- **File**: `Mall_Customers.csv`  
- **Sources**: Public Kaggle datasets ([e.g., here](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python))  
- **Features**: 
  - Gender (Male=0, Female=1)  
  - Age  
  - Annual Income (k$)  
  - Spending Score (1–100)

---

## 🛠️ Tech Stack

- **Platform**: Google Colab (runs entirely in the browser)  
- **Libraries**: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

---

## 🔬 Methodology

1. **Load & Clean**  
   - Convert gender, drop irrelevant columns  
2. **Scale Data**  
   - Use `StandardScaler` for normalized inputs  
3. **Apply PCA**  
   - Reduce 4D to 2D for visualization and speed  
4. **Cluster Selection**  
   - Optimize *k* using Elbow Method + Silhouette Score  
5. **K-Means Clustering**  
   - Segment data into intuitive groups  
6. **Persona Mapping**  
   - Plot clusters on 2D PCA space  
7. **Cluster Profiling**  
   - Summarize age, income, spending averages  
8. **Export Results**  
   - Save CSVs for integration into reports or dashboards

---

## 📈 Notable Output

| Cluster | Avg Age | Avg Income (k$) | Avg Spending | Persona Description           |
|:-------:|:--------:|:----------------:|:-------------:|:------------------------------|
| 0       | 23      | 62               | 78            | Young, high spenders           |
| 1       | 45      | 85               | 32            | High-income, low-spenders (upsell target) |
| ...     | ...     | ...              | ...           | ...                            |

---

## 📦 Repository Structure
```

├── data/
│ └── Mall_Customers.csv
├── segmentation.ipynb
├── results/
│ └── Customer_Segmentation_Result.csv
└── README.md
```

---

## 🚀 Quick Start

1. Clone or download the repo  
2. Open `segmentation.ipynb` in Colab or Jupyter  
3. Run through the cells (clear code + commentary)  
4. Customize the number of clusters or add features  
5. Download final output CSV with:
```python
from google.colab import files
files.download("Customer_Segmentation_Result.csv")
