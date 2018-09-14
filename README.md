# Twitter-sentiment-analysis

fetch the tweets and rate them on their sentiment.


Twitter represents a fundamentally new instrument to make social measurements. Millions of people voluntarily express opinions
across any topic imaginable.

The Twitter Application Programming Interface
Twitter provides a very rich REST API for querying the system, accessing data, and control your account.
You can read more about the Twitter API.

Python 2.7.3 environment
If you are new to Python, you may find it valuable to work through the codeacademy Python tutorials. 
Focus on tutorials 1-9, plus tutorial 12 on File IO. In addition, many students have recommended Google's Python class.

Get Twitter Data:
1.	Create a twitter account if you do not already have one.
2.	Go to https://dev.twitter.com/apps and log in with your twitter credentials.
3.	Click "Create New App”
4.	Fill out the form and agree to the terms. Put in a dummy website if you don't have one you want to use.
5.	At this point you will be prompted to attach a mobile phone number to your account if you have not previously done so.
    Follow the instructions at the link provided. If you cannot complete this protocol, you may use the sample dataset in the repository, 
    but we encourage you to connect to Twitter if possible so you can build your own applications.
6.	On the next page, click the "Keys and Access Tokens" tab along the top, then scroll all the way down until you see the section 
    "Your Access Token”
7.	Click the button "Create My Access Token". You can Read more about Oauth authorization.
8.	You will now copy four values into the file twitterstream.py. These values are your "Consumer Key (API Key)", 
    your "Consumer Secret (API Secret)", your "Access token" and your "Access token secret". All four should now be visible 
    on the "Keys and Access Tokens" page. (You may see "Consumer Key (API Key)" referred to as either "Consumer key" or "API Key" 
    in some places in the code or on the web; all three are synonyms.) Open twitterstream.py and set the variables corresponding to the 
    api key, api secret, access token, and access secret.
    
    api_key ="<Enter api key>" api_secret = "<Enter api secret>"
    access_token_key = "<Enter your access token key here>" 
    access_token_secret = "<Enter your access token secret here>”
    
    Now that your keys are ready, you are ready to test your access.
    Run the following and make sure you see data flowing and that no errors occur.$ python twitterstream.py > output.txt

    #Derive the sentiment of each tweet
     
     For this part, you will compute the sentiment of each tweet based on the sentiment scores of the terms in the tweet. 
     The sentiment of a tweet is equivalent to the sum of the sentiment scores for each term in the tweet.
     You are provided with a skeleton file tweet_sentiment.py which accepts two arguments on the command line: a sentiment file.

    $ python tweet_sentiment.py AFINN-111.txt output.txt
    
    #Derive the sentiment of new terms
    
    In this part you will be creating a script that computes the sentiment for the terms that do not
    appear in the file AFINN-111.txt.
    Here's how you might think about the problem: We know we can use the sentiment-carrying words in AFINN-111.txt to deduce the 
    overall sentiment of a tweet. Once you deduce the sentiment of a tweet, you can work backwards to deduce the sentiment of the 
    non-sentiment carrying words that do not appear in AFINN-111.txt. For example, if the word soccer always appears in proximity 
    with positive words like great and fun, then we can deduce that the term soccer itself carries a positive sentiment.

    $ python term_sentiment.py AFINN-111.txt output.txt
    
    

