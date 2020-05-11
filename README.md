# Mining-the-Social-Web
Pulls textual data of several posts made on Tumblr's network, and determines the sentiment of these posts.  
Also uses text data pulled from Twitter and Reddit to diversify results.

# Step-by-Step Process of the application:
### 1. Interacting with the API
- Access the Application Programming Interface (API) for Tumblr.
After gaining permission from Tumblr to use their API and receiving access tokens to the API, the respective package is imported into the source code (import pytumblr).

- client.tagged() is a method provided from the API to initiate a search for several posts related to a specific keyword (which is currently set to "Macintosh") and present the metadata foe each post.

- pullPost() is a function that was defined to specifically pull the textual data from each post's metadata.

### 2. Processing the Text Data
-  

# Sample Output

![Predicted-Sentiments](https://github.com/Dennis-Kgxay/Mining-the-Social-Web/blob/master/images/Ouput.png)
