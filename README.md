Introduction
 
	Predicting stock performance is a very large and profitable area of study 
	Many companies have developed stock predictors based on neural networks 
	This technique has proven successful in aiding the decisions of investors
	Can give an edge to beginning investors who don’t have a lifetime of experience
	Stock markets are highly volatile and generate huge amounts of data daily
	However, the stock market is influenced by many factors such as political and economic conditions

Objectives
 
	The objective of the project work is to study and use the efficient deep  learning algorithms to predict the stock prices
	Technical objectives will be implementing different python libraries
	The system must be able to access a list of historical prices
	It must calculate the estimated price of stock based on the historical data
	It must also provide the instantaneous visualization of the market 
	Accuracy of predicted stock price is around 90%

Method

Steps to be followed:
1.	Input data set
2.	Filter the input data set
3.	Scale down the input data set to range(0,1)
4.	Create train data
5.	Create and fit into LSTM network
6.	Predict required data set
7.	Plot the graph
1.Input data set:
•	It includes fields such as date,high,low,close,volume
•	Fetch data from quandl using datareader.web
 2.Filter the data set
•	Inside data frame remove high,low and volume
•	Make index as date
 3.Scale down the data set 
•	MinMaxScaler from sklearn is used to scale the filtered data to feature_range=(0,1)
4.Create train data :
•	We have 1090 rows in total , I am taking  1-871 rows to train our model, and other remaining data for validity
•	x_train includes the set of 60 scaled data from 0-60 , 1-61, 2-63 ….. 6-871
•	y_train includes the dates parallel to x_train
•	Both are  taken to  an numpy array
5.Create and fit into the LSTM network:
•	Initialize model as sequential
•	Add LSTM input data as x_train data
•	Set compilation
•	Fit the model
6.Predict data sets:
•	Including the valid dataset also
•	 x_test data includes  as 811-871, 812-872, 813-873, …….. 870-1090 
•	Using the model we made  pass x_test 
•	Get predicted data and pass to dataframe as new column as “Predictions”
7.Plotting graph:
•	Using matplotlib as a plotting library
•	X axis as dates
•	Y axis as stock Price
•	The past data and predicted data. In the same graph with different colors.
 
 

Long Short Term Memory networks – usually just called “LSTMs” – are a special kind of RNN, capable of learning long-term dependencies.
All recurrent neural networks have the form of a chain of repeating modules of neural network. 
LSTMs also have this chain like structure, but the repeating module has a different structure. Instead of having a single neural network layer, there are four, interacting in a very special way.

Mapping to subjects
•	Python :  using different python libraries for implementation
•	CNC  : encryption of username and password . Here we are using SHA-256 encryption
•	FS  : user data is stored in files and search operation on files for                     .                 authentication.
•	ST : testing with different inputs for authentication of user and also for                .                 calculation of accuracy.
•	OR: Optmising final result by applying different algorithm like KNN,Linear Regression etc. and selecting optimal result.
•	OS: Optimising the RAM usage and CPU resources.
Results
 
It contain three data sets:
1.Training set
2.Valid set
3.Test set
Training set contains 871 records containing the closing and opening price of a company. Valid set and test set contains 220 records containing the closing price. The Blue line in graph indicates the training set.The green line in graph indicates the test set. The orange line in graph indicates the valid set 
 
 
Conclusions
	Historical data is from 2015-01-01 to 2018-06-18
	Taking present date as  2018-06-18
	Estimated data of prices from 2018-06-19 to 2019-03-05 from historical data
	Taking correlation between Real data and estimated data gives the accuracy
	Accuracy of Predicted data is around 90%
	Stock price is affected by the news about the company and other factors like demonetization or merger/demerger of the companies.
	Different machine learning algorithms such as linear regression , k-nearest neighbours produces results with less than 50% accuracy
	Hence, We are using LSTM to obtain the Maximum accuracy.

References
	Python and Tkinter Programming, Book by John E.Grayson
	Fundamentals of Deep Learning, Book by Nikhil Buduma
	Stack overflow, geeks for geeks
	Software Testing, Book by paul C.jorgensen  
