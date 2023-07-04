# Sentiment Analysis for Apple Marketing's SXSW Review

## Business Understanding

This is a review of reception of the Apple brand (approximated by Twitter) at this year's South by Southwest tech conference to help Apple's marketing team prepare the brand's strategy for next year's SXSW conference.

## Data Understanding

~8000 tweets from SXSW directed towards Apple, Google and Android (sourced from Crowdflower)

## Data Analysis

- Apple is mentioned far more often than Google or Android, and the ratio of positive to negative tweets towards Apple exceeds 4:1.

- The release of the iPad 2 and the iPad giveaway, as well as the pop-up store in downtown Austin, are received extremely positively and receive a lot of positive mentions, though the iPad2 is also the most frequently mentioned word in negative tweets.

## Modeling

The goal was to build a classifier for positive and negative tweets, then use the model's confidence score as a rating (i.e. a model confidence of 0.84 in the positive class would be interpreted as, this tweet is 84% positive.)

## Evaluation

Primarily, accuracy was used as the metric of evaluation. Balanced accuracy was also considered when further tuning the model with selected hyperparameters.

## Results

Upon inspection, the "best" model according to accuracy / balanced accuracy was not well-suited to classify the most positive and most negative tweets.

## Next Steps

Try building two classifiers -- one to optimize negative class precision and the other to optimize positive class precision. These models may be better suited to rate the most negative and positive tweets, respectively.
