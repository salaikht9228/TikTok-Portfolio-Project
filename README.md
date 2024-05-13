# Random Forest Classification of TikTok Videos

## Overview
This project aimed to create a logistic regression, random forest, and XGBoost model to predict whether the videos posted on TikTok contain claims or opinions. This project utilized a dataset called [tiktok_dataset.csv], which contains synthetic data created for this project in partnership with TikTok. The final champion random forest model performed with 99.87% accuracy and 99.74% recall, determining what features were most important in separating claims from opinions. Based on the model, features associated with user engagement levels with each video, namely the video's view, like, share, and download counts, were most influential in determining a video with a claim vs a video with an opinion.

## Business Understanding
According to socialchamp.io and statista.com, 34 million videos are posted on TikTok daily, with approximately 1.5 million videos removed each day for violating TikTok's Community Guidelines. Videos with claims are significantly more likely to contain content that breaches the platform's terms of service. Given the high volume of reported videos, it's impractical for human moderators to review them all. Therefore, developing a machine learning classification model to predict whether a video contains a claim or opinion could greatly assist in directing these videos to human moderators for further review.

## Data Understanding
The data consisted of 19084 unique uploaded videos and 12 features. The features included information on video claim status, video duration in seconds, video transcription text, users verified status, users ban status as well as video's view, like, share, download and comment counts. The pie chart below shows the breakdown of how many videos with claims versus videos with opinions that exist in the data set.

In connection to this, two new features were engineered based on the video transcription text variable. First new feature is the numbers of words in each video. Second new feature is the collection of words that appear most frequently in all of the uploaded videos' transcription text using scikit learn CountVectorizer package. Multiple redundent columns were dropped and reformatted into the proper data type to build machine learning models.

## Modeling and Evaluation
A random forest model comprising xx decision trees was used to determine feature importance in which videos contain claims or opinions. The below plot shows that number of video views, likes, shares and downloads were the most important factors in determining a claim video from opinion video. The overall model performed with 99.87% accuracy and 99.74% recall.

## Conclusion
This model can greatly benefit TikTok's human moderators by filtering out videos classified as claims. Only these videos will be sent to the moderators for further review, significantly saving time and effort. However, running a logistic regression model using these features may help to provide insights into how much each variables will influence the likelihood of video containing claims. Furthermore, monitoring the distributions of video engagement levels will ensure that the model remains robust to fluctuations in its most predictive features.
