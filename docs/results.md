---
title: Results
layout: default
--- 

# Results

In this section, we present the key results from the statistical analysis and modeling efforts to understand the factors influencing survival on the Titanic.

---

## 1. Principal Component Analysis (PCA)
  
- **PCA Output and Loadings Barplot**:

<img src="images/PCA.jpg" alt="drawing" width="600"/>
<img src="images/PCBargraphs.jpeg" alt="drawing" width="600"/>

From the above PCA output and barplots, we can see that:
    - PC1 is mostly influenced by academic variables such as `MULTIYR_APR_RATE_1000_OFFICIAL`, `MULTIYR_ELIG_RATE`, and `MULTIYR_RET_RATE`. 
    - PC2 is influenced by sport variables: `SPORT_CODE` and `Gender_Sport`
    - PC3 is influenced by school demographics: `CONFNAME_19_numeric` and `SCL_HBCU_numeric`
    - PC4 is influenced by team and school demographics: `MULTIYR_SQUAD_SIZE`, `CONFNAME_19_numeric`, `SCL_PRIVATE_numeric`
Because 4 principal components contribute to a large amount of the variance at 71.7%, we will choose to use 4 principal components for our analysis. 

---

## 2. K Means Clustering


### a. Finding the Right Number of Clusters

<img src="images/ElbowCurve.jpg" alt="drawing" width="600"/>

The Elbow Curve above shows that 2 clusters would be optimal for our analysis.

<img src="images/CH.jpg" alt="drawing" width="600"/>

The CH Index plot shows a maximum at 1, indicating that 1 cluster would be optimal for our data.

<img src="images/GapStat.jpg" alt="drawing" width="600"/>

The Gap Stat plot indicates that we should use 1 cluster for our analysis. 

### b. Testing Cluster Graphs

- **2 Clusters**:

<img src="images/2Cluster.jpg" alt="drawing" width="600"/>

- The plot above shows the 2 cluster k means solution. The clusters are well separated and distinct.

- **3 Clusters**:

<img src="images/3clust.jpg" alt="drawing" width="600"/>

- The plot above shows the 3 cluster k means solution. The clusters are almost equally well separated as the 2 cluster plot, and 3 clusters would give us more information. Therefore, we will use the 3 cluster plot for our analysis.

<img src="images/Contributions3Clust.jpg" alt="drawing" width="600"/>

- The barplot above shows us the contributions of each variable to the cluster centers. A higher positive bar indicates a variable strongly influences that cluster, a low bar indicates little to no influence on that cluster, and a negative bar indicates that the variable is inversely related to that cluster.
- From the plot, we can see that academic variables highly influence all three clusters.
- Interestingly, we also see that gender influences cluster 3 (furthest left, lowest academic scores) positively, and influences cluster 1 (middle, middle academic scores), negatively. This could align with an observation (explained below) that men's sports seem to be, in general, further left on the graph (lower APR scores), and women's sports tend to be further right (higher APR scores). 

### c. Principal Components on Cluster Graphs

- **Dimension 1 Versus Dimension 3**:

<img src="images/Dim1Dim3.jpg" alt="drawing" width="600"/>

- In the plot of principal component 1 versus principal component 3, we see more overlap in clusters than we did in the PC1 versus PC2 graph above. 

- **Dimension 1 Versus Dimension 4**:

<img src="images/Dim1Dim4.jpg" alt="drawing" width="600"/>

In the above plot, we see that there is again more overlap in clusters than there was in the PC1 versus PC2 graph.

- **Dimension 2 Versus Dimension 3**:

<img src="images/Dim2Dim3.jpg" alt="drawing" width="600"/>

In the PC2 versus PC3 plot above, we see the most overlap in clusters (vertical and horizontal overlap), which indicates that PC1 is the most informative in our clustering since this graph is the only one that does not include PC1 and it is has the least defined clusters. Because the graph of PC1 vs PC2 had the clearest clustering, we will use that for the rest of the analysis. 

### d. APR Scores in Each Cluster



## 6. Summary of Key Findings

1. **Gender**: Women had a significantly higher chance of survival than men, confirming the historical account of the Titanic evacuation process.
2. **Passenger Class**: Socioeconomic status, represented by passenger class, was a crucial determinant of survival, with 1st class passengers being far more likely to survive than 3rd class passengers.
3. **Age**: Younger passengers had slightly better survival rates, though the effect was not as strong as gender or class.
4. **Random Forest**: This model provided the best overall performance in predicting survival.

---

## 7. Limitations

- **Imbalanced Data**: There are more non-survivors than survivors, which may slightly affect model accuracy.
- **Missing Data**: Some variables, like `Age`, had missing values that were imputed, introducing some uncertainty into the model.
- **Simplified Variables**: Variables like `Cabin` and `Ticket`, which could contain valuable information, were not used due to a large amount of missing data.

---

## Next Steps

- **Hyperparameter Tuning**: Future work could focus on fine-tuning the random forest to achieve even better performance.
- **Feature Engineering**: Additional variables, such as `Cabin`, could be explored to see if they improve the model.
- **Ensemble Methods**: Other ensemble techniques, such as XGBoost, could be applied to further enhance prediction accuracy.

---






