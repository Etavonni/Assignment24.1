### Project Title
Predicting Stock Price Movement with Gradient boosting, SVMs and LSTMs

**Author**
Dipankar Roy

#### Executive summary
We will try to create a predictive model that can forecast the directional movement of the S&P 500 with a classification accuracy moderately better than random chance (50%). While creating a perfectly accurate prediction is highly unlikely due to the complex and semi-random nature of financial markets, the goal is to develop a model that demonstrates statistically significant predictive power, providing a modest edge in forecasting market trends.

#### Rationale
Why should anyone care about this question?

Financial Application: A model with predictive accuracy can provide a valuable edge for developing automated trading strategies, enhancing portfolio management, and improving financial risk assessment for investors and institutions.

Academic Insight: The project serves as a practical test of the Efficient Market Hypothesis, which posits that asset prices fully reflect all available information, making it impossible to consistently "beat the market." By attempting to find predictable patterns, this research contributes to the ongoing debate about market efficiency.

#### Research Question
What are you trying to answer?

Can a machine learning model, specifically a Long Short-Term Memory (LSTM) network, accurately predict the next day's directional movement (up or down) of the S&P 500 index using historical price data, technical indicators, and key macroeconomic variables?

#### Data Sources
What data will you use to answer you question?

Historical S&P 500 Data: Daily open, high, low, close, and volume data will be obtained using the yfinance library in Python, which pulls data from Yahoo Finance.

Macroeconomic Data: Key economic indicators such as the Federal Funds Rate, Consumer Price Index (CPI), and GDP growth rates will be sourced from the Federal Reserve Economic Data (FRED) database.

#### Methodology
What methods are you using to answer the question?

1. Data Preprocessing: The initial phase will involve cleaning the data, handling any missing values, and aligning the different time-series datasets.

2. Feature Engineering: New features will be created from the raw data to improve model performance. This will include calculating various technical indicators such as the Simple Moving Average (SMA), Relative Strength Index (RSI), and Moving Average Convergence Divergence (MACD).

3. Modeling: We will use the following models:

    3A. A simple model, like Logistic Regression, will be used as a baseline for performance comparison.

    3B. Gradient Boosting Machines : Gradient Boosting is an ensemble technique that builds a strong predictive model by combining many "weak" decision tree models sequentially. They excel when the problem is framed with well-engineered features (like moving averages, RSI, and macroeconomic data).

    3C. Support Vector Machine : SVM is a powerful classification algorithm that works by finding the optimal hyperplane that best separates the data points of different classes. By using the "kernel trick," SVMs can efficiently handle high-dimensional and non-linear problems.

    3D. Decision Trees : Decision Trees are a non-parametric supervised learning method used for classification and regression. The goal is to create a model that predicts the value of a target variable by learning simple decision rules inferred from the data features. A tree can be seen as a piecewise constant approximation.

    3E. A Long Short-Term Memory (LSTM) neural network will be the primary model used for prediction. LSTMs are a type of recurrent neural network (RNN) well-suited for time-series forecasting because they can effectively learn long-term dependencies in sequential data.

4. Model Evaluation: The model's performance will be evaluated based on its ability to classify the next day's movement. Key metrics will include Accuracy, Precision, Recall, and the F1-Score. A confusion matrix will also be generated to visualize the model's performance on a held-out test dataset.

#### Results
What did your research find?

After creating and evaluating all the models, we find that SVC performs the best with an accuracy score of 0.5513. Decision Trees are the second best model with an accuracy score of 0.5256 and a precision better than SVC. Both these models beat the baseline and are better than random chance (50%). Hence this satisfies the project end goal.

|Model|Accuracy|Precision|Recall|F1-Score|
|-----|--------|---------|------|--------|
|LogisticRegression|0.47|0.50|0.47|0.45|
|GradientBoosting|0.46|0.49|0.46|0.44|
|SVC|0.55|0.52|0.55|0.50|
|DecisionTree|0.53|0.55|0.53|0.52|
|LSTM|0.46|0.53|0.46|0.40|

#### Next steps
What suggestions do you have for next steps?

Next steps could be to refine the data and the models further and experiment with various parameters. We can investigate with various types of LSTM models to find a more suitable one with a better accuracy.

#### Outline of project

https://github.com/Etavonni/Assignment24.1

##### Contact and Further Information

Author can be contacted at roydipankar@gmail.com
