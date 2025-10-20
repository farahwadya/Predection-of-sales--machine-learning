# Predection-of-sales--machine-learning
machine learning project that used to predict the sales based on many features `Item_Fat_Content, Outlet_Size, Outlet_Location_Type, Outlet_Type
## Fetaure exploration
1. **Average sales by oulet location and size:** <br>
<img width="704" height="547" alt="download" src="https://github.com/user-attachments/assets/e64ac2b4-50a8-4da1-a02a-736871b511a6" /> <br>
- medium oultet size in tier 3 shows the best average sales, whilesmall size shows the worst sales
- Tier 3 show a good average of sales while Tier 1 show the worst sales among the 3 types of tier
2. **Item Visibility vs Outlet Sales:** <br>
<img width="589" height="455" alt="Item Visibility vs Outlet Sales" src="https://github.com/user-attachments/assets/5fcf4e58-e1f6-406b-9967-f747297d213d" /> <br>
- Supermarket type1 constitiue most of sales while Supermarket type2 have the highest sales
- Item_Visibility doesn't affect the sales, as the grocary supermarket type have the highest item_visibilty number, but it still shows the worst average sales.
## Summery of models:
 Model Evaluation

- Three regression models were trained and evaluated: Random Forest Regressor, K-Nearest Neighbors (KNN) Regressor, and Linear Regression.
Model performance was assessed using standard regression metrics: Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R² (coefficient of determination) - on both training and testing datasets.

| Model                 | Train R² | Test R²   | Test MAE  | Test RMSE   |
| --------------------- | -------- | --------- | --------- | ----------- |
| **Random Forest**     | 0.681    | **0.610** | **718.9** | **1,029.8** |
| **KNN Regressor**     | 0.595    | 0.595     | 747.3     | 1,049.4     |
| **Linear Regression** | 0.559    | 0.579     | 792.0     | 1,069.4     |


The Random Forest Regressor achieved the highest R² and the lowest error values (MAE and RMSE) on both training and testing data. it can interpret 61% of the results.
This indicates that the Random Forest model provides the best generalization performance, effectively capturing the underlying data patterns without significant overfitting.

## . Linear Regression Coefficients

Plot: <img width="640" height="470" alt="لينير ريغريشن" src="https://github.com/user-attachments/assets/bf98d389-f82e-4d8c-9bdd-28456937b3d3" />


Interpretation:
The top three most impactful features for predicting Item_Outlet_Sales are:

Item_MRP (Coefficient ≈ 978): For every $1 increase in the maximum retail price, the predicted sales increase by approximately $978, assuming other variables remain constant.

Outlet_Type_Grocery Store (Coefficient ≈ -1729): When the outlet type is a Grocery Store, the predicted sales decrease by about $1,729 compared to the baseline outlet type.

Outlet_Type_Supermarket Type3 (Coefficient ≈ 1610): When the outlet type is Supermarket Type3, the predicted sales increase by around $1,610 compared to the baseline outlet type.

Note: Positive coefficients indicate that an increase in the feature increases sales, while negative coefficients indicate a decrease in sales.

2. Tree-Based Model Feature Importances

Plot:
<img width="976" height="547" alt="راندوم فوريست" src="https://github.com/user-attachments/assets/67a5d1b0-3057-4e9d-8295-33f2b8cd0088" />

Interpretation:
The Random Forest model identified Item_MRP, Outlet_Type_Grocery Store, and Item_Visibility as the top three most important features.

Item_MRP is the most influential, contributing nearly 47.5% to the model's predictive power.

Outlet_Type_Grocery Store contributes about 19.3%.

Item_Visibility contributes around 13.2%.

Note: Feature importances measure the relative contribution of each feature to the model's predictions. They do not indicate the direction (increase or decrease) of the effect. Partial Dependence Plots (PDPs) or sensitivity analysis can be used to assess direction.

 Selected Model: **Random Forest Regressor**
The Random Forest model was chosen 
as the final regression model for this project due to its superior predictive accuracy and stable performance

## Recommendation for stackholders
Based on the analysis:

Focus marketing and sales strategies on high MRP products, as they have the greatest impact on total sales.

Evaluate and optimize the performance of Grocery Stores, which tend to have lower predicted sales compared to other outlet types.

Consider product placement and visibility improvements, as Item_Visibility also significantly influences sales.

## Recommendation for future working
Further investigation with tree-based models can help uncover non-linear relationships and interactions between features to inform strategic decisions.
- Even after tuning, the Random Forest model performs better than the other models, but it is only able to explain the patterns in about 61% of the data.
- For future improvements, we recommend trying more advanced models, collecting additional data, or further fine-tuning the parameters to achieve more consistent and accurate predictions.

