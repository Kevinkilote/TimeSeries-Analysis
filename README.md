# Climate Data Analysis and Forecasting

## Project Objectives
- **Climate Trends:** Analyze how climate variables change over time.
- **Anomalies:** Identify any outliers or anomalies in the data for further analysis.
- **Correlations:** Calculate correlations to understand relationships between climate variables.
- **Forecasting:** Develop a model to predict future values using historical data.

## Research Questions
1. How has the temperature changed over time (e.g., exponential growth, linear)?
2. Are there any seasonal patterns in temperature?
3. What are the trends in climate variables?
4. How does temperature correlate with other climate variables?
5. Can we accurately forecast temperature using predictive models?
6. How do different forecasting models compare in predicting temperature trends in Indonesia?

## Discussion of Methods

1. **Data Analysis and Visualization:** Use graphs and data analysis to explore the data components.
2. **Modeling Approaches:** Implement and evaluate multiple forecasting models.

### Models Evaluated
1. **Baseline Models:**
   - **Naive, Seasonal Naive, Mean, Drift:** Basic models providing benchmark comparisons.
      - *Naive:* RMSE of 0.819, MAPE of 2.48%
      - *Seasonal Naive:* Higher errors, indicating weak seasonal patterns.
      - *Mean:* Similar performance to Naive.

2. **Statistical Models:**
   - **AR, AR+MA, ARIMA, SARIMA:** Models leveraging time-series dependencies.
      - *ARIMA/SARIMA:* Robust but higher RMSE and MAE, indicating limitations with this dataset.
      - *Holt-Winters:* Potentially effective but limited by lack of stable seasonal data.

3. **Machine Learning Models:**
   - **MLP, CNN, LSTM:**
      - *MLP:* RMSE of 0.793, MAE of 0.615; MAPE (3.60%) suggests occasional large errors.
      - *CNN:* Lowest RMSE (0.551), strong pattern recognition.
      - *LSTM:* RMSE of 0.620, MAE of 0.490; captures temporal dependencies well.

4. **Advanced Models:**
   - **Prophet:** RMSE of 0.696, MAE of 0.537, showing moderate predictive accuracy.

## Best Results
- **Grid Search CNN (Model 14):** Lowest RMSE (0.530), indicating minimal forecasting error.
- **LSTM Model (Model 11):** Lowest MAE (0.490), demonstrating minimal average error.
- **Grid Search CNN (Model 14):** Lowest MAPE (0.016%), indicating minimal percentage error relative to actual values.

## Evaluation Summary
- Baseline models like Naive, Mean, Drift, and ARIMA performed reasonably but fell short of more complex models in accuracy.
- Advanced models (CNN, LSTM, Prophet) demonstrated superior performance, especially the Grid Search CNN with a MAPE of 0.019%.
- Complex models such as ARIMA and SARIMA showed limitations in capturing complex patterns but closely matched baseline model performance.

## Future Works
1. **Enhancing Model Robustness:** Explore alternative architectures and regularization to improve CNN and LSTM robustness.
2. **Benchmarking:** Compare against state-of-the-art models, including Transformers.
3. **Climate Change Impact Analysis:** Extend to investigate climate change impacts on temperature trends in Indonesia using long-term data.

---

This project presents a comprehensive analysis and forecasting approach for climate data, focusing on Indonesia. Each model’s performance provides insights into forecasting accuracy and the utility of various model complexities.
