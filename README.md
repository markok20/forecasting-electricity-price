# electricity-price-forecast

How to make a complete forecast of the development of the stock market price of electricity?

How will the price of electricity on the power exchange develop in the coming weeks or months? Is there a clear trend or seasonality in the price? In what months will the price rise clearly above average and when will it fall?

As of January 2013, data containing approximately 3,000 rows of spot price information was available. The data lasted until March 21, 2021. The spot price is determined on the Nordic Nord Pool power exchange, where the price of electricity is formed for each hour of the day. A separate Spot price will be formed for the Finnish territory. Describe the price development since January 2013, calculated by defining an average for each month.

How can a complete forecast be made for the development of the stock market price of electricity? Traditionally, a moving average has been used as the forecast model, which is the simplest model to predict development. In the moving average method, the forecast of future time demand is the average of the demand of past times. The development of the moving average price is described.

I use an exponential smoothing (moving average weighted to the most recent time) model that is responsive to change and easily updatable. This is one of the most popular models for forecasting demand. Components that take into account trend and seasonality can be added to the model. In addition to the basic level of demand, factors affecting demand include trend, seasonal, cyclical and marketing factors as well as unpredictable fluctuations.

Let us now consider the development of trend and seasonality. The trend is initially slightly declining but rising from 2016-2019 until it starts to decline again. The seasonality shows that the price rises at the turn of the year, but turns to fall for the summer. After the summer, the price curve will rise until the turn of the year.
Based on the data, make a prediction of how the price will develop over the next 12 weeks from mid-March.

The Spot price in the Finnish area is determined on the power exchange for each hour of the following day no later than 12:30 (CET) on the day before the day. The price is formed at the intersection of the buy and sell offers entered into the power exchange.

The spot price is the so-called raw market price for electricity for each region and does not take into account the electricity seller's operating costs, such as certificates of origin, delivery fee, profile costs or, for example, the electricity seller's billing or customer service. In Nord Pool, the unit of electricity prices is the euro per megawatt hour, and the prices listed on the stock exchange do not include VAT.
