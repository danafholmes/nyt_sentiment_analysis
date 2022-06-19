# nyt_sentiment_analysis

A project to retrieve and analyze sentiment of NYT comments for a given article using Jupyter Notebooks and some off the shelf sentiment analysis libraries.

You should actually be able to run this assuming you can succesfully install flair in your python env (good luck...) and TextBlob.

If you want to retrieve freshy fresh comments to analyze, you'll need an NYT API key:

https://developer.nytimes.com/apis

And to enable the community API endpoint. 

Make sure to leave the 7 seconds of sleep between API calls or you'll get rate limited. Outside of that the free tier is quite generous, and you can make 4k calls a day. You could easily hit that mining comments for a month of articles, but for just one or two, you won't come anywhere close.

API secret goes in env variable called NYT SECRET.

# Notes

- Community endpoint has been deprecated as of June 2022, so this won't run any longer :(
- The sentiment analysis scores are lousy. The models were trained on review datasets and don't seem to work very well for this sort of comment, assuming one's goal is to measure use sentiment about the issue(s) in the article.
- This was mostly a project to play with API calls, JSON/pandas data manipulation, etc. - not build a useful analysis pipeline.
