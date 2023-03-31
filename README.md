# Stock-Market-Data-Analysis

# Context<br/>
### I wanted to understand whether trading the S&P500 index based on the direction of a Stochastic Oscillator indicator consistently at a set opening and closing time could yield a profit. In other words, if the Stochastic Oscillator was facing upward at the specified opening time, I would buy and if it was facing down I would buy. I would then close the trade when the closing time arrived.<br/><br/>Considering that this strategy is purely based on objective facts and no subjective interpretation, calculating this with code is ideal. 

# Problem Statement and Objective<br/>
### Problem Statement
> I need to determine if trading the S&P500 can be profitable with the following trading strategy: opening a trade in the direction of the Stochastic Oscillator at a specified opening time and closing the trade at a set closing time, and doing this consistently over a period of time.
### Objective:
> Create a function with parameters for opening time, closing time, analysis period and analysis symbol. The function should return an output that allows me to determine whether the trading strategy in the problem statement will be profitable, on average, over the analysis period. 

# Methodology<br/>
## Dataset<br/>
### I made use of Yahoo Finance to extract the required dataset. I used this data to manually calculate the %d and %k values for the Stochastic Oscillator.<br/>I then performed a series of pre-processing and formatting steps that would allow me to go through the following steps:<br/>
#### Was the trade successful: If the Stocahstic Osillator was facing upward, did the price also move upward?
#### How big was the price movement if the trade was successful vs unsuccessful: If the losses are larger than the wins, you will lose money
#### What is the probability of having a winning trade or a losing trade: Having a few large winning trades and many small losing trades may be a viable strategy

# Output<br/>
### The output of the calculations is a table that answers the above questions. It specifies the following for wins and losses:
1. How large is the average price movement
2. What is the probability
### This is used to calculate a third column called the expected value which tells us what the expected price move is for a win or loss. We use this to determine if a strategy will make a profit over the long run.<br/>If the expected value of a win is larger than the expected value of a loss, it suggests the strategy will be profitable over the long run.<br/><br/>But how profitable will it be?<br/>The Expected Value Win/Loss Ratio tell us the size of the winning trades relative to the losing trades. The larger the value, the larger the profit. A negative value suggests a loss will be made. A value of zero suggests that you will break even and make no profit.
