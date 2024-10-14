# Twitter Sentiment Analysis

## Project Overview

Twitter Sentiment Analysis is a project that uses the **Tweepy** library to fetch tweets and **TextBlob** to analyze the sentiment of those tweets. The sentiment can be classified as **positive**, **negative**, or **neutral**, based on the tweet content. This project aims to provide insights into how people feel about a particular topic, event, or public figure by analyzing a set of tweets.

## Project Structure

- **TwitterClient Class**: This class handles the interaction with Twitter's API, including authenticating and fetching tweets.
- **Text Cleaning**: The project includes a function to clean the tweet text by removing URLs, mentions, and special characters.
- **Sentiment Analysis**: Sentiment is determined using TextBlob, which calculates the polarity of a tweet (positive, negative, or neutral).
- **Environment Variables**: API keys and secrets are securely handled using environment variables to avoid hardcoding sensitive information.
  
## Technologies Used

- **Python**: The main programming language.
- **Tweepy**: For accessing the Twitter API.
- **TextBlob**: For natural language processing and sentiment analysis.
- **Jupyter Notebook**: Used for writing and running the code.
- **Environment Variables**: Used to handle API credentials securely using the `os` module.

## Setup Instructions

### Prerequisites

- Python 3.x
- Twitter Developer Account for API access (You'll need to generate your own API keys from [Twitter Developer Portal](https://developer.twitter.com/)).
- Install the required libraries:
  
  ```bash
  pip install tweepy textblob

## Code Explanation
### Authentication
- The project uses the Tweepy library to authenticate with the Twitter API. The credentials (consumer key, consumer secret, access token, and access token secret) are stored securely as environment variables and fetched using the os.getenv() method.

### Tweet Cleaning
- The clean_tweet() function uses regular expressions to remove URLs, Twitter mentions, and special characters from the tweet text, making the data cleaner for analysis.

### Sentiment Analysis
- The get_tweet_sentiment() function leverages TextBlob to calculate the sentiment polarity of a tweet:

- Positive: Polarity > 0
- Neutral: Polarity = 0
- Negative: Polarity < 0
- Fetching Tweets
- The get_tweets() function fetches tweets based on a user-defined query and number of tweets. It then classifies each tweet as positive, negative, or neutral.

### Results
The script outputs:

- Percentage of positive tweets.
- Percentage of negative tweets.
- Percentage of neutral tweets.
- A sample of the first 10 positive and negative tweets for review.

  ```bash
  Positive tweets percentage: 45.50 %
  Negative tweets percentage: 32.25 %
  Neutral tweets percentage: 22.25 %

  Positive tweets:
  1. "I love the new policy that..."
  2. "Great job on the recent progress..."
  3. ...

  Negative tweets:
  1. "I can't believe this decision was made..."
  2. "Horrible outcome of the recent..."
  3. ...

## Project Results
Based on the search query (e.g., 'Donald Trump'), the project fetches a set of tweets and calculates the sentiment of each tweet using TextBlob. It then provides an analysis of the sentiment distribution:

- Positive Tweets Percentage: Shows the proportion of tweets with a positive sentiment.
- Negative Tweets Percentage: Shows the proportion of tweets with a negative sentiment.
- Neutral Tweets Percentage: Shows the proportion of tweets with a neutral sentiment.
- The user can also view a sample of tweets for each sentiment category (positive and negative) to gain deeper insights into the kinds of opinions being expressed.
