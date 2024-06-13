# Stop the Steal: The Metaphorical Construction of Disinformation and Conspiracy Theories in Donald Trump's Tweets before and during the Capitol Riots
All data and necessary information for my MA Thesis in Digital Humanities at the University of Groningen

### Corpus Description
This corpus contains several datasets consisting of tweets posted by Donald Trump’s personal Twitter account, @realDonaldTrump. They are built upon the merging of existing datasets: 

| Source      | License                                  |
| ------------- | -------------------------------------------- |
| [Kaggle Dataset by user 'codebreaker619'](https://www.kaggle.com/datasets/codebreaker619/donald-trump-tweets-dataset)  | Data files © Original |
| [The Trump Twitter Archive](https://www.thetrumparchive.com/) | Data is freely usable as the creator aims to “provide a public resource” |
| [Kaggle Dataset by user 'headsortails'](https://www.kaggle.com/datasets/headsortails/trump-twitter-archive)  | CC0: Public Domain | 

### File Format and Content
- `.pdf` Portable document format; includes the Data Management Plan for this project
- `.csv` Comma-separated values; includes (meta)data of Trump's tweets of interest to my research. The csv files are stored in the folder 'datasets`
- `.txt` text-files; includes the cleaned tweets of interest to my research. The txt-files are stores in the folders `trump_tweets_txts` and `trump_tweets_keywords_txts`
- `.ipynb` Jupyter Notebooks used for merging, cleaning, and saving the data for further analysis. Also used for keyword and context-extraction. 

### Text Selection Criteria
in progress of writing

### Data Collection Process
in progress of writing

### Cleaning and Preprocessing
in progress of writing

### Column overview

**`1.final_merged_trump_tweets_clean.csv`**

| Variable      | Description                                  |
| ------------- | -------------------------------------------- |
| id          | the tweet id |
| text  | the original content of the tweet    |
| is_retweet     | true or false: is the tweet a retweet? |
| is_deleted | true or false: has the tweet been deleted?                |
| favorites  | amount of favorites the tweet has |
| retweets   | amount of retwets the tweet has  |
| date  | date of the tweet  |
| text_clean  | the cleaned content of the tweet  |

**`2.filtered_trump_tweets.csv`**

Filtered to dates of interest for this research, namely November 3rd, 2020 - January 6th, 2021

| Variable      | Description                                  |
| ------------- | -------------------------------------------- |
| id          | the tweet id |
| text  | the original content of the tweet    |
| is_retweet     | true or false: is the tweet a retweet? |
| is_deleted | true or false: has the tweet been deleted?                |
| favorites  | amount of favorites the tweet has |
| retweets   | amount of retwets the tweet has  |
| date  | date of the tweet  |
| text_clean  | the cleaned content of the tweet  |


**`3.filtered_trump_tweets_keywords.csv`**

Filtered to dates, namely November 3rd, 2020 - January 6th, 2021 and keywords of interest to my research

Keywords: *'election', 'antifa', 'dominion', 'vote', 'fraud', 'steal', 'steal', 'flip', 'glitch', 'michigan', 'georgia', 'undermine', 'stop', 'collapse', 'ballot', 'conspiracy', 'lie', 'hoax', 'power', 'reject', 'certify', 'fbi', 'legal', 'illegal', 'overturn', 'biden', 'trump', 'integrity', 'justice', 'win', 'win', 'poll', 'evidence', 'rig', 'landslide', 'fake', 'verify'*

| Variable      | Description                                  |
| ------------- | -------------------------------------------- |
| id          | the tweet id |
| text  | the original content of the tweet    |
| is_retweet     | true or false: is the tweet a retweet? |
| is_deleted | true or false: has the tweet been deleted?                |
| favorites  | amount of favorites the tweet has |
| retweets   | amount of retwets the tweet has  |
| date  | date of the tweet  |
| text_clean  | the cleaned content of the tweet  |
| doc  | The tweet as processed by using spaCy | 
| lemmas  | lemmatization of the tweet | 

**`4.candidate_metaphor_trump_tweets.csv`**
Filtered to the rows that include a candidate metaphor keyword. 

keywords_metaphors: *"abuse", "attack", "battle", "betray", "chapter", "cesspool", "crooked", "cure", "defend", "destroy", "drench", "dump", "fight", "flood", "game", "garbage", "goldmine", "harvesting", "hill", "hustle", "inundate", "kill", "landslide", "lose", "play", "plague", "pour", "run", "race", "save", "shatter", "sick", "silent", "sleepy", "spearhead", "steal", "stuff", "tank", "thin", "toss", "turtle", "undermine", "victory", "war", "witch"*
    
| Variable      | Description                                  |
| ------------- | -------------------------------------------- |
| id          | the tweet id |
| text  | the original content of the tweet    |
| is_retweet     | true or false: is the tweet a retweet? |
| is_deleted | true or false: has the tweet been deleted?                |
| favorites  | amount of favorites the tweet has |
| retweets   | amount of retwets the tweet has  |
| date  | date of the tweet  |
| text_clean  | the cleaned content of the tweet  |
| doc  | The tweet as processed by using spaCy | 
| lemmas  | lemmatization of the tweet | 
| contains_metaphor  | returns true for matching keywords | 

**`5.context_candidate_metaphor_trump_tweets.csv`**

Includes the necessary meta data, and a row including the context around the metaphor for quicker human analysis.

| Variable      | Description                                  |
| ------------- | -------------------------------------------- |
| id          | the tweet id |
| date  | date of the tweet  |
| text  | the original content of the tweet    |
| context  | words surrounding metaphor keyword, up to 8 words  |
| is_retweet     | true or false: is the tweet a retweet? |
| is_deleted | true or false: has the tweet been deleted?                |
| favorites  | amount of favorites the tweet has |
| retweets   | amount of retwets the tweet has  |
| lemmas  | lemmatization of the tweet | 

**`6.metaphor_trump_tweets.csv`**

All rows now include an identified metaphor.

| Variable      | Description                                  |
| ------------- | -------------------------------------------- |
| id          | the tweet id |
| text  | the original content of the tweet    |
| is_retweet     | true or false: is the tweet a retweet? |
| is_deleted | true or false: has the tweet been deleted?                |
| favorites  | amount of favorites the tweet has |
| retweets   | amount of retwets the tweet has  |
| date  | date of the tweet  |
| text_clean  | the cleaned content of the tweet  |
| doc  | The tweet as processed by using spaCy | 
| lemmas  | lemmatization of the tweet | 

