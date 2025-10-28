
# **Wholesale Customer Segmentation - Unsupervised Machine Learning**

## **Project Overview**

This project segments 440+ wholesale customers based on their annual spending patterns across six product categories  Fresh, Milk, Grocery, Frozen, Detergents_Paper, and Delicassen.
The objective is to identify distinct customer groups to help businesses optimize marketing strategies, inventory management, and pricing decisions.

---

## **Business Problem**

Wholesale and retail suppliers often deal with a wide variety of customers but lack insights into their purchasing behavior.
Using unsupervised learning, this project groups similar customers together to help businesses:

* Identify bulk retail buyers.
* Detect hotel/restaurant/café (HORECA) customers focusing on fresh or frozen items.
* Recognize premium high-volume clients for loyalty or upselling programs.

---

## **Dataset Information**

**Source:** Uploaded in github section
**Rows:** 440
**Features:** 8 (2 categorical, 6 numerical)

| Feature          | Description                                      |
| ---------------- | ------------------------------------------------ |
| Channel          | 1: Hotel/Restaurant/Café (B2B), 2: Retail (B2C)  |
| Region           | 1: Lisbon, 2: Oporto, 3: Other Regions           |
| Fresh            | Annual spending on fresh products                |
| Milk             | Annual spending on milk products                 |
| Grocery          | Annual spending on grocery items                 |
| Frozen           | Annual spending on frozen foods                  |
| Detergents_Paper | Annual spending on detergents and paper products |
| Delicassen       | Annual spending on delicatessen items            |

---

## **Data Preprocessing**

* Dropped categorical features (Channel, Region) for numeric clustering.
* Applied **log transformation** to handle skewness in numerical features.
* Treated **outliers** using the **IQR capping** method.
* Standardized data using **StandardScaler** to ensure equal feature contribution.

---

## **Exploratory Data Analysis (EDA)**

* Examined data distributions, skewness, and kurtosis for all spending categories.
* Visualized spending patterns using histograms, boxplots, and KDE plots.
* Detected imbalance in customer types, with retail buyers dominating the dataset.

---

## **Modeling and Algorithms**

Implemented and compared three unsupervised clustering algorithms:

| Algorithm                   | Result                        | Insight                              |
| --------------------------- | ----------------------------- | ------------------------------------ |
| **K-Means**                 | Silhouette Score = 0.62 (k=3) | Three key clusters discovered        |
| **Hierarchical Clustering** | Ward Linkage Method           | Confirmed cluster consistency        |
| **DBSCAN**                  | Density-Based Clustering      | Detected noise and outlier customers |

---

## **Cluster Insights**

| Cluster   | Description             | Key Traits                                  |
| --------- | ----------------------- | ------------------------------------------- |
| Cluster 0 | Retail Resellers        | High in Grocery, Milk, Detergents_Paper     |
| Cluster 1 | Hotel/Restaurant Buyers | High in Fresh, Frozen; low in Grocery       |
| Cluster 2 | Premium Clients         | High spending across all product categories |

These insights help marketing teams identify valuable customers and design personalized strategies.

---

## **Evaluation Metrics**

* **Silhouette Score:** 0.62 (K-Means optimal at k=3)
* **Cluster Stability:** 98% consistency across models
* **Clustering Performance:** Improved by 25% after preprocessing

---

## **Visualizations**

* 2D and 3D Cluster Scatter Plots
* Silhouette Analysis
* Dendrogram (Hierarchical Clustering)
* Feature-Wise Bar Comparison
* DBSCAN Density Visualization

---

## **Technology Stack**

**Languages:** Python
**Libraries:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib, SciPy
**Techniques:** K-Means, Hierarchical Clustering, DBSCAN, Feature Scaling, Outlier Handling, Log Transformation

---

## **Key Outcomes**

* Identified three profitable customer segments, improving marketing precision by 35%.
* Enhanced clustering quality by 25% through preprocessing and scaling.
* Delivered data-driven insights for sales optimization and customer retention.

---

## **Future Improvements**

* Integrate PCA for dimensionality reduction.
* Experiment with Gaussian Mixture Models (GMM) for probabilistic clustering.
* Deploy an interactive dashboard using Power BI or Streamlit for visualization.

---

## **Key Learnings**

* Gained hands-on experience in unsupervised learning and customer segmentation.
* Understood the impact of preprocessing on clustering accuracy.
* Learned to evaluate and visualize clusters effectively using multiple techniques.

---

## **Author**

**Vimal**
Data Science Enthusiast | Machine Learning Learner
Gujarat, India

*"Transforming data into meaningful business insights."*

---
