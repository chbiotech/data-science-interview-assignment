# Drawing Conclusions
Thank you for your interest in joining the CH Biotech team!

This assignment is intended to evaluate your ability to analyze data with a sample scenario that will be similar to real scenarios you may encounter at CH Biotech.

## Requirements
- Your solution should run on Python 3; if you prefer to use another language, please discuss with us first.
- You may use standard libraries, but you should be able to explain what the library is doing, how it works, and why you chose that library to do that function. 
- You should be able to explain the underlying mechanics of each analysis you do, even if a particular analysis was implemented via a library.
- You may not use generative AI tools such as ChatGPT or Copilot for this assignment.
- You should complete this assignment on your own. Your solution should reflect your own work and skill level.

## Problem Background
A multinational agricultural company seeks to evaluate its experimental treatments across multiple fields and their impact on crop yield under varying environmental conditions. The dataset includes longitudinal data collected over three years, requiring extensive processing, advanced statistical analysis, and predictive modeling.

### Datasets
You are provided with the following datasets in the [data](data) folder:
1. [field_data.csv](data/field_data.csv) - Contains daily vegetation index (VI) measurements and environmental variables:
   - **Field**: Field ID
   - **Trt**: Treatment method
   - **Date**: Observation date
   - **Mean**: Vegetation index
   - **Temp (°C)**: Daily temperature
   - **Rainfall (mm)**: Daily rainfall
   - **Soil Moisture (%)**: Daily soil moisture
2. [yield_data.csv](data/yield_data.csv) - Annual crop yield data:
   - **Field**: Field ID
   - **Trt**: Treatment method
   - **Year**: Harvest year
   - **Yield (Y)**: Annual crop yield
3. [metadata.csv](data/metadata.csv) - Describes field characteristics:
   - **Field**: Field ID
   - **Region**: Geographic region (e.g., North America, Europe, Asia)
   - **Soil Type**: Soil classification (e.g., Sandy, Loam, Clay)
   - **Size (ha)**: Field size in hectares

### Tasks
1. **Data Preparation and Cleaning**
   - Merge the datasets using `Field` and `Trt` as keys.
   - Handle missing values:
     - For continuous variables, use interpolation or imputation.
     - For categorical variables, use the most frequent category.
   - Normalize continuous variables (e.g., temperature, rainfall) to account for variability across fields.
2. **Exploratory Data Analysis (EDA)**
   - Perform an EDA to identify patterns in the data:
     - Generate summary statistics for vegetation index, yield, and environmental variables by region and treatment.
     - Plot time series of vegetation index and soil moisture for at least three fields over the three-year period.
     - Use correlation heatmaps to identify relationships among variables.
3. **Advanced Modeling**
   - Feature Engineering
     - Create additional features:
       - Monthly averages for vegetation index, temperature, rainfall, and soil moisture.
       - Cumulative rainfall and soil moisture leading up to the harvest date.
     - Encode categorical variables (e.g., `Region`, `Soil Type`) for modeling.
   - Multilevel Regression Model
     - Build a hierarchical linear regression model to account for:
       - Treatment effects (`Trt`).
       - Regional differences (`Region`).
       - Field-specific variability (random effects).
     - Report the model equation, coefficients, and significance levels.
   - Predictive Modeling
     - Train a predictive model to estimate annual crop yield (`Yield (Y)`) using vegetation index, environmental variables, and metadata.
     - Use the following models:
       - Linear Regression.
       - Random Forest.
       - Gradient Boosting (e.g., XGBoost).
     - Compare model performance using cross-validation (R-squared, RMSE).
4. **Insights and Recommendations**
   - Identify the best treatment (`Trt`) for maximizing yield in each region.
   - Evaluate the impact of environmental conditions (e.g., rainfall, soil moisture) on yield variability.
   - Propose recommendations for improving yield under extreme weather conditions (e.g., drought, high rainfall).
5. **Visualizations**
   - Create the following visualizations:
     - **Time Series Plot**: Vegetation index trends for selected fields.
     - **Boxplot**: Yield distribution across treatments by region.
     - **Feature Importance Chart**: Highlight key drivers of yield variability from machine learning models.
     - **Residual Plot**: For the hierarchical regression model.

## Deliverables
Your deliverables should be delivered as a private Github repository shared with the Github user @chbiotech.

1. **Processed Data**
   - Cleaned and merged datasets
   - Feature-engineered dataset
2. **EDA Report**
   - Summary statistics and visualizations
   - Insights derived from EDA
3. **Model outputs**
   - Regression and machine learning model results, including performance metrics.
4. **Code**
   - Jupyter Notebooks containing your Python 3 code with detailed comments.
5. **Presentation**
   - A PDF or PowerPoint summarizing key insights and recommendations.
6. **README.md**
   - A README file introducing your project, each of the aforementioned deliverables, and any special instructions that are needed to run your solution.

During your interview, you may be asked to demonstrate parts of your solution. For this purpose, we recommend bringing your notebook computer to your interview and ensuring that your solution runs on it.

## Evaluation Criteria
1. **Data Processing**: Accuracy in handling missing data and normalization.
2. **EDA Quality**: Depth of insights and clarity of visualizations.
3. **Modeling Expertise**: Proper application of multilevel regression and predictive modeling.
4. **Interpretation**: Ability to derive actionable insights and provide meaningful recommendations.
5. **Code Quality**: Clean, modular, and well-documented code that follows standard best practices.
6. **Defense**: Ability to defend your project when challenged during the interview, and ability to explain your project and results to an audience who doesn't have a background in data science.
