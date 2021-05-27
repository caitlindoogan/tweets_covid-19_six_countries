# Data dictionary - Tweets
The data you retrive using the tweet ids provided will depend on your choice of tweet rehydration method and what you aim to do with these tweets. These choices will dictate what tweet objects you retrieve using the tweet id. 

The tweet object is the foundation of the Twitter object model. Tweet objects serve as the 'parent' object for several child objects, including user, media, poll and place objects. The object model is specific to the API version you are using (Twitter, 2021). 

There are numerous root fields in the tweet object, including id, text, and created_at.  We used the Twitter API v1.1 You should refer to the data dictionary specific to the version of the API you are using. 
- The data dictionary for the Standard v1.1 API can be accessed [here](https://developer.twitter.com/en/docs/twitter-api/v1/data-dictionary/object-model/tweet).
- The data dictionary for the new Twitter API v2 can be accessed [here](https://developer.twitter.com/en/docs/twitter-api/data-dictionary/introduction)

The following table summarises the key field values retrieved for this project. Additionally, the datatype, description, and use case for each field value are displayed.

| **Field value** | **Type**       | **Description** | **Use case**    |
| --------------- | -------------  | ------- | --------------- | 
| id           | string | The tweet's unique identified, a string of 17-20 numbers. e.g. `"id":"108717649843652962"` | This can be used to reconstruct a message based on a Tweet.|
| created_at | date (ISO8601)| This field can be used to determine the time a Tweet was created. `"created_at": "2019-06-04T23:12:08.000Z"` | This can be used for event detection and time series analysis, among other things.|
| author_id | string | The user's unique identifier of the user who created the tweet. `"author_id": "1764387110264"`| Used to hydrate the user object or for input into techniques such as social network analysis.
| conversation_id | string | The tweet's id which began a conversation which includes replies and replies to replies. `"conversation_id": "1556752366219013838"`| This can be used to reconstruct discussions based on a Tweet. |
| text | string| The tweet's UTF-8 text. `"text": "The text of a tweet includes emojis."`| Analytic techniques including topic modelling, text classification, sentiment analysis and keyword extraction.|


Only the `id` has been supplied for the datasets provided, as per the Twitter developer policy. 
