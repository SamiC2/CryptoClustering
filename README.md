# CryptoClustering
## By Sami Chowdhury

## Summary
This assignment will be using machine learning and K-Means clustering to look at crypto currency data. I found this assignment to be one of my favorites as it was interesting to cluster the data using K-means to figure out how to best categorize the price changes. Scaling and transforming the data so that it could be clustered without one feature dominating the clusters helped a lot in the analysis. 

I found from my analysis that with the data given, it was best to use 4 clusters for the k-means clustering. This was because after plotting the inertia for values of k, the inertia stopped signficantly decreasing after reaching 4 clusters. This meant that I could reasonably cluster the data with 4 clusters without much room for error.

I also enjoyed completing the Principal Component Analysis to see how much variance in the data could be explained by the features. Seeing the model be built with 3 components helped visualize the data better, and I also found that I was able to cluster the data again in 4 clusters after plotting the PCA model's inertia for a range of values of k. 

Each component had different features that influenced them the most. 

| Feature | PCA1 | PCA2 | PCA3 |
| ------- | ---- | ---- | ---- |
| price_change_percentage_24h | -0.416728 | 0.358162 | -0.218795 |
| price_change_percentage_7d | -0.102432 | 0.227432 | 0.787670 |
| price_change_percentage_14d | -0.009162 | 0.540415 | 0.349534 |
| price_change_percentage_30d | 0.191523 | 0.562182 | -0.181744 |
| price_change_percentage_60d | 0.320365 | 0.434040 | -0.361377 |
| price_change_percentage_200d | 0.594468 | 0.027735 | 0.039733 |
| price_change_percentage_1y | 0.568379 | -0.150789 | 0.210541 |

- **TABLE 1: Principal Component Feature Analysis**

- For example, Principal Component 1 had strong positive influences from the **'price_change_percentage_200d'** feature followed by the  **'price_change_percentage_1y'** feature, so it was more explained by long term change in price values. This makes sense as its strongest negative influence was the **'price_change_percentage_24h'** feature. 
- Principal Component 2 on the other hand was more influenced by biweekly and monthly price change features, namely **'price_change_percentage_30d'** followed by **'price_change_percentage_14d'**. Its strongest negative influence was the long term field **'price_change_percentage_1y'**, indicating that it was influenced more for a monthly and biweekly price change.
- Lastly, Principal Component 3 was mostly influenced by the weekly feature, **'price_change_percentage_7d'**. It was strongly negatively influenced by the features **'price_change_percentage_60d'** followed by **'price_change_percentage_24h'**. This could mean that it strongly was influenced by weekly changes in the price only. 

Overall, it was great exploring this data using K-means clustering. I now feel comfortable building K-means models, analyzing inertia values to determine optimal K values, and utilizing Principal Component Analysis to understand the influence each feature has on the data. 
