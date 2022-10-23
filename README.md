# Beer-data-analytics-and-statistics
## Introduction
In this project, the beer company want to design a new product, so the beer data is cleaned, observed, and analysed through the statistics test. 

The tests mainly focus on rating scores, types of beers, ABV, Sweet and Malty flavours. 
At the end of the project (in the section 2), the statistical results and business insights are presented.

--------------------------------------------------------------------------------------------------------------------------------------------------------

## Analysis and business insights
This report presents a data analysis for a beer company. The company want to know whether particular types of beers has higher rating score. In this report, beers are categorised into nine categories (IPA, Lager, Porter, Stout, Wheat, Pale, Pilsner, and Bock) by detecting the strings and identifiers shown in Style column. Afterwards, confidence intervals and means are invested, and the outcomes demonstrated that the means and CIs of rating for each category fall around 3 and 4. 

To further the investigation, most of the categories are more concentrated to their means, except for the Lager and Others categories. More specifically, the data of Lager and Others categories are more scattered according to the violin plot. That is, their ratings are various. Also, the mean of data in Lager category has a lower average rating comparing to other categories.

The company also wants to get insights from the data to design a new high-rating product. From the data, we have 5,558 beers and also their properties, including their names, rating score, and multiple flavourings.

According to the graph, linear regression, and correlation test, it can show that rating, ABV, Sweet, and Malty are all positive but low or little correlated. From the correlation test, ABV has higher correlation with rating comparing to other variables. Increasing one unit of ABV would increase the rating by an average of 0.08 points (coefficient = 0.08, 95%CI[0.0755, 0.0844]). Moreover, the p-value of ABV to the rating is significance difference (p-value < 0.05, t(5538) = 35.34), so it can be concluded that ABV is also a significant predictor towards the rating.

Furthermore, based on the historical data, it can be proved that as the ABV increases, the rating would increase.

Further, based on the model comparison between main effect and interaction effect model (ANOVA test), it can be concluded that the interaction effect model is better because the p-value is less than 0.001, which means the model with the interaction term is significantly improved (F(4, 5532) = 27.827, p-value < 0.001). Thus, the interaction term should be considered when analyze the data.

From the interaction effect model, we can see that Sweet, Malty, and ABV are significant predictors of the model with the p-value lower than 0.001. Moreover, only Malty negatively affects the rating, which means increasing one unit of Malty would decrease 0.003 in the rating. For the Sweet property, increasing one unit of Sweet would lead to an increase of 0.00638 points towars rating(p-value < 0.001, t(5532) = 8.355, coefficient = 0.00638, 95%CI[0.0049, 0.0079]).

For the interaction term only the interaction of Sweet and ABV and the interaction of Malty of ABV are associated with rating. What's more, the interaction of Sweet and ABV is negatively associated to the rating (p-value < 0.001, t(5532) = 6.265, coefficient = -0.0006223, 95%CI[-0.0008, -0.0004]). Although ABV has a positive impact (p-value < 0.001, t(5532) = 13.942, coefficient = 0.08, 95%CI[0.0689, 0.0915]) towards rating, when it interacted with Sweet property, the rating would be negatively impacted. In comparison, the interaction of Malty and ABV positively influence the rating (p-value < 0.001, t(5532) = 4,886, coefficient = 0.0004669, 95%CI[0.0003, 0.0007]).

To investigate how to maximise the rating based on the variables ABV, Sweet, and Malty, the 0.9 and 0.1 quantile of ABV are adopted, and the maximum and minimum of Sweet and Malty are used to predict the rating with the ABV.

According to the graphs and tables about the relationship between ABV, rating, and Sweet/Malty shown above, it can be concluded that to maximise the rating, Sweet should not be added when ABV is high (quantile = 0.9). In contrary, Malty flavours has positive impact towards the rating when ABV is high (quantile = 0.9), so Malty could be added more under high ABV. Also, the rating would increase when Sweet increases or Malty decreases as ABV is low (quantile = 0.1).

According to the findings, if the company are creating a high ABV beer, they should not add Sweet but Malty. On the other hand, for the low ABV beer, the company should add more Sweet and not malty to maximise the rating score.
Accordingly, with higher or lower ABVs, the company should execute different plan to design its product.
