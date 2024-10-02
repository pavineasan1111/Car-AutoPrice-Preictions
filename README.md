Car Auto price prediction:

## Problem Statement

This project aims to predict car prices based on several independent variables. The main objectives are:

1. Prepare a complete data analysis report on the given data.
2. Create a predictive model to understand how car prices vary with independent variables, which will help management make informed business decisions.

The dataset contains various attributes like the car's make, engine size, fuel type, and more, which will be used to model the car prices. By analyzing the relationship between these variables and the price, management can adjust car design and strategy to meet certain price levels. Additionally, this model will provide insights into pricing dynamics for new markets.

## Dataset Information

The dataset consists of the following attributes:

1. **Symboling**: -3 to 3 (Insurance risk rating).
2. **Normalized-losses**: 65 to 256 (Continuous).
3. **Make**: The brand of the car (e.g., Alfa-Romero, Audi, BMW, etc.).
4. **Fuel-type**: Diesel, gas.
5. **Aspiration**: Standard, turbo.
6. **Number of doors**: Two, four.
7. **Body-style**: Hardtop, wagon, sedan, hatchback, convertible.
8. **Drive-wheels**: 4WD, FWD, RWD.
9. **Engine-location**: Front, rear.
10. **Wheel-base**: 86.6 to 120.9 inches.
11. **Length**: 141.1 to 208.1 inches.
12. **Width**: 60.3 to 72.3 inches.
13. **Height**: 47.8 to 59.8 inches.
14. **Curb-weight**: 1488 to 4066 lbs.
15. **Engine-type**: DOHC, OHCV, OHCF, etc.
16. **Number of cylinders**: 2 to 12.
17. **Engine size**: 61 to 326 cubic inches.
18. **Fuel-system**: 1bbl, 2bbl, 4bbl, idi, mfi, mpfi, etc.
19. **Bore**: 2.54 to 3.94 inches.
20. **Stroke**: 2.07 to 4.17 inches.
21. **Compression-ratio**: 7 to 23.
22. **Horsepower**: 48 to 288.
23. **Peak RPM**: 4150 to 6600.
24. **City MPG**: 13 to 49.
25. **Highway MPG**: 16 to 54.
26. **Price**: 5118 to 45,400 USD (Target variable).

## Model Comparison Report

Several models were evaluated to predict car prices based on the available features. These include:
- **Linear Regression**
- **Decision Trees**
- **Random Forest**
- **XGBoost**

Each model was evaluated using metrics such as **Mean Absolute Error (MAE)**, **Root Mean Squared Error (RMSE)**, and **R²** to measure accuracy and generalizability. After running multiple iterations, the XGBoost model performed the best, with the lowest MAE and RMSE.

### Best Model
**XGBoost** was selected for production due to its superior performance and ability to handle both linear and non-linear relationships in the data.



## Challenges Faced

During the project, several challenges were encountered:

1. **Missing Data**: The dataset had missing values in columns such as `normalized-losses`. We handled this by using mean imputation to replace the missing values.
2. **Categorical Variables**: The `make`, `fuel-type`, `body-style`, and other categorical variables needed to be encoded before model training. We used one-hot encoding to transform these into numerical values.
3. **Outliers**: Some variables, like `horsepower` and `price`, contained outliers. We addressed this by normalizing the features and applying logarithmic transformation for skewed data.
4. **Model Tuning**: Hyperparameter tuning was necessary for models like Random Forest and XGBoost to avoid overfitting and improve performance.

These steps ensured that the dataset was ready for model training, and the final model was robust and accurate.

![Correlation Heat Map](https://github.com/pavineasan1111/Car-AutoPrice-Preictions/blob/main/Correlation%20Heat%20map.JPG?raw=true)

## Conclusion

The XGBoost model accurately predicts car prices based on a variety of features such as engine size, make, and horsepower. This project provides valuable insights into how different features affect the price, allowing management to make informed decisions regarding car design and pricing strategies.

### Future Work
- Incorporate additional features like brand reputation or resale value to improve prediction accuracy.
- Use deep learning models for further improvement.
- Expand the dataset to cover more regions and car models.
