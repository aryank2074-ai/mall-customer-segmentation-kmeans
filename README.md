# mall-customer-segmentation-kmeans
# 🛍️ Mall Customer Segmentation using K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> **Who are your customers, really?** This project uses unsupervised learning to
> group mall shoppers by **annual income** and **spending behaviour**, then proves
> the segments are meaningful by training classifiers that can predict them
> with **~95% accuracy**.

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Dataset](#-dataset)
- [Workflow](#-workflow)
- [Results](#-results)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Business Insights](#-business-insights)
- [Future Improvements](#-future-improvements)

---

## 🎯 Overview
Customer segmentation helps businesses target the right people with the right
offers. In this project I:

1. Explore and validate the Mall Customers dataset
2. Use the **Elbow Method (WCSS)** to find the optimal number of clusters
3. Apply **K-Means** (k = 5) on *Annual Income* and *Spending Score*
4. Visualize the customer segments
5. Turn the clusters into labels and train **Decision Tree** and
   **Random Forest** classifiers to verify that the segments are learnable

## 📊 Dataset
**Mall_Customers.csv** – 200 customers

| Feature | Description |
|---|---|
| `CustomerID` | Unique customer ID |
| `Gender` | Male / Female |
| `Age` | Customer age |
| `Annual Income (k$)` | Yearly income in thousand dollars |
| `Spending Score (1-100)` | Score assigned by the mall based on spending behaviour |

✅ No missing values  ✅ No duplicate rows

## 🔄 Workflow
Load Data → Data Checks → Select Features (Income, Spending)
→ Elbow Method → K-Means (k=5) → Cluster Visualization
→ Label Encoding + Scaling → Train/Test Split (70/30)
→ Decision Tree & Random Forest → Evaluation


## 📈 Results

**Cluster sizes**

| Cluster | Customers |
|:-:|:-:|
| 0 | 81 |
| 2 | 39 |
| 3 | 35 |
| 4 | 23 |
| 1 | 22 |

**Classifier performance (on held-out 30% test set)**

| Model | Accuracy | Macro F1 |
|---|:-:|:-:|
| Decision Tree | 0.93 | 0.94 |
| Random Forest | **0.95** | **0.96** |

> The high accuracy confirms that the discovered clusters are well-separated
> and consistent.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, scikit-learn
- **Environment:** Jupyter Notebook

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/<aryank2074-a>/mall-customer-segmentation-kmeans.git
cd mall-customer-segmentation-kmeans

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 3. Launch the notebook
jupyter notebook ml_algo_8_Kmeans_cluster_3.ipynb
```

> Make sure `Mall_Customers.csv` is in the same folder as the notebook.

## 💡 Business Insights
The five segments typically look like this (based on income vs. spending):

| Segment | Profile | Suggested Strategy |
|---|---|---|
| 🎯 High income, high spending | Ideal customers | Loyalty programs, premium offers |
| 💎 High income, low spending | Untapped potential | Personalized promotions |
| 🛒 Mid income, mid spending | Core average shoppers | Steady engagement, seasonal deals |
| 🎉 Low income, high spending | Enthusiastic spenders | Discounts, budget-friendly bundles |
| 💤 Low income, low spending | Least engaged | Low-cost outreach only |

## 🔮 Future Improvements
- Include **Age** and **Gender** in the clustering
- Validate k with **Silhouette Score**
- Try **DBSCAN** / **Hierarchical Clustering** for comparison
- Add cluster centroids to the plot
- Deploy as a **Streamlit** app for interactive segmentation

## 🤝 Contributing
Suggestions and pull requests are welcome!

⭐ If you found this useful, consider giving the repo a star!
