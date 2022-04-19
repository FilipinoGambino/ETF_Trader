# ETF_Trader

This trading bot was designed to trade the S&P 500 ETF, ticker 'SPY'. I used about 3 years of 1-minute candle data to train the models for on Kaggle (v2 of this bot [with stable baselines3] is going to use 17 years of data trained on GCP hardware). The missing values in my dataset were quite easy to fill in as the only missing data I could find were candels with zero volume. If there was no volume, there shouldn't be a change in the value of the asset. As such, simply forward filling each column of OHCLV data would fill out the dataset.

This implementation uses a Double-DQN which I selected because I hadn't heard of it and thought it would be fun and interesting to try. Stable baselines3 doesn't have a Double-DQN (yet), but they have a few other policy networks I would like to try, like PPO.

# TODO
- [x] Build custom feature extractor
- [ ] Build LR Scheduler
- [ ] Hyperparameter tuning
- [ ] Try out differnet net_archs
