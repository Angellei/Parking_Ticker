# San Francisco Parking Ticket Model
<p align="center">
    <img src="https://www.resetsanfrancisco.org/wp-content/uploads/sites/47/2014/07/parking_ticket.png" alt="alternate text" width="800">
 </p>
 
## Motivation
- The dataset used in this project included number of street parking ticket in San Francisco with spcific Date, Time, Year, and Street Names in San Francisco. The dataset obstained by a public request from SFMTA. 
- Street parking citation in San Francisco can makes a huge portion of government income. By knowing the estimation of parking ticket received next week, months, or year aids government on planning its budget accordingly. 
- I utilized this dataset to do data mining, to find the variation trend of highest number of parking ticket citation in San Francisco, and the factors associated with it. 

## Target
- Find number of ticket with significant variation based on daily, weekly, monthly, and yearly ticket
- Train the model to predict number of parking tickets in next week, months or years based on last one year and half of parking tickets since 2016 
- Explore the variation effect on number of parking ticket

# Data

## Learning methods for classification
      1. Linear Regression 
      2. LSTM(time series) 
      
- **What's LSTM?**<br/>
Long short-term memory (LSTM) is a special kind of recurrent neural network (RNN) architecture (Hochreiter *et al*) used in the field of deep learning, which is able to remembering information for long periods of time. In Natural language processing (NLP), documents are fed into the model of LSTM one word by one word and the model will make the prediction with consideration of **word sequence**. A common LSTM unit is composed of a cell, an **input gate**, an **output gate** and a **forget gate**. The cell remembered values over arbitrary time intervals and the three gates regulated the flow of information in and out of the cell. Comparing to classical RNN, LSTM is capable of handling "long-term dependencies" **VERY WELL**.
  

<div align="center">
  An unrolled recurrent neural network
</div>

<br/>

<p align="center">
   <img src="https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/RNN-unrolled.png" alt="alternate text" width="800">
</p>

<br/>

<br/>

<div align="center">
  An illustration of the LSTM cells
</div>
<p align="center">
   <img src="https://wiki.tum.de/download/attachments/22578349/LSTMdiff.jpg?version=1&modificationDate=1486080694247&api=v2" alt="alternate text" width="800">
</p>

## Exploratory data analysis
- The highest number of parking ticket is Friday among other days, and August among other months. Also noticed the weekday parking ticket tend to be higher compare to weekend parking ticket
- Although a majority of the street cleaning tickets are given out between 8-10AM, I think that's just because there are more streets that are cleaned at time. Lets see if that's substantiated.
- treets cleaned on Saturday and Sunday are more effective.
<p align="left">
   <img src="Plot/num_comments_date.png" alt="alternate text">
</p>

<p align="right">
   <img src="Plot/num_comments_date.png" alt="alternate text">
</p>


### Found parking ticket with significant variations in weekend/weekday users
- The graph below shows a huge gap, due to weekend and weekday users, so I decided to separate the data into two distributions: weekday and weekend to see if there's a linear relationship between each features.
</p>

<p align="center">
   <img src="Plot/num_comments_date.png" alt="alternate text">
</p>

# Modeling with weekday users
- Used Linear Regression model 
got a RMSE score better than benchmark

# Modeling with weekend users

# Prediction for next day
- Used 

# Results
I began my project by scraping ticket_issue_date feature into date_time stamp and aggregate it into yearly, monthly and daily counts of number of parking ticket. Then, I moved onto feature engineering to 
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

#Initial Exploration Findings
First I did some exploratory analysis just to look for some interesting takeaways in the data, as well as ensure the data was processed properly and no major holes existed. There are quite a few graphs generated in the notebooks, so I placed them in a separate readme file in the explore data older.



- Highest number of parking ticket citation is at Geary Street in the morning rush hour from 7:00am - 9:00am, and Mission Street in the afternoon rush hour from 4:00pm - 6:00pm
<p align="left">
   <img src="Plot/num_comments_date.png" alt="alternate text">
</p>

<p align="right">
   <img src="Plot/num_comments_date.png" alt="alternate text">
</p>

- From the graph below, there's huge gap difference between twoweekday and weekend parking ticket. So I decided to separate the data into two distributions: weekday and weekend
