# Stock Market Sentiment Analysis Script using Polygon.io and OPEN.ai CHAT-GPT 3.5-Turbo #

## Application Functional Summary ##

This application is a sentiment analysis tool for stock market news. It uses both the Vader sentiment analysis tool from the Natural Language Toolkit (NLTK) and the OpenAI API to analyze the sentiment of news articles related to specific stock tickers.

The application uses API keys from the environment variables. The keys that it uses are for OpenAI and Polygon.io. Stock tickers are obtained from a CSV file named `Tickers.csv` (not stored with the code).

The application saves news articles and sentiment analysis results to SQLite databases, and it also prints a final report with the aggregated sentiment scores for all stock tickers.

## Required or Suggested Programs ##

Python 3.6 or higher is required to run this application. You'll also need several Python libraries which you can install using provided `requirements.txt`

## API Keys and Websites ##

You'll need API keys for the following services:

 * [OpenAI](https://www.openai.com/)
 * [Polygon.io](https://polygon.io/)

Register and export access tokens in the `OPENAI_API_KEY` and `POLYGON_API_KEY` environment variables.

Remember to always keep your API keys secure and never share them publicly.

## Areas for Improvement ##

### Aggregated Scores Algorithm ###
The current algorithm for calculating the aggregated score is quite simple, and it might not accurately reflect the actual sentiment of the news articles. This could be improved by using a more sophisticated sentiment scoring algorithm, perhaps one that takes into account more nuanced aspects of the news articles.

### GPT Prompt ###
The prompt used for GPT-3 could potentially be improved. Currently, it asks the model to categorize the sentiment of an article as 'Good', 'Bad', or 'Unknown'. This could be expanded to include more nuanced sentiments, or to ask for a more detailed analysis of the article.

### Expanding the Inputs to the Sentiment Analysis ###
Currently, the application only considers the title and description of each news article for sentiment analysis. This could be expanded to include other elements of the articles, such as the main body text, or even comments on the article if available.

### Expand to More Data Sources ###
Currently, the application only uses news articles from Polygon.io. It might be beneficial to include more data sources to get a more comprehensive view of the sentiment around each stock ticker.

### Error Handling and Logging ###
While the application does some error handling, it could be improved by adding more detailed logging, so that if something goes wrong, it's easier to diagnose the problem.

### Code Optimization ###
Some parts of the code could potentially be optimized for better performance, especially the parts that involve making requests to external APIs or querying the database.
