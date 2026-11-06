# Customer Segmentation Using K-Means Clustering & PCA

## Project Overview
This project applies Unsupervised Machine Learning to segment customers based on their purchasing behavior using the RFM (Recency, Frequency, Monetary) model.

The goal is to identify meaningful customer groups and provide insights that can support data-driven marketing and business decisions.

## Dataset
- **Source:** [UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)
- **Original Records:** 541,909 transactions
- **Features:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country.

## Project Workflow

1. **Data Loading & Exploration**
   - Loaded the retail dataset.
   - Inspected data types, missing values, and duplicate records.

2. **Data Cleaning**
   - Removed duplicate records.
   - Removed transactions with missing CustomerID.
   - Excluded cancelled invoices.
   - Removed non-positive quantities and unit prices.
   - Created a TotalAmount feature.

3. **RFM Analysis**
   - Recency: Days since the customer's last purchase.
   - Frequency: Number of unique invoices per customer.
   - Monetary: Total amount spent by each customer.

4. **Feature Preparation**
   - Applied Log Transformation using `log1p`.
   - Scaled features using StandardScaler.

5. **Dimensionality Reduction**
   - Applied Principal Component Analysis (PCA).
   - Reduced the feature space to two principal components.
   - The two components explained **93.87%** of the total variance.

6. **Customer Clustering**
   - Used the Elbow Method to help select the number of clusters.
   - Applied K-Means with 4 clusters.

7. **Visualization & Interpretation**
   - Visualized customer clusters using PCA.
   - Compared customer segments using RFM metrics.

## Customer Segments

| Cluster | Customer Segment | Customers |
|---|---|---:|
| 0 | High-Value Loyal Customers | 713 |
| 1 | At-Risk / Inactive Customers | 1,622 |
| 2 | Recent Low-Spending Customers | 837 |
| 3 | Regular Customers | 1,166 |

### Business Insights
- **High-Value Loyal Customers:** Recent, frequent purchasers with high spending.
- **At-Risk / Inactive Customers:** Customers with relatively long periods since their last purchase and low purchasing frequency.
- **Recent Low-Spending Customers:** Recently active customers with relatively low spending.
- **Regular Customers:** Customers with moderate purchasing activity and spending.

These segments can help businesses design targeted marketing campaigns, improve customer retention, and identify valuable customer groups.

## Project Results
- **Cleaned Transactions:** 392,692
- **Unique Customers:** 4,338
- **Number of Clusters:** 4
- **PCA Explained Variance:** 93.87%
- **Missing Values in Final Segmentation:** 0

## Project Structure

```text
Customer_Segmentation_Project/
│
├── Customer_Segmentation.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   └── Online Retail.xlsx
│
└── outputs/
    ├── customer_segments.csv
    ├── cluster_summary.csv
    └── pca_results.csv
```

## Technologies & Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## How to Run

1. Clone this repository.
2. Download the dataset from the official UCI repository.
3. Place `Online Retail.xlsx` inside the `data/` folder.
4. Install the required libraries:

```bash
pip install -r requirements.txt
```

5. Open and run `Customer_Segmentation.ipynb`.

## Output Files
- `customer_segments.csv`: Customer-level RFM values, cluster assignments, and segment labels.
- `cluster_summary.csv`: Summary statistics for each customer segment.
- `pca_results.csv`: PCA coordinates and cluster assignments.

## Author
**Zeinab Samaha**

Data Science Intern | AI Student

[GitHub Profile](https://github.com/ZeinabTalaat)