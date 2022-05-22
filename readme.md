# Stock Price Prediction
* Let's say we want to make money by buying stocks. Since we want to make money, we only want to buy stock on days when the price will go up (we're against shorting the stock). We'll create a machine learning algorithm to predict if the stock price will increase tomorrow. If the algorithm says that the price will increase, we'll buy stock. If the algorithm says that the price will go down, we won't do anything.
* We want to maximize our true positives - days when the algorithm predicts that the price will go up, and it actually goes go up. Therefore, we'll be using precision as our error metric for our algorithm, which is true positives / (false positives + true positives). This will ensure that we minimize how much money we lose with false positives (days when we buy the stock, but the price actually goes down).
* This means that we will have to accept a lot of false negatives - days when we predict that the price will go down, but it actually goes up. This is okay, since we'd rather minimize our potential losses than maximize our potential gains
# Method
* Before we get to the machine learning, we need to do a lot of work to acquire and clean up the data. Here are the steps we'll follow:
* Download historical stock prices from Yahoo finance
* Explore the data
* Setup the dataset to predict future prices using historical prices
* Test a machine learning model
* Setup a backtesting engine
* Improve the accuracy of the model
* At the end, we'll document some potential future directions we can go in to improve the technique.
# Note:
- Open - the price the stock opened at.
- High - the highest price during the day
- Low - the lowest price during the day
- Close - the closing price on the trading day
- Volume - how many shares were traded
# Improve the technique
Calculate how much money you'd make if you traded with this algorithm
# Improve the algorithm
- Run with a reduced step size! This will take longer, but increase accuracy
- Try discarding older data (only keeping data in a certain window)
- Try a different machine learning algorithm
- Tweak random forest parameters, or the prediction threshold
# Add in more predictors
- Account for activity post-close and pre-open
- Early trading
- Trading on other exchanges that open before the NYSE (to see what the global sentiment is)
- Economic indicators
- Interest rates
- Other important economic news
- Key dates
- Dividends
- External factors like elections
- Company milestones
- Earnings calls
- Analyst ratings
- Major announcements
- Prices of related stocks
- Other companies in the same sector
- Key partners, customers, etc.
