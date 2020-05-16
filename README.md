# Mining-the-Social-Web

[![License MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

### Introduction
This application pulls the textual data of several posts made on Tumblr's network, and determines the sentiment of these posts as being either negative, neutral, or positive via Natural Language Processing (NLP) techniques and Random Forest Classification.

It also uses other text data pulled using the APIs of Twitter and Reddit; which is not shown in this code because this application is only a portion of a larger project.


### Purpose of this application
In our current age, social media reigns supreme in the exchange and spread of news and information. It could be said that it is sort of like a gold mine of data. There is a plethora of ways to utilize this abundance of data, but this application is simply one of many examples of what we could use this data for.


## Step-by-step explanation of the application:
### 1. Interacting with the API
- It accesses the Application Programming Interface (API) for Tumblr.
Permission to use their API must be given directly from Tumblr in the form of access tokens and access keys.

- The client.tagged() function, provided from the API, is used to initiate a search for several posts related to a specific keyword (which is currently set to "Macintosh") and presents the metadata for each post.

- The pullPost() function is then used to specifically extract the textual data from each post's metadata.

### 2. Processing the text data
- The extracted text data is cleaned out by using the preProc() function. It utilizes regular expressions to remove special characters, numbers, and url's, leaving only the words from each sentence/post.

-  "Stop-words" (words with little contextual meaning) are filtered out of the text data. Such that only the most meaningful words are being evaluated during sentiment analysis.

- The processed text data is then fed through a Skip Gram Model to create vector representations of each word.

- The application calls the makeMatrix() function to create vector representation for each sentence/post using the word vectors.

- All of the actions in Step 2 was also executed on a predefined data set from [another GitHub repository](https://github.com/kolaveridi/kaggle-Twitter-US-Airline-Sentiment-).

### 3. Sentiment analysis
- The application utilizes a Fandom Forest model to act as the sentiment classifier model; and will be trained using the aforementioned predefined data from Step 2.

- After training the classifier model with the predefined data, the classifier model is used on the post vectors of the pulled data from Tumblr, Twitter, and Reddit.

### 4. Sample output / Predicted Sentiments

![Predicted-Sentiments](https://github.com/Dennis-Kgxay/Mining-the-Social-Web/blob/master/images/Ouput.png)
