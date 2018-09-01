# Amazon-Sentiment-Analysis
Here the dataset used is from kaggle.<br>
We try to understand the sentiment of the review based on the text under summary and review<br>.
The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.
* Dataset link https://www.kaggle.com/snap/amazon-fine-food-reviews <br> 
Number of reviews: 568,454<br>
Number of users: 256,059<br>
Number of products: 74,258<br>
Timespan: Oct 1999 - Oct 2012<br>
Number of Attributes/Columns in data: 10 

Attribute Information:

1. Id
2. ProductId - unique identifier for the product
3. UserId - unqiue identifier for the user
4. ProfileName
5. HelpfulnessNumerator - number of users who found the review helpful
6. HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not
7. Score - rating between 1 and 5
8. Time - timestamp for the review
9. Summary - brief summary of the review
10. Text - text of the review


#### Objective:
Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).

[Q] How to determine if a review is positive or negative?<br>
<br> 
[Ans] We could use the Score/Rating. A rating of 4 or 5 could be cosnidered a positive review. A review of 1 or 2 could be considered negative. A review of 3 is nuetral and ignored. This is an approximate way of determining the polarity (positivity/negativity) of a review.

#### Loading the data
The dataset is available in two forms
1. .csv file
2. SQLite Database

Here as we only want to get the global sentiment of the recommendations (positive or negative), we will purposefully ignore all Scores equal to 3. If the score id above 3, then the recommendation wil be set to "positive". Otherwise, it will be set to "negative".

##### Types of text preprocessing done
* Count BOW 
* Binary BOW
* TFIDF
* Average Word2Vec
* TFIDF Word2Vec
#### Models Used
* KNN
* Naive Bayes
