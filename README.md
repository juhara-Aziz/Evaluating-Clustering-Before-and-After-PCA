# Evaluating-Clustering-Before-and-After-PCA

## Principal Component Analysis (PCA)

To reduce the dimensionality of the Wine dataset while preserving as much information as possible, Principal Component Analysis (PCA) was applied using different numbers of principal components.

### PCA Comparison

| PCA Components | Explained Variance (%) | Silhouette Score | Visualization | Recommendation |
|---------------:|-----------------------:|-----------------:|--------------|----------------|
| 2 | 55.00 | **0.56** | Very clear | Good for visualization |
| 3 | 66.53 | 0.40 | Clear | Good balance |
| 4 | 73.60 | 0.40 | Clear | **Best overall** |
| 5 | 80.16 | 0.36 | Less clear | More information retained |

### Discussion

- **2 Components**
  - Explained **55%** of the total variance.
  - Produced the highest Silhouette Score (**0.56**).
  - Generated the clearest 2D cluster visualization.
  - Suitable when visualization is the main objective.

- **3 Components**
  - Increased explained variance to **66.53%**.
  - Silhouette Score decreased to **0.40**.
  - Preserved more information while maintaining clear cluster separation.

- **4 Components**
  - Preserved **73.60%** of the dataset variance.
  - Achieved a Silhouette Score of **0.40**, similar to 3 components.
  - Retained substantially more information without reducing clustering quality.
  - Selected as the **best overall configuration** because it provides the best balance between dimensionality reduction and information preservation.

- **5 Components**
  - Retained **80.16%** of the original variance.
  - Silhouette Score decreased to **0.36**.
  - Although more information was preserved, the cluster separation became less distinct.

### Conclusion

PCA successfully reduced the dimensionality of the Wine dataset while preserving most of its important information.

- **2 components** are the best choice for cluster visualization due to the highest Silhouette Score.
- **4 components** provide the best trade-off between explained variance and clustering performance, making them the preferred option for analysis.
- Increasing the number of components beyond four retained more variance but did not improve clustering quality.
