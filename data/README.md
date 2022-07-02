# DATA FOLDER
Contains three files such as:
- `data_complete.json`
- `final_user_classification.json`
- `hashtags_classification.json`


## `data_complete.json`
Contains all extracted tweets anonimizied.
The structure of a tweet is as follows:
```
{
    "tweet_id": string,
    "user": string,
    "date": string,
    "hashtags": string[],
    "mentions": [],
    "retweets": [],
    "reply_to": [],
    "quote_to": [],
    "followers": number,
    "following": number,
    "tweets": number,
    "tweet_classification": number,
    "user_classification": float,
    "vip": boolean
}
```

## `final_user_classification.json`
Contains all users of the extracted tweets with their relative classification, based on the file `hashtags_classification.json`

## `hashtags_classification.json`
It contains all the hashtags of the extracted tweets with their relative classification.
A numerical value was associated with each hashtag in the dataset: 
- ±3 if the hashtag expresses a position strongly against (+)/strongly in favor(-) of the act of kneeling, 
- ±1 if the hashtag is significant in that it is close to the motives of the faction opposed (+)/for(-) the gesture, but not specific on the issue of "kneeling"
- 0 for neutral and/or irrelevant hashtags.