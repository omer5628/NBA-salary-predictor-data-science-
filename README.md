# NBA Salary Prediction

## Project Overview
This project aims to predict NBA player salaries based on their performance and statistical data from the 2022-2023 season. By leveraging machine learning models, the project analyzes key player metrics to understand salary drivers and produce accurate predictions. Models such as XGBoost, Random Forest, ElasticNet, and Decision Trees were used, with XGBoost providing the best performance after hyperparameter tuning.

---

## Key Objectives
- Analyze and preprocess NBA player data for accurate modeling.
- Use machine learning models to predict player salaries based on statistics.
- Optimize models using techniques like hyperparameter tuning and cross-validation.
- Visualize findings and feature importance to derive insights into salary determinants.

---

## Dataset
The dataset includes player statistics and salaries for the 2022-2023 NBA season, containing 467 records and 51 features. Key features include:
- **Player Information:** Name, age, position, and seasons played in the NBA.
- **Performance Statistics:** Points per game, rebounds, assists, games played, and minutes played.
- **Target Variable:** Player salary (in millions of dollars).

### Data Processing Steps
1. **Data Cleaning:**
   - Handled missing data by imputing means for numerical variables and modes for categorical variables.
   - Renamed columns for clarity and removed spaces.
2. **Normalization:**
   - Applied log transformation to salary data to reduce the influence of outliers.
   - Used Box-Cox transformations for features with high skewness.
3. **Feature Engineering:**
   - Encoded categorical variables (e.g., position, team) using `LabelEncoder`.
   - Dropped low-correlation features (< 0.2) to improve model focus.
4. **Exploratory Data Analysis (EDA):**
   - Visualized distributions, correlations, and feature relationships with salary.
   - Created scatter plots, histograms, heatmaps, and box plots for deeper insights.

---

## Methodology

### Models Used
- **Linear Regression:** With and without intercept.
- **ElasticNet Regression:** Combines L1 and L2 regularization.
- **Decision Tree and Random Forest:** Captures non-linear relationships.
- **XGBoost:** Gradient-boosted trees optimized for performance.

### Model Evaluation
- **Metric:** Root Mean Squared Error (RMSE) was used to evaluate prediction accuracy.
- **Cross-Validation:** Applied k-fold cross-validation (k=5) to ensure robust performance.
- **Hyperparameter Tuning:** Optimized XGBoost using Bayesian optimization.

---

## Results

### Model Comparison
| Model                | RMSE   | Standard Deviation |
|----------------------|--------|--------------------|
| Linear Regression (no intercept) | ~3.50  | ~0.30              |
| Linear Regression (with intercept) | ~3.40  | ~0.28              |
| ElasticNet           | ~3.20  | ~0.25              |
| Decision Tree        | ~3.60  | ~0.35              |
| Random Forest        | ~3.00  | ~0.22              |
| XGBoost              | ~2.50  | ~0.20              |
| XGBoost (optimized)  | ~2.12  | ~0.03              |

### Feature Importance
Key features influencing salary prediction:
1. **Minutes Played per Game**
2. **Points per Game**
3. **Games Played**

### Insights
- Players with higher playtime and better scoring performance tend to earn more.
- Optimized XGBoost model achieved the best results with minimal error.

---

## Visualizations
- **Salary Distributions:** Analyzed pre- and post-normalization data.
- **Correlation Heatmaps:** Highlighted relationships between features and salary.
- **Box Plots:** Showed salary distributions across player positions.
- **Scatter Plots:** Examined relationships between key features and salary.

---

## Conclusions
- The optimized XGBoost model is the most suitable for predicting NBA player salaries.
- Feature importance analysis provides valuable insights for decision-makers in player evaluations.
- Regular updates with new player data can maintain prediction accuracy and relevance.

---

## How to Run the Project
1. **Setup Environment:**
   - Install required libraries using `pip install -r requirements.txt`.
2. **Run the Notebook:**
   - Open `Data science final project.ipynb` in Jupyter Notebook.
   - Execute cells step-by-step to preprocess data, train models, and analyze results.
3. **Explore Results:**
   - View visualizations and evaluate model predictions in the notebook.

---

## Contributors
- **Omer Vazana** (ID: 318870102)
- **Bar Sonego** (ID: 318678943)
- **Ron Benjamin** (ID: 323906024)

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
