# Ubiquant Market Prediction
Make predictions against future market data


### Gold-Medal Discussion [link](https://www.kaggle.com/competitions/ubiquant-market-prediction/discussion/309146)


#### Description
Regardless of your investment strategy, fluctuations are expected in the financial market. Despite this variance, professional investors try to estimate their overall returns. Risks and returns differ based on investment types and other factors, which impact stability and volatility. To attempt to predict returns, there are many computer-based algorithms and models for financial market trading. Yet, with new techniques and approaches, data science could improve quantitative researchers' ability to forecast an investment's return.



Ubiquant Investment (Beijing) Co., Ltd is a leading domestic quantitative hedge fund based in China. Established in 2012, they rely on international talents in math and computer science along with cutting-edge technology to drive quantitative financial market investment. Overall, Ubiquant is committed to creating long-term stable returns for investors.

In this competition, you’ll build a model that forecasts an investment's return rate. Train and test your algorithm on historical prices. Top entries will solve this real-world data science problem with as much accuracy as possible.

If successful, you could improve the ability of quantitative researchers to forecast returns. This will enable investors at any scale to make better decisions. You may even discover you have a knack for financial datasets, opening up a world of new opportunities in many industries.

This is a Code Competition. Refer to Code Requirements for details.


#### Evaluation
Submissions are evaluated on the mean of the Pearson correlation coefficient for each time ID.

You must submit to this competition using the provided python time-series API, which ensures that models do not peek forward in time. To use the API, follow this template in Kaggle Notebooks:

```
import ubiquant
env = ubiquant.make_env()   # initialize the environment
iter_test = env.iter_test()    # an iterator which loops over the test set and sample submission
for (test_df, sample_prediction_df) in iter_test:
    sample_prediction_df['target'] = 0  # make your predictions here
    env.predict(sample_prediction_df)   # register your predictions
```

You will get an error if you submission includes nulls or infinities and submissions that only include one prediction value will receive a score of -1.

#### Kaggle Competition [Link](https://www.kaggle.com/competitions/ubiquant-market-prediction/overview)