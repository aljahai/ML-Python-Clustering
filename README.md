# Wine Quality Clustering Analysis
## Project Overview
This project performs an unsupervised machine learning analysis on a comprehensive wine quality dataset to identify distinct groupings among red and white wines. By utilizing __K-Means Clustering__ and __Principal Component Analysis (PCA)__, the study explores how chemical properties—such as acidity, sulfur dioxide levels, and alcohol content—differentiate various types of wine.
## Dataset
The analysis uses the Wine Quality Dataset (containing both red and white variants), originally sourced from Kaggle.
### Key Features:
* __Type:__ Red or White wine.
* __Acidity:__ Fixed acidity, volatile acidity, and citric acid
* __Sulfur Dioxide:__ Free and total sulfur dioxide levels (preservatives)
* __Chemical Properties:__ Residual sugar, chlorides, density, pH, and sulphates
* __Quality & Alcohol:__ Alcohol percentage and quality rating (output variables)
## Methodology
The project follows a structured data science workflow:
1. __Exploratory Data Analysis (EDA):__ Investigating the distribution and summary statistics of the 6,497 wine samples.
2. __Data Preprocessing:__
    - Mapping categorical 'type' to numeric values.
    - Dropping the 'quality' target variable for unsupervised learning.
    - Feature scaling using _StandardScaler_ to ensure all features contribute equally to the distance metrics.
3. __Dimensionality Reduction:__ Implementing __PCA__ to reduce high-dimensional data for visualization while preserving significant variance.
4. __Clustering:__
    - Determining the optimal number of clusters using the __Elbow Method.__
     - Applying __K-Means Clustering__ to segment the data.
     - Exploring __Hierarchical Clustering__ (Agglomerative) and generating Dendrograms.
## Key Findings
The analysis identified three primary clusters through the Elbow method:
* __Cluster 0 (White Wines):__ Characterized by significantly higher levels of total and free sulfur dioxide, commonly used as preservatives in white wines.
* __Cluster 1 (Red Wines):__ Defined by higher fixed acidity, volatile acidity, and pH levels.
* __Cluster 2 (Body & Texture):__ Distinguished by high alcohol content and lower density, likely separating wines based on their body and texture.
> [!NOTE]
> To run the analysis, ensure you have the following Python libraries installed:
> * _numpy_
> * _pandas_
> * _matplotlib_
> * _seaborn_
> * _scikit-learn_
> * _scipy_
## Future Improvements
__Outlier Management:__ Implementing robust methods to account for data outliers.
__Alternative Algorithms:__ Using density-based clustering like DBSCAN to better evaluate complex data shapes.
__Granularity:__ Performing analysis with $k=4$ to see if further meaningful sub-groups emerge.
