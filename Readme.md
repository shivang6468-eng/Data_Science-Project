# 🛍️ Mall Customer Segmentation using K-Means Clustering

An end-to-end unsupervised machine learning project that segments retail store customers into distinct groups based on their annual income and spending scores, enabling data-driven marketing strategies.

---

## 📌 Project Overview
In modern retail, treating all customers the same leads to wasted marketing budgets and missed sales opportunities. This project applies **K-Means Clustering** to automatically group mall customers based on their purchasing behavior and income levels. By identifying these clusters, businesses can tailor promotions, optimize loyalty programs, and target high-value clients effectively.

---

## 📊 Data Extraction & Description

### Where to Extract the Data
The dataset used for this project is publicly available on Kaggle:
* **Dataset Name:** Customer Segmentation Tutorial in Python
* **Direct Link:** [Kaggle Mall Customer Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
* **File Used:** `Mall_Customers.csv`

### Dataset Features
The dataset contains 200 records with the following 5 attributes:
1. **CustomerID:** Unique ID assigned to the customer.
2. **Gender:** Male or Female.
3. **Age:** Age of the customer.
4. **Annual Income (k$):** Annual income of the customer in thousands of dollars.
5. **Spending Score (1-100):** Score assigned by the mall based on customer purchasing behavior and spending habits.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (`KMeans`)

---

## 🚀 Step-by-Step Project Workflow

### 1. Exploratory Data Analysis (EDA)
* Inspected data types, checked for missing values, and summarized statistical distributions.
* Visualized the relationship between **Annual Income** and **Spending Score** using scatter plots to spot initial clusters.

### 2. Determining Optimal Clusters (The Elbow Method)
* Since K-Means requires the number of clusters ($k$) upfront, we calculated the **Within-Cluster Sum of Squares (WCSS)** for $k = 1$ to $10$.
* Plotted the Elbow curve, which clearly indicated an optimal inflection point at **$k = 5$**.

### 3. Model Training & Visualization
* Trained the K-Means model with $5$ clusters using `init='k-means++'`.
* Mapped the cluster assignments back to the dataset and plotted the cluster centroids alongside customer groups.

---

## 💡 Key Findings & Business Personas

By analyzing the average income and spending scores of each cluster, we decoded 5 distinct customer personas:

| Cluster | Persona Name | Characteristics | Business Strategy |
| :--- | :--- | :--- | :--- |
| **Cluster 0** | Standard Customers | Moderate Income, Moderate Spending | Reliable shoppers; maintain steady, consistent engagement. |
| **Cluster 1** | Careful Spenders | High Income, Low Spending | Cautious with money; target with premium perks or loyalty incentives. |
| **Cluster 2** | Target / VIP Customers | High Income, High Spending | **Most valuable!** Prioritize with VIP rewards and exclusive early sales access. |
| **Cluster 3** | Impulse Buyers | Low Income, High Spending | Heavy spenders relative to earnings; great for flash sales and trendy items. |
| **Cluster 4** | Budget Shoppers | Low Income, Low Spending | Cost-conscious; target with value bundles, discounts, and clearance events. |

---

## 💻 How to Run the Code

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/mall-customer-segmentation.git](https://github.com/your-username/mall-customer-segmentation.git)
   cd mall-customer-segmentation