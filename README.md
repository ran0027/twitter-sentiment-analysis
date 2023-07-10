# Sentiment Analysis for Apple Marketing's SXSW Review

## Business Understanding

This is a review of reception of the Apple brand (approximated by Twitter) at this year's South by Southwest tech conference to help Apple's marketing team prepare the brand's strategy for next year's SXSW conference.

## Data Understanding

~8000 tweets from SXSW directed towards Apple, Google and Android (sourced from Crowdflower)

Ultimately, a classifier was built using only those tweets which were classified as having a sentiment of "positive emotion" or "negative emotion". As illustrated by the bar chart below, this is an imbalanced classification problem.

![Bar Graph showing Class Distribution](data/graphs/class_dist.jpg)

## Data Analysis

- Apple is mentioned far more often than Google or Android, and the ratio of positive to negative tweets towards Apple exceeds 4:1.

- The release of the iPad 2 and the iPad giveaway, as well as the pop-up store in downtown Austin, are received extremely positively and receive a lot of positive mentions, though the iPad2 is also the most frequently mentioned word in negative tweets.

## Modeling

The goal was to build a classifier for positive and negative tweets, then use the model's confidence score as a rating (i.e. a model confidence of 0.84 in the positive class would be interpreted as, this tweet is 84% positive.)

## Evaluation

Primarily, accuracy was used as the metric of evaluation. Balanced accuracy was also considered when further tuning the model with selected hyperparameters. In hindsight, using balanced accuracy for all tuning, or building two models (one tuned for negative class precision and the other for positive class precision) would have been a more valuable metric.

**Classification Report (Hold-Out Test Set)**

| Class | Precision | Recall | F1 Score | Support |
| --- | --- | --- | --- | --- |
| Negative Tweets | 0.39 | 0.58 | 0.47 | 107 |
| Positive Tweets | 0.92 | 0.84 | 0.88 | 603 |

The model itself didn't provide a lot of insight, though the exploratory data analysis performed in preparation for modeling yielded some valuable insights about what caused Apple to receive so much positive attention on Twitter at this year's SXSW conference.

## Recommendations

Based on exploratory data analysis performed prior to the modeling stage, I recommend that Apple's marketing team considers another pop-up store at next year's SXSW and timing the release of a new product with the conference again, if possible, as part of their conference strategy.
 
The pop-up store downtown and the iPad 2 launch / giveaway garnered an overwhelmingly positive and relatively large amount of attention on Twitter at this year's conference, and they made Apple the focal point of SXSW (at least, on Twitter.)

## Next Steps

Try building two classifiers -- one to optimize negative class precision and the other to optimize positive class precision. These models may be better suited to rate the most negative and positive tweets, respectively.
