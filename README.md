# stock-prediiction
using ML algorithms to predict stock prices
8.1 Fbprophet
 Prophet makes it much more straightforward to create a reasonable, accurate forecast. The forecast package includes many different forecasting techniques (ARIMA, exponential smoothing, etc.), each with their own strengths, weaknesses, and tuning parameters. We have found that choosing the wrong model or parameters can often yield poor results, and it is unlikely that even experienced analysts can choose the correct model and parameters efficiently given this array of choices. Prophet forecasts are customizable in ways that are intuitive to non-experts. There are smoothing parameters for seasonality that allow you to adjust how closely to fit historical cycles, as well as smoothing parameters for trends that allow you to adjust how aggressively to follow historical trend changes. For growth curves, you can manually specify “capacities” or the upper limit of the growth curve, allowing you to inject your own prior information about how your forecast will grow (or decline). Finally, you can specify irregular holidays to model like the dates of the Super Bowl, Thanksgiving and Black Friday. At its core, the Prophet procedure is an additive regression model with four main components: 
• A piecewise linear or logistic growth curve trend. Prophet automatically detects changes in trends by selecting change points from the data. 
• A yearly seasonal component modelled using Fourier series.                                                      
 • A weekly seasonal component using dummy variables. 
• A user-provided list of important holidays. 



8.2 K nearest neighbour
 K-nearest neighbour technique is a machine learning algorithm that is considered as simple to implement (Aha et al. 1991). The stock prediction problem can be mapped into a similarity based classification. The historical stock data and the test data is mapped into a set of vectors. Each vector represents N dimension for each stock features. Then, a similarity metric such as Euclidean distance is computed to take a decision. In this section, a description of kNN is provided. kNN is considered a lazy learning that does not build a model or function previously, but yields the closest k records of the training data set that have the highest similarity to the test (i.e. query record). Then, a majority vote is performed among the selected k records to determine the class label and then assigned it to the query record. The prediction of stock market closing price is computed using kNN as follows: 
a) Determine the number of nearest neighbours, k.
b) Compute the distance between the training samples and the query record.
c) Sort all training records according to the distance values. 
d) Use a majority vote for the class labels of k nearest neighbors, and assign it as a prediction value of the query record.

8.3 Linear regression
Linear regression is widely used throughout Finance in a plethora of applications. In previous tutorials, we calculated a companies’ beta compared to a relative index using the ordinary least squares (OLS) method. Now, we will use linear regression in order to estimate stock prices. Linear regression is a method used to model a relationship between a dependent variable (y), and an independent variable (x). With simple linear regression, there will only be one independent variable x. There can be many independent variables which would fall under the category of multiple linear regression. In this circumstance, we only have one independent variable which is the date. The date will be represented by an integer starting at 1 for the first date going up to the length of the vector of dates which can vary depending on the time series data. Our dependent variable, of course, will be the price of a stock. In order to understand linear regression, you must understand a fairly elementary equation you probably learned early on in school.
y = a + bx
where
Y = the predicted value or dependent variable
b = the slope of the line
x = the coefficient or independent variable
a = the y-intercept
8.4 Long short term memory   
LSTM is the advanced version of Recurrent-Neural-Networks (RNN) where the information belonging to previous state persists. These are different from RNNs as they involve long term dependencies and RNNs works on finding the relationship between the recent and the current information. This indicates that the interval of information is relatively smaller than that to LSTM. The main purpose behind using this model in stock market prediction is that the predictions depends on large amounts of data and are generally ependent on the long term history of the market. So LSTM regulates error by giving an aid to the RNNs through retaining information for older stages making the prediction more accurate. Thus proving itself as much more reliable compared to other methods. Since stock market involves processing of huge data, the gradients with respect to the weight matrix may become very small and may degrade the learning rate. This corresponds to the problem of Vanishing Gradient. LSTM prevents this from happening. The LSTM consists of a remembering cell, input gate, output gate and a forget gate. The cell remembers the value for long term propagation and the gates regulate them.
