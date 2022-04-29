# Creating a Diversified Stock Portfolio Using Clustering Analysis



### About
The aim of the project is to create a diversified portfolio of stocks using clustering analysis and back test its performance against the historical data of a stock index. For this we look at the S&P500 index, that is deemed to be the most accurate quantifier of the US economy. S&P500 is the comparable standard for many funds in the marketplace.

The attempt is to use K-Means clustering based on Euclidian distances to understand the effect of different parameters that affect the stock performance. The comprehension of stock performance will be aided by dividing stocks into clusters that have stocks with similar performance. These clusters provide valuable information to create stock portfolios. 

### Link to the dataset 
https://www.kaggle.com/datasets/andrewmvd/sp-500-stocks?select=sp500_companies.csv

### Exploring the dataset

<p float="left" align="center">
<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/treemap.png" alt="drawing"     style="width:400px;"/>

<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/US%20Map.png" alt="drawing" style="width:400px;"/>

</p>

<p float="left" align="center">

<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/barplot.png" alt="drawing" style="width:400px;"/>

<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/Scatterplot1.png" alt="drawing"     style="width:400px;"/>
</p>


### Approach
The following features were calculated from the 10 year daily historical data for all the stocks in the S&P 500 index
• Correlation with SP500 index value
• Beta with SP500 index value
• Annualized Return on equity (daily returns)
• Annualized Volatility on equity (daily returns)
• Sharpe Ratio
• Daily Change in price
• Daily Variation in price

### K-Means Clustering
The following results depict the optimal value for choosing K value using a spree plot and the clusters convex formed after choosing K =4. The stock symbols are used to represent its relative position in the cluster.

<p float="left" align="center">
<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/1.png" alt="drawing"     style="width:400px;"/>

<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/2.png" alt="drawing" style="width:400px;"/>
</p>

### Clusterwise Summary Statistics and Visualization

Post K- Means clustering, Cluster wise distribution of Annualized returns, Annualized Volatility, Sharpe ratio and Beta were plotted. It can be observed that there is a significant difference in at least two or more clusters both in terms of mean value and standard deviation.

<p float="left" align="center">
<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/3.png" alt="drawing"     style="width:400px;"/>

<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/4.png" alt="drawing" style="width:400px;"/>
</p>

<p float="left" align="center">
<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/5.png" alt="drawing"     style="width:400px;"/>

<img src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/6.png" alt="drawing" style="width:400px;"/>
</p>

<p align="center">
  <img width="810" height="600" src="https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/Ann%20returns%20vs%20Ann%20vol%20vs%20Clusters.png">
</p>


### Backtesting results KMeans Portfolio vs the S&P500 index cumulative returns
For validating the process of using clustering for creating a diversified portfolio we back tested it performance on the test/validation data. The clustering was performed on the first 7 years of data and then the remaining 3 years of data were used to validate the results of our portfolio. For this, two portfolios containing 20 stocks were created
  1. Portfolio created using top five stocks (as per Sharpe ratio) from each cluster - [RED]
  2. Portfolio created using top 20 stocks out of all 500 as per Sharpe ratio from the 7-year historical
     performance - [ORANGE]


![aly_text](https://github.com/karthikramx/Diversified-Stock-Portfolio-Using-Clustering-Analysis/blob/main/Images/8.png)




