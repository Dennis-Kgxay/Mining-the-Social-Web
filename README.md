# Mining-the-Social-Web
Pulls textual data of several posts made on Tumblr's network, and determines the sentiment of these posts.  
Also uses text data pulled from Twitter and Reddit to diversify results.

[![License MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

# Step-by-Step Process of the Application:
### 1. Interacting with the API
- Access the Application Programming Interface (API) for Tumblr.
Permission to use their API must be given directly from Tumblr in the form of access tokens and access keys.

- client.tagged() is a method provided from the API to initiate a search for several posts related to a specific keyword (which is currently set to "Macintosh") and presents the metadata for each post.

- pullPost() is a function that was defined to specifically extract the textual data from each post's metadata.

### 2. Processing the Text Data
- The extracted text data is cleaned out by using the preProc() function. It utilizes regular expressions to remove special characters, numbers, and url's, leaving only the words from each sentence/post.

-  "Stop-words" (words with little contextual meaning) are filtered out of the text data. Such that only the most meaningful words are being evaluated during sentiment analysis.

- The processed text data is then fed through a Skip Gram Model to create vector representations of each word.

- After 

# Sample Output

![Predicted-Sentiments](https://github.com/Dennis-Kgxay/Mining-the-Social-Web/blob/master/images/Ouput.png)
