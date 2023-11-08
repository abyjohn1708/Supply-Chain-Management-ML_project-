# Supply Chain Optimization for FMCG Company

**Executive Summary:**

A Fast Moving Consumer Goods (FMCG) company ventured into the instant noodles business two years ago. However, the company has been facing challenges related to the imbalance between demand and supply in different regions, resulting in increased inventory costs and financial losses. To address this issue, the higher management has initiated a project to optimize the supply quantity in each warehouse throughout the country.

The primary goal of this project is to create a predictive model using historical data that determines the optimal product weight to be shipped from each warehouse. The project will encompass all essential steps of data science, including Exploratory Data Analysis (EDA), data processing, model development, evaluation, and visualization. In this report, we will present the methodology, insights, and next steps for improvement.

**Data Description:**

The training dataset consists of various features that provide information about different aspects of each warehouse. Below is a brief description of the variables:

- Ware_house_ID: Unique Warehouse ID where products are prepared for dispatch.
- WH_Manager_ID: Manager ID present in the warehouse.
- zone: Zone of the warehouse.
- WH_regional_zone: Regional Zone of the warehouse.
- num_refill_req_l3m: Refilling requests received by the warehouse in the last 3 months.
- transport_issue_l1y: Number of transport issues for the warehouse in the last year.
- Competitor_in_mkt: Number of competitors in the market.
- retail_shop_num: Number of retail shops selling noodles produced by the warehouse.
- wh_owner_type: Ownership status of the warehouse (company-owned or rented).
- distributor_num: Number of distributors working between the warehouse and retail shops.
- flood_impacted: Indicator for whether the warehouse is in a flood-impacted area.
- flood_proof: Indicator for whether the warehouse has flood-proof measures.
- electric_supply: Indicator for the presence of proper electric supply and power backup.
- dist_from_hub: Distance from the warehouse to the production hub.
- workers_num: Number of workers in the warehouse.
- wh_est_year: Warehouse establishment year.
- storage_issue_reported_l3m: Storage issues reported by the warehouse in the last 3 months.
- temp_reg_mach: Indicator for temperature regulating machine presence.
- approved_wh_govt_certificate: Type of government approval certificate for the warehouse.
- wh_breakdown_l3m: Number of breakdowns faced by the warehouse in the last 3 months.
- product_wg_ton: Product weight in tons.

**Methodology:**

1. **Data Preprocessing:**
   - Data cleaning: Handle missing values and outliers.
   - Feature engineering: Create relevant features and encode categorical variables.
   - Data splitting: Divide the dataset into a training set and a test set.

2. **Exploratory Data Analysis (EDA):**
   - Visualize the distribution of key variables.
   - Identify trends, correlations, and outliers.
   - Investigate the impact of different features on demand and supply mismatches.

3. **Model Building:**
   - Apply 5 to 6 machine learning algorithms, such as regression models, decision trees, and ensemble methods.
   - Train models using the training dataset to predict the optimal product weight to be shipped from each warehouse.

4. **Model Evaluation:**
   - Evaluate model performance on the test dataset using appropriate metrics.
   - Identify the most accurate and reliable model for optimization.

5. **Visualization and Reporting:**
   - Present insights and trends in the data.
   - Create visualizations to support decision-making.
   - Generate recommendations for optimizing supply quantity in each warehouse.

**Model Performance:**

**Regression Models:**

Six regression models were evaluated in this analysis. The models, along with their corresponding performance metrics, are summarized below:

**Linear Regression:**

MSE: 136,696,713.83
R-squared (R²): -0.0027
Description: Linear Regression is a simple model that provides limited predictive power and does not fit the data well, as evidenced by the high MSE and a negative R² value.

**Random Forest (Regression):**

MSE: 21,631,687.77
R-squared (R²): 0.8413
Description: The Random Forest model exhibits relatively high predictive power, with a low MSE and a relatively high R², suggesting it captures a substantial portion of the variance in the data.

**Decision Tree (Regression):**

