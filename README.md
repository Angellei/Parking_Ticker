# Parking_Ticker
                                                        Purpose
Street parking ticket citation in San Francisco can makes a huge portion of government income. By knowing the estimation of parking ticket received next week aids government on planning its budget accordingly. My model can predict the number of parking ticket for next week from target street.

Process
I began my project by scraping ticket_issue_date feature into date_time stamp and aggregate it into yearly, monthly and daily counts 
of number of parking ticket. Then, I moved onto feature engineering to 
see which time period is more reasonable to predict for next period. 

Tech_sack
Some of the tools I had used: Pandas, NumPy, Scikit-learn, Jupyter Notebook, AWS, EC2, Pickle, fbprophet, EDA, LSTM(Time Series Model), Prophet, Keras, Linear Regression, and cross_validation.

Modeling
Utilized entire data set (number of parking tickets from past two years since 2016) split into training and test set. Used training set to fit the LSTM model, and used test set to predict next week’s total number of parking ticket in San Francisco. 
Used Epoches, Batch_size, Window_size, and Verbose as hyper-parameters
Optimized minimum RMSE (Root Mean Square Error) score

Results

Achieved RMSE of 1205.98 on test set (right), vs Baseline RMSE of 43.68
From EDA, I know Mission Street and Geary Street has the highest number of parking ticket written compare to other streets in San Francisco, so I used Mission Street’s parking ticket data to predict next week’s parking ticket
Achieved RMSE in Mission Street of 41.91 vs Mission Street Baseline RMSE of 43.68. My model outperform the baseline model, which means my model is better at predicting future values compare to randomly choose a number
