# Portfolio-SAS

Visualizing the Wine Quality Red Dataset
This document outlines the data visualization techniques used to explore the Wine Quality dataset, and 
the insights derived from these visualizations. The primary goal is to provide a comprehensive 
understanding of the key factors influencing wine quality.
Data Exploration and Cleaning
• Data Loading: The Wine Quality dataset was loaded into SAS for analysis.
• Data Cleaning: Necessary data cleaning steps were performed, including handling missing values 
and outliers.
Before diving into visualizations, let's see the key variables in the Wine Quality dataset:
• Fixed Acidity: The fixed acidity in the wine
• Volatile Acidity: The volatile acidity in the wine
• Citric Acid: The citric acid in the wine
• Residual Sugar: The residual sugar in the wine
• Chlorides: The chlorides in the wine
• Free Sulfur Dioxide: The free sulfur dioxide in the wine
• Total Sulfur Dioxide: The total sulfur dioxide in the wine
• Density: The density of the wine
• pH: The pH of the wine
• Sulphates: The sulphates in the wine
• Alcohol: The alcohol content in the wine
• Quality: The quality rating of the wine (0-10)
Visualization Techniques
1. Histogram of Quality Ratings
A histogram was created to visualize the distribution of quality ratings.
Creating the Histogram:
Here's the SAS code to create a histogram of the Quality variable:
Histogram Visualization of Wine Quality Ratings
Analyzing the Histogram of Wine Quality Ratings
Key Observations:
• Distribution: The histogram maintains its multimodal shape, with distinct peaks at quality ratings 
of 5, 6, and 7.
• Central Tendency: The median quality rating is likely still around 6, indicating that most wines fall 
within the average or slightly above-average range.
• Range: The overall range of quality ratings might have changed slightly due to outlier removal.
• Skewness: The distribution might have become less skewed or more symmetric depending on 
the specific outliers removed.
2. Scatter Plots Visualizations:
2a. Alcohol vs. Quality: Explore the relationship between alcohol content and quality.
2b. Scatter plot of Alcohol, Quality, and Fixed Acidity: Analyze the relationship between alcohol, fixed
acidity and quality.
2a. Analyzing the Scatter Plot of Alcohol vs. Quality
Key Observations:
• Clustering: The data points tend to cluster around specific quality levels, particularly 5, 6, and 7.
• Limited Overlap: There is limited overlap between the clusters for different quality levels, 
suggesting that alcohol content might be a differentiating factor.
• Outliers: A few outliers are visible, especially at lower quality levels and higher alcohol values.
• Overall Trend: While there is a general trend of higher quality wines having slightly higher 
alcohol levels, the relationship is not perfectly linear.
Interpretation:
• Quality Bands: The clustering around specific quality levels indicates that alcohol content might 
be one of the factors influencing wine quality, but it's not the sole determinant.
• Outliers: The outliers suggest that there might be some wines with unique characteristics or 
production processes that deviate from the general trends.
• Non-Linear Relationship: The scatter plot hints at a potential non-linear relationship between 
alcohol and quality. A more complex model might be needed to capture this relationship 
accurately.
2b. Scatter plot of Alcohol, Quality, and Fixed Acidity: Analyze the relationship between fixed 
acidity, alcohol and quality.
Example of the code below:
Scatter plot of Alcohol, Quality, and Fixed Acidity
Key Observations:
• Clustering: The data points tend to cluster around specific quality levels, particularly 5, 6, and 7, 
regardless of fixed acidity.
• Limited Overlap: There is limited overlap between the clusters for different quality levels, 
suggesting that fixed acidity might not be a strong differentiating factor for overall quality.
• Outliers: A few outliers are visible, especially at lower quality levels and higher alcohol values.
• No Clear Trend: There doesn't seem to be a strong linear relationship between alcohol and 
quality when considering fixed acidity as a grouping factor.
Interpretation:
• Quality is Influenced by Multiple Factors: The scatter plot suggests that wine quality is 
influenced by multiple factors beyond just alcohol and fixed acidity. Other variables might play a 
more significant role.
• Fixed Acidity's Limited Effect: While fixed acidity might contribute to quality, it doesn't seem to 
be a primary driver of the observed quality differences.
• Outliers: The outliers might represent wines with unique characteristics or production processes 
that deviate from the general trends.
3. Heatmap code is shown below to show interactions effects:
A correlation heatmap was generated to visualize the relationships between all variables.
See the code generated in SAS below:
Result of Heatmap Visualization


