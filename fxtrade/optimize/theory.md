## Value iteration
Discount factor (long-terms success 0.9, immediate success 0)

V = R + yV'

greedy policy

## Policy iteration

V = R + y*Sum(weighted Vì)
Converges faster

## TD learning

V = V + alpha*(R + yV' - V)

## Q learning

state-action pair

## RL in trading strategies

Reward function:
- Absolute reward maximization (less used)
- Optimal sharpe ratio (most efficient reward goal for DRL reward algorithms)

Efficiency and performance of trading strategy:
- good match for rapidly-changing environments
- financial markets are dynamic environments
- short-lived and hard-to-identify, unique, patterns
- historical data quickly become irrelevant for predecting current movements

- pattern based strategies are now useless

Successfull = Flexible, able to adpat to current situation

DRL learn on the go and by doing, better at taking real time decisions. Markets are a high density environment for modeling because of all the variables, affecting the outcome of a trading decision. This makes it difficult for the developer to anticipate future market environments which means that they must update their trading algorithms on a more or less continuous basis. An RL algo avoids this by being able to update itself in real time.

Financial market = High density environment

Existing ML algos have 2 main components:
- Strategy: usually designed by the trader
- Implementation: handled by the machine

Get unbiased data from financial market

Human effort:
- requires millions of iteration to be profitable
- reward design is tricky


## Deal with time-series data

To create a supervised dataset from time series, go over the data with a sliding window to get data within the windows as X and future data within a certain horizon as labels.