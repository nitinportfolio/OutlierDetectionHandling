Outliers in machine learning refer to data points that significantly differ from other observations in a dataset. These data points may be unusually high or low compared to the majority of the data and can distort the analysis or modeling process if not handled appropriately.

Outliers can arise due to various reasons, such as errors in data collection, measurement inaccuracies, or genuine extreme values in the underlying phenomenon being studied. It's important to identify and handle outliers to ensure that they don't unduly influence the analysis or the performance of machine learning models.

Here are some common approaches for dealing with outliers in machine learning:

Identifying Outliers:

Visual inspection: Use box plots, scatter plots, or histograms to visually identify data points that lie significantly far from the majority of the data.
Statistical methods: Employ statistical techniques like the z-score, IQR (Interquartile Range), or modified z-score to detect outliers based on their deviation from the mean or median.
Handling Outliers:

Removing outliers: In some cases, outliers can be removed from the dataset. However, this should be done cautiously, ensuring that the outliers are genuinely erroneous or not relevant to the analysis.
Transforming variables: Applying transformations like log transformation, square root transformation, or box-cox transformation can help reduce the impact of outliers on the model.
Winsorizing: Winsorizing involves capping the extreme values by replacing them with the maximum or minimum non-outlier values.
Clipping or capping: Similar to Winsorizing, this involves setting a threshold beyond which any values are capped or replaced.
Modeling techniques robust to outliers: Using machine learning models that are less sensitive to outliers, such as tree-based models (e.g., Random Forest) or robust regression models.
Incorporating Outliers in Analysis:

In some cases, outliers may contain valuable information about the underlying process being studied. It might be appropriate to analyze these outliers separately or consider them in a specific analysis.
Handling outliers is a critical step in the preprocessing of data for machine learning models, as it can significantly affect model performance and the validity of insights derived from the data. The approach to dealing with outliers should be chosen based on the specific context and nature of the data.

Outliers Impact below ML models as they are Weight bases
1) Linear Regression
2) Logistic Regression
3) AdaBoost
4) DeepLearning
Tree based models are not very sensitive to outliers

Remember - In case of Outliers always try to find out the reason. Do we need to remove outliers or do we need to keep them as they signifies something important. Such as Abnormal patient's readings such as BP, Heart Rate, Sugar Levels 

Treating Outliers - 
1) Trimming - Remove outliers - Problem with this approach is it reduce the dataset & benifit is its very fast
2) Capping  - Give outliers max or min values outside threshold 
3) Missing Values - Treat outliers as missing values & treat them accordingly
4) Discretization - Use Buckets methods
1st two are very popular among the ML community

**Detecting Outliers**
- Normal Distribution - IF data is normally distributed
Values less then mean - 3times Std & Values more than mean + 3times std are considered outliers
- Skewed - If data is skewed then we use interquartile proximity rule
Values less then Q1 - 1.5IQR & Values more then Q3+1.5IQR are considered Outliers 
Q1 - 25th Percentile
Q3 - 75th Percentile
IQR - Q3-Q1
- Other Method - Percentile based approach
Outside certail percentile levels - 2.5 & 97.5 etc

Techniques that we will discuss - 
1) ZScore
2) IQR Based Filtering
3) Percentile
4) Winsorization