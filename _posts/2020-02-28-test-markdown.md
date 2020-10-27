---
layout: post
title: The Future of the NBA Three-Point Shot
subtitle: Each post also has a subtitle
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

This project was conceived during a Data Science Club meeting at UC Santa Barbara by five students who shared two common interests: Data and the NBA. Given the recent rise in three point attempts in the NBA, we were all interested in forecasting how long this trend would continue. To examine this phenomenon we approached the problem in three different ways. First, we looked at the expected value of both threes and twos over time using data from Basketball Reference. What we saw was that while historically three point shots had been a more valuable shot, the expected value of the 2 point shot had been rising to the point where it may no longer be advantageous to continue shooting more three point shots. This would suggest that the rise in three point attempts could soon tail off. The relative strength of the three point shot to the two point shot over time is illustrated in the graph below:

![Ratio](https://user-images.githubusercontent.com/47067688/76171201-da389380-6145-11ea-84af-16ce44a4bf36.png){: .mx-auto.d-block :}

To simulate how offenses and defenses adjust to changes in the expected value of shots, we used a stochastic model to simulate the percentage of three point shots the offense would take. For the inputs we used data from NBA.com on shooting percentages with respect to closest defender distance. As the expected values change, the model adjusts the proclivity of the offense to take three point shots and the level of effort the defense focuses on defending the three point shot. The stochastic model indicates that we might see a natural equilibrium between the percentage of three point shots and the percentage of two point shots as seen below:

![Model](https://user-images.githubusercontent.com/46733087/76170755-1ff35d00-6142-11ea-8c5c-fed41c0ec076.png){: .mx-auto.d-block :}

Finally, we used time series forecasting to predict where the percentage of three point shots taken could end up. We created two datasets, a training set with the observations from 1979 - 2016 and a test set of all observations (1979 - 2019). Our goal was to create an ARIMA model of the training set, forecast until 2019, and compare it to the test set. If our model was accurate, then we would forecast the next few years. After plotting our forecasts against the test set observations, we found that they matched fairly well. We then used that model to forecast the percentage of three point shots in future years. The time series forecast below shows a slight continuation of the increase of three point shots followed by a convergence and flattening out of three point attempts.

![Forecast](https://user-images.githubusercontent.com/51941454/76173043-e843df80-6158-11ea-9ce7-904b426d1577.png){: .mx-auto.d-block :}

In conclusion, all three methods suggest the same outcome: While we may continue to see a rise in the number of three point attempts in the short term, we are not far off from seeing a plateau in three point attempts and the arrival at a sort of equilibrium between the percentage of three point shots and the percentage of two point shots taken by NBA teams.

Thank you for reading. For a more detailed report, you can take a look at our
[github repository](https://github.com/sonalimayer/NBA_threepoint_2020)