Analyzing the Correlation Plots
Key Observations:
• Alcohol vs. Quality: The scatter plot shows a general positive correlation between alcohol 
content and quality, with higher alcohol levels associated with higher quality ratings. However, 
there are some outliers, and the relationship is not perfectly linear.
• Fixed Acidity vs. Quality: The scatter plot reveals a weak negative correlation between fixed 
acidity and quality. This suggests that wines with slightly lower fixed acidity might have a slight 
advantage in terms of quality.
• Other Variable Relationships: The other scatter plots show various relationships between the 
variables. Some variables might have stronger or weaker correlations with quality than others.
Interpretation:
• Alcohol as a Key Factor: Alcohol content appears to be a significant factor influencing wine 
quality, with higher alcohol levels generally associated with higher ratings.
• Fixed Acidity's Limited Effect: Fixed acidity has a limited negative impact on quality, suggesting 
that it's not a primary driver of quality.
• Other Variables: The relationships between other variables and quality might be more complex 
and require further exploration.
4. Multivariate Analysis: we are going to use multivariate analysis techniques; specifically;
principal component analysis (PCA) to identify underlying patterns and relationships among 
variables.
Principal Component Analysis) PCA is statistical techniques used to reduce the dimensionality of data by 
combining correlated variables into a smaller set of uncorrelated components. SAS provides several 
procedures to perform these analyses.
Result of the Principal Component Analysis

• Scree Plot: The scree plot shows a rapid decrease in eigenvalues with the first few principal 
components, indicating that a significant amount of variance can be explained by a small 
number of components.
• Variance Explained: The variance explained plot shows that the first two principal components 
capture a substantial portion of the total variance in the data, suggesting that they are effective 
in summarizing the important information.
• Eigenvectors: The eigenvectors (loadings) for each principal component indicate the contribution 
of each variable to that component. You can use these loadings to interpret the meaning of the 
principal components.
Interpreting the Principal Components:
• PC1: Examine the loadings for PC1 to understand the variables that contribute most to this 
component. For example, if variables related to acidity have high loadings on PC1, it might 
suggest that PC1 represents an acidity factor.
• PC2: Analyze the loadings for PC2 to identify the variables that contribute most to this 
component. This might reveal another underlying factor or pattern in the data.
• Subsequent Components: Examine the loadings for subsequent principal components to 
understand the additional factors captured by the analysis.
Analyzing the Scree Plot
Key Observations:
• Steep Descent: The eigenvalues decrease rapidly with the first few principal components.
• Elbow Point: There appears to be an elbow point around the 3rd or 4th principal component.
• Diminishing Returns: Beyond the elbow point, the eigenvalues decrease more gradually.
Interpretation:
• Dominant Factors: The steep descent in the scree plot suggests that a few principal components 
capture a significant portion of the total variance in the data.
• Optimal Number of Components: The elbow point indicates that retaining the first 3 or 4 
principal components might be sufficient to capture most of the important information.
• Diminishing Returns: Beyond the elbow point, adding more principal components would provide 
diminishing returns in terms of explained variance.
Based on the scree plot, it seems that 3 or 4 principal components would be sufficient to capture most of 
the important variation in the Wine Quality dataset. This suggests that the complexity of the data can be 
effectively reduced to a smaller number of dimensions.
Conclusion
• Quality is influenced by multiple factors: Wine quality is not determined by a single variable but 
rather by a combination of factors.
• Alcohol and fixed acidity: While alcohol content and fixed acidity play a role, they are not the 
sole determinants of quality.
• Other variables: Other variables, such as residual sugar, volatile acidity, and pH, also contribute 
to wine quality.
• Dimensionality reduction: PCA can be used to reduce the dimensionality of the data and 
identify the most important factors influencing quality.


