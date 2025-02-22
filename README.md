![Python](https://img.shields.io/badge/-Python-black?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas)
![Matplotlib](https://img.shields.io/badge/-Matplotlib-black?style=flat-square&logo=matplotlib)
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy)
![scikit-learn](https://img.shields.io/badge/-Scikit--learn-F7931E?style=flat-square&logo=scikitlearn)

## Tech Stack  
- **Languages & Tools:** Python, Pandas, scikit-learn, Matplotlib  
- **Libraries:** NumPy, Pandas, scikit-learn  

## Features  
- **Regression Models:** Built univariate, multivariate, and polynomial regression models to predict viewership with up to 72% explained variance (R²).  
- **Outlier Detection:** Enhanced model accuracy by identifying and addressing outliers, resulting in a 34% improvement in Residual Sum of Squares (RSS).  
- **Data Visualizations:** Created insightful graphs (e.g., bar graphs, scatter plots) to highlight trends like high-performing video categories.  
- **Actionable Insights:** Identified predictors like "likes" and "comment counts" as key factors for maximizing engagement.  

## Architecture  
The project follows a structured data analysis pipeline:  

1. **Data Loading and Preparation:**  
   - Imported datasets and performed initial cleaning (handling missing values, scaling).  
2. **Model Development:**  
   - Built and compared multiple regression models to identify the best predictors.  
3. **Visualization and Insights:**  
   - Visualized relationships between metrics and provided actionable recommendations.  
4. **Evaluation and Iteration:**  
   - Used R-squared, MSE, and RSS to refine models and improve predictions.  

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Regression Models for YouTube Views Prediction

### Objective: To gain actionable insights from YouTube data. We aim to identify the most influential metrics and popular categories.

- [Univariate Regression](#Univariate)
- [Univariate Regression / No Outliers](#Univariate2)
- [Multivariate](#Multivariate)
- [Polynomial](#Polynomial)
- [Comparison, Interpretation and Recommendation](#Comparison)


```python
# Import libraries and set up environment


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
# Set Pandas display options to show numbers in a more readable format
pd.options.display.float_format = '{:.2f}'.format
from sklearn.preprocessing import scale, PolynomialFeatures
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
from sklearn.metrics import confusion_matrix, accuracy_score, precision_recall_fscore_support, roc_auc_score
from sklearn.preprocessing import LabelEncoder

%matplotlib inline
plt.style.use('ggplot')


```

## Data Loading and Description

We begin by loading our dataset, which comprises various metrics from YouTube videos, including likes and views, to understand the average interaction metrics and their distributions.

## Initial Analysis

We perform an initial analysis to get descriptive statistics, which gives us insights into the mean, standard deviation, and range of views, likes, and other engagement metrics. This analysis will influence our models and preparation.

- A description of the data is provided here. What it shows is high variance and large numbers. We will see what that reveals, its impact on our model, and potential actions we will take. We will iterate with other models after our Linear Regression
    


```python
# Load the provided youtube data and display the first five rows of data.
youtube = pd.read_csv('CAvideos.csv')

youtube.head()
youtube.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>category_id</th>
      <th>views</th>
      <th>likes</th>
      <th>dislikes</th>
      <th>comment_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>40881.00</td>
      <td>40881.00</td>
      <td>40881.00</td>
      <td>40881.00</td>
      <td>40881.00</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>20.80</td>
      <td>1147035.91</td>
      <td>39582.69</td>
      <td>2009.20</td>
      <td>5042.97</td>
    </tr>
    <tr>
      <th>std</th>
      <td>6.78</td>
      <td>3390913.02</td>
      <td>132689.53</td>
      <td>19008.37</td>
      <td>21579.02</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.00</td>
      <td>733.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>20.00</td>
      <td>143902.00</td>
      <td>2191.00</td>
      <td>99.00</td>
      <td>417.00</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>24.00</td>
      <td>371204.00</td>
      <td>8780.00</td>
      <td>303.00</td>
      <td>1301.00</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>24.00</td>
      <td>963302.00</td>
      <td>28717.00</td>
      <td>950.00</td>
      <td>3713.00</td>
    </tr>
    <tr>
      <th>max</th>
      <td>43.00</td>
      <td>137843120.00</td>
      <td>5053338.00</td>
      <td>1602383.00</td>
      <td>1114800.00</td>
    </tr>
  </tbody>
</table>
</div>



## Data Preparation:

- We use the number of likes as our single predictor variable to fit a linear regression model.
- We split our dataset into two halves, one for training and one for testing our model.
- We scale the data for better interpretibility since the numbers are very large.

## Univariate Regresssion Model:
<a id='Univariate'></a>


```python
# Univariate Regresssion Model
mid = len(youtube) // 2

X = youtube['likes'].values[:, np.newaxis]
y = youtube['views'];
# scale data down for better readability/interpretability
scaledViews = scale(y)
y = scaledViews
X_train = X[0:mid]
X_test = X[mid:]

y_train = y[0:mid]
y_test = y[mid:]

linmod = LinearRegression()

linmod.fit(X_train, y_train)

preds = linmod.predict(X_test)
```

## Visualization

- We visualize the predicted versus actual values of views using a scatter plot to assess the model fit. We see a clear positive correlation but outliers as well


```python
plt.scatter(y_test, preds,color='g')
plt.xlabel("Actual y Value")
plt.ylabel("Predicted y Value")
plt.title("Linear Regression Model")
plt.show()
```


    
![png](Project_files/Project_7_0.png)
    


## Model Evaluation


```python
print(linmod.intercept_)
print(linmod.coef_)
```

    -0.27628730769235516
    [6.85656107e-06]
    

- We calculate the residuals, R-squared, and Mean Squared Error (MSE) on the test set to evaluate model performance.


```python
# evaluate
# Calculate residuals
rss = sum((y_test - preds) ** 2)
print(f"RSS = {rss:.3e}")

# Calculate R-squared
rs = r2_score(y_test, preds)
print(f"RS = {round(rs, 3)}")

# Calculate MSE
mse = mean_squared_error(y_test, preds)
print(f"MSE = {round(mse, 3)}")

# Model with all categories
```

    RSS = 6.384e+03
    RS = 0.655
    MSE = 0.312
    

## Interpretation:

The R-squared value of 0.65 suggests that 65% of the variance in the views can be explained by the likes. The issue is this doesn't tell the whole story about how the data is affecting video views.

### Outliers and MSE:

The presence of outliers, particularly in data like social media views, will skew the data. The median view count is 371,204 vs the mean view count of 1,147,035.91, our intrepretation of this is that we found what are called 'viral' videos, which have extreme view counts.


## Removing Outliers

- After our initial model we wanted to improve and control for the outliers, when we group the data by category and views,
  we find some interesting data. Two categories are massive outliers on youtube, these are Music and Movies. 


```python
# Probably use this bar graph to show more about the data, that some categories are outliers, 
# suggest a user to focus on thos high view categories for success
# other insights
# gett the mean views per category
categoryViews = youtube.groupby('category_id')['views'].mean()
# sort as desc
categoryViewsSorted = categoryViews.sort_values(ascending=False)
# bar graph
plt.figure(figsize=(15, 10))
categoryViewsSorted.plot(kind='bar')
plt.title('Average Views per Video Category')
plt.xlabel('Video Category')
plt.ylabel('Average Views')
plt.xticks(rotation=45, ha='right')
plt.tight_layout()
plt.show()
# for reference
categoryMapping = {
    "1": "Film & Animation",
    "2": "Autos & Vehicles",
    "10": "Music",
    "15": "Pets & Animals",
    "17": "Sports",
    "18": "Short Movies",
    "19": "Travel & Events",
    "20": "Gaming",
    "21": "Videoblogging",
    "22": "People & Blogs",
    "23": "Comedy",
    "24": "Entertainment",
    "25": "News & Politics",
    "26": "Howto & Style",
    "27": "Education",
    "28": "Science & Technology",
    "30": "Movies",
    "31": "Anime/Animation",
    "32": "Action/Adventure",
    "33": "Classics",
    "34": "Comedy",
    "35": "Documentary",
    "36": "Drama",
    "37": "Family",
    "38": "Foreign",
    "39": "Horror",
    "40": "Sci-Fi/Fantasy",
    "41": "Thriller",
    "42": "Shorts",
    "43": "Shows",
    "44": "Trailers"
}
```


    
![png](Project_files/Project_14_0.png)
    


## Univariate without outliers
<a id='Univariate2'></a>


```python
# SECOND Univariate Regresssion Model

# ##############################
# Filter out outlier category_id 10 and 30
filteredIndices = (youtube['category_id'] != 10) & (youtube['category_id'] != 30)
filteredData = youtube[filteredIndices]

# Update X and y variables
X = filteredData['likes'].values[:, np.newaxis]
y = filteredData['views']
# ##############################
scaledViews = scale(y)
y = scaledViews
mid = len(youtube) // 2
X_train = X[0:mid]
X_test = X[mid:]
y_train = y[0:mid]
y_test = y[mid:]
linmod = LinearRegression()
linmod.fit(X_train, y_train)
preds = linmod.predict(X_test)
# evaluate
rss1 = sum((y_test - preds) ** 2)
rs1 = r2_score(y_test, preds)
mse1 = mean_squared_error(y_test, preds)

# Display the results
print(f"RSS: {rss:.3e} vs{rss1: .3e}. A {((rss - rss1) / rss * 100):.2f}% improvement.")
print(f"MSE: {round(mse, 3)} vs {round(mse1, 3)}. A {((mse - mse1) / mse * 100):.2f}% improvement.")
print(f"RS2: {round(rs1, 3)} vs {round(rs, 3)}. Similar values")

```

    RSS: 6.384e+03 vs 4.204e+03. A 34.15% improvement.
    MSE: 0.312 vs 0.252. A 19.41% improvement.
    RS2: 0.636 vs 0.655. Similar values
    

## What We Found

- Its clear the second model that controls for outliers performs much better to predict the impact of youtube 'likes' on its 'view' count.
- If you want success on Youtube, the data says to put your content in Music/Movie categories, and maximize the 'likes' engagement metric. 





```python


```

## Next Steps - Polynomial Model and Interaction Terms
<a id='Polynomial'></a>
- The last model we will use is another Linear Regression but with interaction terms and polynomial etc etc


```python
# Select featuress and target variable for the model
X = youtube[['likes', 'comment_count', 'dislikes']]
y = youtube['views']

# adding teh interaction terms
poly = PolynomialFeatures(2, interaction_only=True)
polyX = poly.fit_transform(X)
# SCALE IT
scaledViews = scale(y)
y = scaledViews
# DEFINE TRAIN/TEST SETS
X_train = polyX[0:mid]
X_test = polyX[mid:]

y_train = y[0:mid]
y_test = y[mid:]

# FIT THE MODEL
linmod3 = LinearRegression()

linmod3.fit(X_train, y_train)

# DO PREDICTION
preds3 = linmod3.predict(X_test)

plt.scatter(y_test, preds3,color='g')
plt.xlabel("Actual y Value")
plt.ylabel("Predicted y Value")
plt.show()

# MSE and RS function
mse3 = mean_squared_error(y_test, preds3)
rs3 = r2_score(y_test, preds3)
rss3 = sum((y_test - preds3) ** 2)
# Print it
print("RSS:", rss3)
print('Mean Squared Error:',round(mse3, 3))
print('R Squared:',round(rs3, 3))
```


    
![png](Project_files/Project_21_0.png)
    


    RSS: 5417.034573487704
    Mean Squared Error: 0.265
    R Squared: 0.707
    

### Interpretation of Polynomial Model

- Here is what we found and our suggestions from this model etc etc


```python

```


## Next Steps - Multivariate Model
<a id='Multivariate'></a>
To try to capture more complexity and improve predictions, we'll proceed with a multivariate model that includes additional predictors. This will also help us understand the combined effect of multiple engagement metrics on video views and hopefully lead to a better model. 


```python
# Import necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.preprocessing import scale
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# Load dataset
youtube = pd.read_csv('CAvideos.csv')

# Define predictor variables and response variable
X = youtube[['likes', 'dislikes', 'comment_count']]
y = youtube['views']

# Split the dataset into training and testing sets
mid = len(youtube) // 2
scaledViews = scale(y)
y = scaledViews
X_train = X.iloc[:mid]
X_test = X.iloc[mid:]
y_train = y[:mid] 
y_test = y[mid:]  

# Create the linear regression model
linmod2 = LinearRegression()

# Fit the model on the training data
linmod2.fit(X_train, y_train)

# Make predictions on the test data
preds2 = linmod2.predict(X_test)

# Visualize tghe relationship between actual and predicted values
plt.scatter(y_test, preds2, color='blue')
plt.xlabel("Actual Views")
plt.ylabel("Predicted Views")
plt.title("Multivariate Linear Regression Model")
plt.show()

# Output the model's intercept and coefficients
print("Intercept:", linmod2.intercept_)
print("Coefficients:", linmod2.coef_)

# Evaluate the model
rss2 = sum((y_test - preds2) ** 2)
rsq2 = r2_score(y_test, preds2)
mse2 = mean_squared_error(y_test, preds2)

print("RSS:", round(rss2, 3))
print("R-squared:", round(rsq2, 3))
print("MSE:", round(mse2, 3))

```


    
![png](Project_files/Project_25_0.png)
    


    Intercept: -0.2543667977302746
    Coefficients: [ 7.02530954e-06  1.47410331e-05 -1.21136758e-05]
    RSS: 5192.256
    R-squared: 0.719
    MSE: 0.254
    

## Interpretations of Multivariate Model

- Its clear this model performs much better than the single predictor model with 'likes' only, the addition of other engagement metrics like comment count and dislikes captures much more. This model also outperformed the Polynomial and Interaction model with the same features, suggesting x y z

## Which was the best model? A comparison
<a id='Comparison'></a>



```python
# Gather all the evaluation metrics for each model we did.

# print(f"\nUnivariate Model - \n  RSS: {round(rss, 3)}, \n  R-Squared: {round(rs, 3)}, \n  MSE: {round(mse, 3)}")
# print(f"\nUnivariate Model/No Outliers - \n  RSS: {round(rss1, 3)}, \n  RS: {round(rs1, 3)}, \n  MSE: {round(mse1, 3)}")
# print(f"\nMultivariate Model - \n  RSS: {round(rss2, 3)}, \n  R-squared: {round(rsq2, 3)}, \n  MSE: {round(mse2, 3)}")
# print(f"\nPolynomial, Interaction Term Model - \n  RSS: {round(rss3, 3)}, \n  R-Squared: {round(rs3, 3)}, \n  MSE: {round(mse3, 3)}")

```

## Comparisons and Recommendations


**Univariate Model:**
- RSS: 6384.342
- R-Squared: 0.655
- MSE: 0.312
    - Good R-squared value but higher MSE compared to others.
    
**Univariate Model/No Outliers:**
- RSS: 4204.271 (↓34.15% from Univariate Model)
- RS: 0.636 (↓2.90% from Univariate Model)
- MSE: 0.252 (↓19.23% from Univariate Model)
    - Improvement in both RSS and MSE compared to the first model, but slightly lower R-squared.

**Multivariate Model:**
- RSS: 5192.256 (↑23.50% from Univariate Model/No Outliers)
- R-squared: 0.719 (↑13.11% from Univariate Model/No Outliers)
- MSE: 0.254 (↑0.79% from Univariate Model/No Outliers)
    - Best R-squared value and comparable MSE to the no-outliers model, this indicates it explains variance in the data well while maintaining accuracy.
    
**Polynomial, Interaction Term Model:**
- RSS: 5417.035 (↑4.33% from Multivariate Model)
- R-Squared: 0.707 (↓1.67% from Multivariate Model)
- MSE: 0.265 (↑4.33% from Multivariate Model)
    - Similar R-squared to the multivariate model but higher MSE.

<hr>
Comparing the R-squared and MSE of the multivariate model with the other models, it is very clear that the multivariate model is better for predictions of view counts. After conducting these models, the recommendation remains the same: for success on YouTube, focus on content in categories like Music and Movies and optimize engagement metrics such as likes above all else, while also paying attention to comments and minimizing dislikes.

### Winner?

Multivariate Regression Model with [ likes, dislikes, comments ] as predictors


```python

```
