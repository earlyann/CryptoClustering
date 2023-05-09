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

Next, the elbow method is used to find the best value for k using the original scaled DataFrame. A list with the number of k values from 1 to 11 is created, and the inertia values are computed with each possible value of k. The following line chart was used to visually identify the optimal value for k.

![Screen Shot 2023-05-09 at 8 04 37 AM](https://github.com/earlyann/CryptoClustering/assets/119711479/7167b7ab-ee66-4283-b749-d2ed6b19a983)

The cryptocurrencies are then clustered using K-means with the best value for k obtained from the previous task. The K-means model is initialized with the best value for k which was 4 was we discovered through the elbow method. The model is then fitted using the original scaled DataFrame, and the clusters are predicted. A scatter plot is created using hvPlot to visualize the clustering results.

![Screen Shot 2023-05-09 at 7 53 32 AM](https://github.com/earlyann/CryptoClustering/assets/119711479/143115aa-9c7b-41e2-bd4c-4f2276fee9e6)

Principal component analysis (PCA) is performed on the original scaled DataFrame to reduce the features to three principal components. The explained variance is retrieved to determine how much information can be attributed to each principal component, and a new DataFrame with the PCA data is created.

For comparison, the elbow method is also used on the PCA data. The inertia values are computed with each possible value of k, and a line chart is plotted to visually identify the optimal value for k, which also was 4. 

![Screen Shot 2023-05-09 at 7 50 00 AM](https://github.com/earlyann/CryptoClustering/assets/119711479/6cbf9bd8-ed40-42f8-a375-1e1bdf830506)

A scatter plot is then created using hvPlot to visualize the clustering results. And an additional plot shows the difference between the clustering results from using the full featured data and the PCA data; the PCA results are much tighter and more defined.

![Screen Shot 2023-05-09 at 8 10 16 AM](https://github.com/earlyann/CryptoClustering/assets/119711479/a6f41278-5012-472f-9c6a-e7facb314bdc)


### Conclusion
This project demonstrates how K-Means clustering and PCA can be used to cluster and visualize cryptocurrencies. The elbow method is used to determine the optimal number of clusters, and the clustering results obtained from the original scaled DataFrame and the PCA data are compared. The project showcases the importance of feature selection and data normalization for accurate clustering results.

### Future Work
Future work for this project could involve exploring other clustering algorithms, such as hierarchical clustering or DBSCAN, and comparing their results with those obtained using K-Means clustering. Additionally, other feature selection and dimensionality reduction techniques, such as feature scaling or t-SNE, could be applied to the data to further optimize the clustering results.

Author: Lacey Morgan
