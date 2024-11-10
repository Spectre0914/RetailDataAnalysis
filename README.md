# RetailDataAnalysis

Project Overview:

This project focuses on customer segmentation using RFM (Recency, Frequency, and Monetary) analysis and KMeans clustering. The goal is to group customers based on their behavior and spending patterns in order to derive actionable insights that can help businesses optimize marketing strategies, personalize offerings, and improve customer retention.

Dataset:

The dataset used for this project includes customer transaction data with the following columns:

  InvoiceNo: Unique identifier for each invoice
  StockCode: Unique identifier for each product/item
  Description: Description of the item
  Quantity: Quantity of the item purchased
  InvoiceDate: Date and time of the transaction
  UnitPrice: Price per unit of the item
  CustomerID: Unique identifier for the customer
  Country: Country where the customer is located

Steps Involved:

1. Data Preprocessing: The raw dataset was cleaned by removing unnecessary columns such as R_Quartile, F_Quartile, M_Quartile, and RFMScore, leaving only the relevant features: Recency, Frequency, and MonetaryValue.

2. Correlation Analysis: The correlation matrix was calculated to identify the relationships between Recency, Frequency, and MonetaryValue. The results indicated weak correlations between recency and monetary value, and moderate positive correlations between frequency and monetary value.

3. Data Visualization: A scatter matrix (pairplot) was used to visualize the distribution of the three key features. This revealed skewness and outliers, suggesting the need for normalization.

4. Normalization via Log Transformation: To address the skewness, a log transformation was applied to each of the three features (Recency, Frequency, and MonetaryValue), improving their distribution and making them more suitable for clustering.

5. Elbow Method for Optimal Number of Clusters: The Elbow Method was used to determine the optimal number of clusters for KMeans. By plotting the Within-Cluster Sum of Squares (WCSS), we identified that two clusters were the best fit.

6. KMeans Clustering: KMeans clustering was applied with 2 clusters, based on the Elbow Method. The clustering algorithm grouped customers into two segments based on their Recency, Frequency, and MonetaryValue.

7. Cluster Visualization: A pairplot with the clusters highlighted was created to visually interpret the segmentation results. Customers are now divided into segments that can be further analyzed for targeted marketing strategies.

Key Insights:

  Cluster 1 likely represents customers with high engagement (frequent purchases, high monetary value).
  Cluster 2 likely represents customers with low engagement (infrequent purchases, lower monetary value).

Conclusion

This project demonstrates how customer data can be segmented using KMeans clustering after performing necessary data preprocessing and transformation. The segmented groups can then be analyzed to guide decision-making in marketing and customer engagement strategies.