MSE: 0.0
R-squared (R²): 1.0
Description: The Decision Tree model demonstrates the best performance in this evaluation, with an MSE of 0.0 and a perfect R² of 1.0. This suggests that the model perfectly fits the data, potentially indicating overfitting.

**Support Vector Machine (SVM) (Regression):**

MSE: 136,284,383.77
R-squared (R²): 0.0003
Description: The SVM model's performance is limited, as indicated by the high MSE and a very close-to-zero R² value.

**Gradient Boosting (Regression):**

MSE: 101,792,426.61
R-squared (R²): 0.2533
Description: The Gradient Boosting model shows moderate predictive power, with a relatively low MSE and a modest R² value.

**XGBoost (Regression):**

MSE: 17,731,188.82
R-squared (R²): 0.8699
Description: The XGBoost model demonstrates high predictive power, with a low MSE and a high R² value, indicating its strong ability to capture the variance in the data.

**Best Regression Model:**

Based on the evaluation of the regression models, the Decision Tree Regression model stands out as the best-performing model for this task. It achieved an MSE of 0.0, indicating a perfect fit to the data, which may warrant further investigation to ensure there is no overfitting.

**Evaluated Decision Tree Regressor to check if it's overfitting using cross-validation and a test dataset.**

It appears that the model is not overfitting. The fact that the test MSE is very low (0.00) and the test R-squared is close to 1.00 indicates that the model performs well on the test data, which is a good sign of generalization. Additionally, the average cross-validation MSE is consistent with the test MSE, suggesting that the model's performance is not significantly different on different subsets of the training data.

These results indicate that the Decision Tree Regressor is a good fit for your data and is not suffering from overfitting. It's capturing the underlying patterns in the data and generalizing well to new, unseen data.

**Future Predictions**
The DecisionTreeRegressor model was saved to a file for future use. You can load this model and make predictions on new data. The R-squared value of approximately 0.8867 for your test data indicates that the model performs well when applied to unseen data.



**Next Steps and Improvements:**

- Further data collection: Consider gathering additional data on external factors that may impact demand and supply, such as weather conditions, holidays, and local events.

- Advanced modeling techniques: Explore more advanced machine learning and forecasting techniques, including time series analysis and demand prediction.

- Continuous monitoring: Implement a system for real-time monitoring of inventory and supply chain operations to adapt to changing conditions.

- Supply chain optimization tools: Utilize supply chain optimization software to improve decision-making and reduce costs.

- Regular maintenance and updates: Maintain and update the predictive model periodically to adapt to changing market dynamics and warehouse conditions.

- Collaboration with stakeholders: Collaborate closely with warehouse managers, distributors, and retailers to gain valuable insights and make data-driven decisions.

### Conclusion

In conclusion, this project aims to optimize the supply quantity in each warehouse of the FMCG company. By leveraging historical data and applying advanced data science techniques, we can create a predictive model that will determine the optimum product weight to be shipped from each warehouse. This will help the company reduce inventory costs, minimize financial losses, and enhance overall supply chain efficiency.

In this evaluation, we assessed six regression models for the task. The Decision Tree Regression model exhibited exceptional performance, achieving an MSE of 0.0 and a perfect R² value, indicating a perfect fit to the data. However, it is essential to be cautious of potential overfitting.

It is recommended to further fine-tune and validate the Decision Tree model on unseen data and consider ensemble techniques or other models to ensure robustness and generalizability.

The choice of the final model should take into account not only performance but also practical considerations, including model interpretability and computational resources. Further investigations and model improvements should be undertaken to deploy the model effectively for the given task.

This evaluation provides a foundation for model selection and further refinement to enhance the accuracy and reliability of predictions in Supply-Chain-Management-ML_project.

The project has uncovered valuable insights from the data, and we recommend implementing the next steps and improvements outlined in this report to achieve even greater success in supply chain optimization. By staying proactive and data-driven, the company can better address demand and supply imbalances and secure its position in the competitive FMCG market. The XGBoost model is the most promising for this task and should be further validated and fine-tuned
