---
title: Methodology
layout: default
--- 
# Methodology

## 1. Data Preprocessing

Before performing any statistical analysis, the data needed to be cleaned and preprocessed. The following steps were taken to prepare the dataset for analysis:

- **Removing Variables**: 
  - There were originally 101 variables in the dataset. I subsetted the data to only include variables from 2019 and ones that were necessary        for analysis.
  - I removed the "SCL_DIV_19" variable, which corresponded to which Division (I, II, or III) a given sport was in in 2019. After filtering          the data to only include Division I teams, this variable was removed as it was no longer needed.

- **Handling Missing Values**: 
  - The `MULTIYR_APR_RATE_1000_OFFICIAL` variable had 15 missing values. These rows were excluded from the analysis.
  - The `MULTIYR_ELIG_RATE` variable had 15 missing values. These rows were excluded from the analysis.
  - The `MULTIYR_RET_RATE` variable had 15 missing values. These rows were excluded from the analysis.
  - The `MULTIYR_SQUAD_SIZE` variable had 15 missing values. These rows were excluded from the analysis.
  - The `PUB_AWARD_20` variable had 41 missing values. These rows were excluded from the analysis.
  
- **Encoding Categorical Variables As Numeric and Feature Engineering**:
  - I created a new variable `Gender_Sport` by filtering the `SPORT_NAME` variable to group men's, women's, and mixed sports into categories.
  - The categorical variables `CONFNAME_19` and `SCL_HBCU` were converted into numeric variables and `SCL_HBCU` was changed from Y/N to 0/1         indicators.

- **Subset and Scale**:
  - In the end of the pre-processing, I subsetted the data to include all numeric variables in order to do K means clustering. 
  - I scaled the data since some variables were measured on different scales than others. 

## 2. Statistical Methods

I employed multiple statistical methods to analyze the relationships between academic and non-academic variables in the data, and understand similarities and differences between different sports/schools based on these variables. The following methods were used:

### a. Principal Component Analysis (PCA)

- **Goal**: To understand which variables contribute to which dimension (principal component) and how many principal components to look at in K Means Clustering.
- **Implementation**: 
  - Principal Component Analysis was run on the scaled dataset, creating bargraphs of the loadings for each component.

- **Results**:
  - **Number of PC's to Use**: 4 principal components explain 72% of the variance. 
  - **Principal Component Variable Contributions**: PC1 is controlled by academic variables, PC2 is sports variables, PC3 is school demographic        variables, and PC4 is team/school demographic variables. 

### b. K Means Clustering

- **Goal**: Decipher which variable(s) influence cluster groupings the most and analyze the cluster location of a few schools/sports. 
- **Implementation**:
  - Create and Elbow Curve, CH Index Graph, and Gap Stat Graph to visualize the optimal number of clusters.
  - Create cluster plot with the optimal number of clusters.
  - Look at bar graph of variable contributions to the clusters and decipher which variables are most influential.
  - Plot different dimensions against each other in cluster plots to see which principal component is most influential on clustering.
  - Overlay different school and sports team names on the points in the cluster plot and analyze. 

- **Results**:
  - **Number of Clusters**: 3 clusters seemed to be most optimal.
  - **Clustering Variable Contributions**: Academic variables, specifically `MULTIYR_APR_RATE_1000_OFFICIAL` contributed most to clustering.
  - **PC Most Influential in Clustering**: PC1 was most influential in clustering.
  - **Trends in Schools/Sports**: 

### c. Canonical Correlation Analysis

- **Goal**: To 
- **Implementation**:
  - 
  - 
  
- **Results**:
  - **Feature Importance**: 

## 3. Limitations

- **Few Demographic Variables**: The dataset did not include that many demographic variables due to confidentiality of the players. We could         have had a better idea of how demographic variables affect academics if there were more to choose from. 
- **Data Doesn't Include Every NCAA Division**: We may have been able to see differences between sports teams more clearly if the schools            differed more. It would be interesting to see this data for all three NCAA divisions rather than just Division I.
- **Optimal Number of Clusters Not Clear**: We used multiple graphs to try to find the optimal number of clusters, but there was not clear           consensus, so th end result was a best guess at the optimal number based on the visualizations. 

---

## Next Steps

- **Other Clustering Methods**: We could try other clustering methods on the data to see if they would better represent non-academic variables       in the clusters.
- **Factor Analysis**: A few of the academic variables were likely highly correlated, so it may help to do factor analysis on the data in the        future.

---

