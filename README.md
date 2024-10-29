# Distillation Column Sensor Data Analysis and Prediction

### Overview
This project utilizes sensor data from a distillation column to build a predictive model for product composition based on various operational parameters. Through correlation analysis and support vector regression, we aim to predict the mole fraction of key components in the distillate using selected sensor readings. This project incorporates data preprocessing, feature selection, model tuning, and evaluation, resulting in high-performance predictions for distillation column operation optimization.

### Data Source
**Dataset:** [Distillation Column Sensor Data](https://www.kaggle.com/datasets/amarhaiqal/aspen-hysys-distillation-column-data)  
**Author:** Amar Haiqal  
The dataset provides sensor readings from a simulated distillation column environment, including various pressure, temperature, and flow parameters across different column locations.

### Workflow
1. **Data Preprocessing**  
   - Load and inspect the data.
   - Remove constant and redundant features identified by correlation analysis.
   - Standardize inputs to enhance model convergence.

2. **Feature Selection**
   - Select critical sensors (Feed Tray Temperature and Reflux Ratio) based on high correlations with the target output (Mole Fractions TX and HX).
   - Target Variables: Mole Fraction of light (TX) and heavy components (HX) in distillate.

3. **Model Training & Hyperparameter Tuning**
   - Implement Support Vector Regression (SVR) with an RBF kernel.
   - Perform grid search for optimal parameters (`C`, `epsilon`) using cross-validation.

4. **Evaluation**
   - Compute and display Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared (R²).
   - Plot predictions against test data, including smoothed trendlines for visual clarity.

### Results
The tuned SVR model achieved high accuracy in predicting the mole fraction of key distillate components:
- **R-squared (R²):** 0.947
- **Root Mean Squared Error (RMSE):** 0.0019

These metrics confirm the model’s reliability in simulating distillation column outputs based on sensor input.

### Dependencies
This analysis requires the following Python libraries:
```python
numpy, pandas, matplotlib, seaborn, sklearn, mlxtend, tensorflow, keras
```

### Usage
- **Preprocessing:** Run the initial data cleanup, including column removal and correlation checks.
- **Model Training:** Utilize the provided code to fit the SVR model and optimize using grid search.
- **Evaluation:** Use the metrics and plots to assess model performance.

### Visualization
The project includes detailed line plots of the actual vs. predicted mole fractions with smoothing for enhanced trend visibility. These visualizations help assess the model's predictive accuracy effectively.
