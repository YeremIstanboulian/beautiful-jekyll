---
layout: post
title: Predicting Pitchers’ ERA Using Skill-Based Measures
subtitle: Building a Linear Model to predict ERA
#gh-repo: daattali/beautiful-jekyll
#gh-badge: [star, fork, follow]
#tags: [test]
comments: true
---

Baseball is a sport that has always celebrated the use of statistics to compare players and teams. Coaches and managers have used data to determine how to improve their team for several decades and even fans of baseball often have an acute knowledge of baseball statistics. The most commonly used statistic to compare pitchers is Earned Run Average, abbreviated as ERA, which is the average number of runs a pitcher gives up per 9 innings (the length of a professional baseball game). The pitcher’s goal is to give up as few as runs as possible, so a lower ERA is considered better.  ERA is useful as a measure of a pitcher’s success, but it is not necessarily indicative of a pitcher’s skills.  There are a lot of factors that lead to runs being scored, so there is often a lot of luck associated with a pitcher’s ERA that may not necessarily be repeatable in the future. For this reason it would be helpful to have a model that predicted ERA based on a pitcher’s skills to help identify a pitcher’s expected results based on their skills. Some of the most commonly used statistics that measure pitchers’ skills are K%, BB%, GB%, and Hard Hit rate. K% is how often the pitcher strikes out the opposing hitter. BB% is how often the pitcher walks the opposing hitter. GB% is the percentage of balls hit in play by the opposing hitter that are ground balls, or balls that hit the ground in the infield. Hard Hit rate measures the percentage of balls that are hit hard by the opposing batters out of all the plays where a hitter makes contact with the ball. In short, ERA can be thought of as the results a pitcher obtains, while K%, BB%, GB%, Hard hit rate, can be thought of as ways to explain how a pitcher is obtaining his results. The data used in this project was from the 2018 season and was obtained from Fangraphs, a website that provides statistics for every player in major league baseball history.

My goal was to construct a linear model to predict era using these skill indicators and answer the following questions:
1. 	Which variables are useful in predicting ERA?
2. 	Can a significant regression model be found that predicts ERA using a combination of underlying skill indicators?
3. 	If a model is found, which specific pitchers might be over-performing or underperforming their ERA according to the model?

After performing variable testing K%, BB%, GB rate, and Hard Hit rate were all found to be useful in predicting ERA. A linear model was then fitted and was determined to be significant in predicting ERA. Using the linear model, I identified under-performing and over-performing pitchers by finding pitchers whose differences from the predictions were larger than one standard deviation of the average. Nick Pivetta, Vince Velasquez, Jon Gray, and Dylan Bundy were among the underperforming pitchers, while Blake Snell, Hyun-Jin-Ryu, Clay Buchholz, Miles Mikolas, Kyle Freeland, and Dereck Rodriguez were among the overperforming pitchers. Although these factors were useful in predicting ERA, there are still a lot of other factors that contribute to ERA, such as the quality of the opponent a pitcher faces, the quality of the pitcher’s teammates’ defense on his own team, and the stadium in which a pitcher pitches. Going forward, I’d like to see this model expanded on with more potential predictors that aren’t strongly correlated to the ones already used to see if a better fit can be found.

To see the full detailed report with insight on variable selection and model building and with R code
[click here](https://docs.google.com/document/d/1liCsm5YrpBUEe-gMdp5kCOsbBJVUJHyxq0TbSg3us8w/edit?usp=sharing)

