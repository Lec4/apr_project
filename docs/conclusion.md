---
layout: default   # This tells Jekyll to use the default layout (from the theme)
title: "Conclusion" # Title of the page
---

# Conclusion

## Summary of Findings

This project aimed to analyze the factors that influenced academic success in student-athletes and whether academic success is similar among all sports at a specific school, or among similar schools (in terms of demographics). Through my analysis, I uncovered several key insights:

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

---

## Limitations

While the analysis provided valuable insights, several limitations should be noted:

1. **Few Demographic Variables**:
   - The dataset did not include that many demographic variables due to confidentiality of the players. We could have had a better idea of how demographic variables affect academics if there were more to choose from.
   
2. **Data Doesn't Include Every NCAA Division**:
   - We may have been able to see differences between sports teams more clearly if the schools differed more. It would be interesting to see this data for all three NCAA divisions rather than just Division I.

3. **Optimal Number of Clusters Not Clear**:
   - We used multiple graphs to try to find the optimal number of clusters, but there was not clear consensus, so th end result was a best guess at the optimal number based on the visualizations.

4. **The Variables Measured Very Similar Things**:
   - All of the academic variables measured very similar things, which is a good thing when we are trying to figure out which variables contribute most to the clustering, but could increase the risk of multicollinearity, which would negatively effect the k means clustering and PCA. 

---
## Future Work

Based on the insights gained from this analysis, several avenues for future work could be pursued:

1. **Other Clustering Methods**:
   - We could try other clustering methods on the data to see if they would better represent non-academic variables in the clusters.
   - Hierarchical clustering could provide interesting results.

2. **Add More Demographic Variables and Sports Performance Variables**:
   - Adding more demographic variables could help inform more of the analysis and reasoning for why certain sports were farther or closer away from each other in each cluster.
   - This could also help group schools and sports more accurately.
   - It would be interesting to see if there is a correlation between sports performance (wins/losses) and academic success of a team. 

3. **Factor Analysis**:
   - A few of the academic variables were highly correlated, so it may help to do factor analysis on the data in the future to reduce the risk of multicollinearity having an effect on our analysis.

---
## Final Thoughts

This project provided useful information on the variables influencing academic success of Division I sports teams, using PCA, k means clustering, and CCA to quantify and visualize similar sports teams and variables influencing similarities. It was interesting to see separation of teams by academic variables, but in the future I would like to see which other variables influence academic success in a team, such as a measurement of the team's success in athletics and how that might positively or negatively influence their academics. 

It is also important to note that there could be limitations to this study due to potential multicollinearity (as many variables were highly correlated) and the optimal number of clusters not being clear. 

By exploring additional variables and using new statistical methods, future analyses could improve these results and potentially find more significant observations in the data. 

**Thank you for exploring this analysis! Feel free to check out the [GitHub repository](https://github.com/Lec4/apr_project) for code, data, and further details.**

