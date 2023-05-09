## Cryptocurrency Clustering with K-Means

### Project Overview
This project groups cryptocurrencies using K-Means clustering. We will also compare the clustering results obtained from the original data and the principal component analysis (PCA) data. The project utilizes Python and various data science libraries such as scikit-learn, pandas, and hvPlot to prepare and analyze the data, visualize the results, and draw insights from the clustering analysis.

### Technologies and Methods Used
- Python
- Scikit-learn
- Pandas
- hvPlot
- K-Means clustering
- StandardScaler
- Principal Component Analysis (PCA)
- Elbow method

### Project Description
To start, the data from the CSV file is normalized using the StandardScaler() module from scikit-learn, and a DataFrame with the scaled data is created with the "coin_id" index from the original DataFrame set as the index for the new DataFrame.

Next, the elbow method is used to find the best value for k using the original scaled DataFrame. A list with the number of k values from 1 to 11 is created, and the inertia values are computed with each possible value of k. A line chart is plotted to visually identify the optimal value for k, and the best value for k is then determined.

The cryptocurrencies are then clustered using K-means with the best value for k obtained from the previous task. The K-means model is initialized with the best value for k, fitted using the original scaled DataFrame, and the clusters are predicted. A scatter plot is created using hvPlot to visualize the clustering results.

Principal component analysis (PCA) is performed on the original scaled DataFrame to reduce the features to three principal components. The explained variance is retrieved to determine how much information can be attributed to each principal component, and a new DataFrame with the PCA data is created.

For comparison, the elbow method is used on the PCA data to find the best value for k. The inertia values are computed with each possible value of k, and a line chart is plotted to visually identify the optimal value for k. The best value for k is then determined and the K-means model is initialized with the best value for k, fitted using the PCA data, and the clusters are predicted. A scatter plot is created using hvPlot to visualize the clustering results.

### Conclusion
This project demonstrates how K-Means clustering and PCA can be used to cluster and visualize cryptocurrencies. The elbow method is used to determine the optimal number of clusters, and the clustering results obtained from the original scaled DataFrame and the PCA data are compared. The project showcases the importance of feature selection and data normalization for accurate clustering results.

### Future Work
Future work for this project could involve exploring other clustering algorithms, such as hierarchical clustering or DBSCAN, and comparing their results with those obtained using K-Means clustering. Additionally, other feature selection and dimensionality reduction techniques, such as feature scaling or t-SNE, could be applied to the data to further optimize the clustering results.

Author: Lacey Morgan
