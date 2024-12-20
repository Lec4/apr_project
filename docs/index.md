---
title: "Multivariate Statistical Analysis Final Project" # Title of the page
layout: default # This tells Jekyll to use the default layout (from the theme)
---
# Academic Progress Rate Analysis for NCAA DI Athletes

## Overview

As a student-athlete, I know that balancing academics and athletics is very difficult. Some schools and teams have a harder time keeping their athletes eligible to play (by academic standards) than others. In this project, I wanted to find out what factors might influence academic progress rates, and by extension, retention rates, and whether these rates are similar among all sports at a specific school, or among similar schools (in terms of demographics). 

- **Dataset Source**: [NCAA Website](https://www.ncaa.org/sports/2016/12/14/shared-ncaa-research-data.aspx)
- **Tools Used**: R
- **Statistical Methods**: Principal Component Analysis, K-Means Clustering, Canonical Correlation Analysis

## Objectives 
1. Determine how many clusters to use and what variable(s) influence the clustering the most.
2. Analyze cluster trends in various sports for a few selected schools.
3. Perform CCA and determine which variables have the highest influence on the canonical covariates, as well as the correlation between canonical covariates.

## Table of Contents

- [Data Description](data.md)
- [Methodology](methodology.md)
- [Results](results.md)
- [Conclusion](conclusion.md)
- [Code and Notebooks](https://lec4.github.io/apr_project/)

## Key Findings

1. **Academic Variables Control Clustering**: 
   - I found that academic variables had the most influence on clustering of sports teams. 
   - In the cluster graph, from left to right, average APR scores increased. 

2. **Gender Seems to Have an Effect on Academic Success**:
   - While this has not been proven in a statistically significant way, in the 5 schools that I investigated, only men's sports teams fell in the lowest academic cluster, with women's teams staying in the middle or high academic cluster.
   - This would need to be investigates further for significance, but is an interesting observation. 

3. **Baseball Consistently in Lowest Academic Cluster**:
   - Interestingly, baseball seemed to be the only sport that was in cluster 3 (lowest academic cluster) for all 5 schools that I looked at.
   - This is also not a significant finding without more data, but an interesting observation. 

4. **Academic and Demographic Variables are Highly Correlated in CCA**:
   - Through CCA, I saw that academic and demographic variables were fairly highly correlated. 
   - This would provide reasoning to do factor analysis in the future. 

You can explore the detailed analysis in the sections above. If you're interested in the code or methodology, feel free to check out the [GitHub repository](https://github.com/Lec4/apr_project).

---
## Future Work

Potential extensions of this analysis include:
- Using other clustering methods
- Adding more demographic variables and sports performance variables
- Factor Analysis of the data

---

## Author

Lily Codd <br/>
Williams College, Class of '26

---

## References 
https://www.ncaa.org/sports/2016/12/14/shared-ncaa-research-data.aspx
