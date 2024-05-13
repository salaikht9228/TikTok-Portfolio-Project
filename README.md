# Random Forest Classification of TikTok Videos

## Overview
This project aimed to create a logistic regression, random forest, and XGBoost model to predict whether the videos posted on TikTok contain claims or opinions. This project utilized a dataset called [tiktok_dataset.csv](data/tiktok_dataset.csv), which contains synthetic data created for this project in partnership with TikTok. The final champion random forest model performed with 99.87% accuracy and 99.74% recall, determining what features were most important in separating claims from opinions. Based on the model, features associated with user engagement levels with each video, namely the video's view, like, share, and download counts, were most influential in determining a video with a claim vs a video with an opinion. [Overview of features associated with user engagement levels can be found on Tableau Public.](https://public.tableau.com/views/TikTokPortfolioProject_17152345366470/Story1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link)

## Business Understanding
According to socialchamp.io and statista.com, 34 million videos are posted on TikTok daily, with approximately 1.5 million videos removed each day for violating TikTok's Community Guidelines. Videos with claims are significantly more likely to contain content that breaches the platform's terms of service. Given the high volume of reported videos, it's impractical for human moderators to review them all. Therefore, developing a machine learning classification model to predict whether a video contains a claim or opinion could greatly assist in directing these videos to human moderators for further review.

## Data Understanding
The data consisted of 19084 unique uploaded videos and 12 features. The features included information on video claim status, video duration in seconds, video transcription text, user verified status, users' ban status, as well as video's view, like, share, download, and comment counts. The pie chart below shows how many videos with claims versus videos with opinions exist in the data set.

![pie chart](https://github.com/salaikht9228/TikTok-Portfolio-Project/blob/main/Images/Claim%20vs%20Opinion.jpeg)

In connection with this, two new features were engineered based on the video transcription text variable. The first new feature is the number of words in each video. The second new feature is the collection of words that appear most frequently in all of the uploaded videos' transcription text using the scikit learn CountVectorizer package. Multiple redundant columns were dropped and reformatted into the proper data type to build machine-learning models.

## [Modeling and Evaluation](https://github.com/salaikht9228/TikTok-Portfolio-Project/blob/main/TitTok%20Claim%20Project.ipynb)
A random forest model comprising 100 decision trees was used to determine the feature importance of videos containing claims or opinions. The plot below shows that the numbers of video views, likes, shares, and downloads were the most important factors in determining a video with a claim from a video with an opinion. The overall model performed with 99.87% accuracy and 99.74% recall.

![Feature Importance](https://github.com/salaikht9228/TikTok-Portfolio-Project/blob/main/Images/Feature%20Importance.jpeg)

## Conclusion
This model can greatly benefit TikTok's human moderators by filtering out videos classified as claims. Only these videos will be sent to the moderators for further review, significantly saving time and effort. However, running a logistic regression model using these features may help provide insights into how much each variable will influence the likelihood of a video containing claims. Furthermore, monitoring the distribution of video engagement levels will ensure that the model remains robust to fluctuations in its most predictive features.
