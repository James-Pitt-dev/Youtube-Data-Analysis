# YouTube Engagement Metrics Analysis

![Python](https://img.shields.io/badge/-Python-black?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas)
![Matplotlib](https://img.shields.io/badge/-Matplotlib-black?style=flat-square&logo=matplotlib)
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy)
![scikit-learn](https://img.shields.io/badge/-Scikit--learn-F7931E?style=flat-square&logo=scikitlearn)

## What It Does  
YouTube Engagement Metrics Analysis is a data analysis project aimed at predicting and understanding factors influencing video viewership. The project evaluates key metrics like likes, dislikes, and comment counts to derive actionable insights for content optimization.  

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

## Results and Insights  
- High-performing categories such as Music and Movies were found to have 30% higher average viewership.  
- Actionable strategies for creators: focus on engagement metrics like likes while targeting popular categories for maximum impact.  

## Notebook  
Explore the full analysis in the Jupyter Notebook: [analysis.ipynb](analysis.ipynb) 
