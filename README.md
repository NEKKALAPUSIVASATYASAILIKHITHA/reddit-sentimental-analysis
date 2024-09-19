reddit-sentiment-analysis
This program goes through reddit, finds the most mentioned tickers and uses Vader SentimentIntensityAnalyzer to calculate the ticker compound value.

Program Parameters
subs = []           sub-reddit to search
post_flairs = {}    posts flairs to search || None flair is automatically considered
goodAuth = {}       authors whom comments are allowed more than once
uniqueCmt = True    allow one comment per author per symbol
ignoreAuthP = {}    authors to ignore for posts
ignoreAuthC = {}    authors to ignore for comment 
upvoteRatio = float upvote ratio for post to be considered, 0.70 = 70%
ups = int           define # of upvotes, post is considered if upvotes exceed this #
limit = int         define the limit, comments 'replace more' limit
upvotes = int       define # of upvotes, comment is considered if upvotes exceed this #
picks = int         define # of picks here, prints as "Top ## picks are:"
picks_ayz = int     define # of picks for sentiment analysis
How to run:
pip install -r requirements.txt
python3 reddit-sentiment-analysis.py
Sample Output
It took 1574.61 seconds to analyze 14236 comments in 8 posts in 1 subreddits.

Posts analyzed saved in titles

10 most mentioned picks:
GME: 764
SPCE: 183
PLTR: 89
TSLA: 71
MVIS: 42
NVDA: 34
AMD: 30
F: 29
TLRY: 29
AAPL: 26

Sentiment analysis of top 5 picks:
         Bearish  Neutral  Bullish  Total/Compound
GME   0.087   0.707    1.548     0.030
SPCE   0.119   0.645    1.618     0.027
PLTR   0.073   0.649    1.751     0.032
TSLA   0.088   0.650    1.543     0.049
MVIS   0.155   0.698    1.714     -0.020 
