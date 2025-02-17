# Rohlik Sales Forecasting Challenge - A Kaggle Competition
The "Rohlik Sales Forecasting Challenge" on Kaggle tasks participants with predicting sales of online groceries. Using historical sales data, competitors create models to forecast demand, optimizing inventory, pricing, and promotions. It’s a chance to showcase skills in time-series forecasting and predictive analytics.

Rohlik Group, a leading European e-grocery innovator, is revolutionising the food retail industry. The company operates across 11 warehouses in Czech Republic, Germany, Austria, Hungary, and Romania.

The company is now transitioning from the Rohlik Orders Forecasting Challenge to the Rohlik Sales Forecasting Challenge. This challenge focuses on predicting the sales of each selected warehouse inventory for next 14 days using historical sales data.

I participated in this competition along with my two friends Vekatesh and Vishnu. We have been looking forward to working together on something for a long time and found this competition in Kaggle.
We did not finish with a great rank, but we had a lot of fun and learnt a lot while working on this challenge.

**Final Result:** 271 out of 777. Public score: **20.86121**, Private score: **20.24298**.

You can find the final submission in the link given here: https://www.kaggle.com/code/venkytheknown/team-403-rohlik-sales-forecasting

You can find the competition details in the link give here: https://www.kaggle.com/competitions/rohlik-sales-forecasting-challenge-v2/overview

**Final Submission**
LightGBM-based model was utilized with feature engineering that incorporates temporal patterns, seasonal trends, and specific store behaviors. Key features include date-related attributes, warehouse-specific conditions, and custom lag features for sales data. Additionally, a critical improvement is made by integrating the year-over-year sales growth, considering the natural increase in sales over time, which helps the model account for long-term trends.

We have used other gradient-boosting methods like XGBoost and CatBoost method but found that LighGBM results were more accurate.

One significant enhancement that we worked on was adjusting the model predictions based on the observed sales growth over the years. By multiplying the model’s output by a calculated sales change multiplier (1.05), we accounted for the general upward sales trend. This adjustment led to a more accurate prediction, especially when tested on future data.

**Missed Oppurtunities**

We missed/failed to use some of the lag features and conversions that we did in our other models like using moving averages to fill in null values in sales and orders columns and converting sales to log function in order to include all outliers rather than removing them. We believe that using them could have improved our scores.
Nevertheless, what is done is done, and we are happy with what we achieved in this challenge.

**Approaches that did not work for us**

1. We observed that increasing features in the model did not improve our prediction results.
2. Using MAE to train our model gave terrible results for some reason. (But some teams reported gains.)
3. Adding the cosine and the sine functions to time-based features led to worse results. (But some teams reported gains.)

**Key Takeaways**

1. Decision tree models are generally not very good at extrapolating.
2. Using the multiplier at the end for our results gave us great improvements to our final score.

We have attached our final file to this GitHub repository. We have also attached other models that we created and experimented with for your reference.
We hope our work proves helpful in generating new ideas and methods of approach and help in any way possible.


