# STOP THE STEAL: The Metaphorical Construction of Disinformation and Conspiracy Theories in Donald Trump's Tweets before and during the Capitol Riots
All data and necessary information for my MA Thesis in Digital Humanities at the University of Groningen. This also included data for further study. 

### Thesis Abstract
The 2020 U.S. presidential election marked an important moment in American politics, in particular, because of the controversy surrounding its outcome and the Capitol Riots that followed. This thesis investigates how disinformation and conspiracy theories are metaphorically constructed and contribute to populist polarization by analyzing the tweets of former U.S. President Donald Trump during this turbulent period. By analyzing a corpus of @realDonaldTrump tweets, ranging from November 3, 2020, to January 6, 2021, this thesis identifies narratives of election fraud, mail-in ballot corruption, and a belief that Trump has won the election, which played a center-stage role in the disinformation and conspiracy theories Trump draws upon in this timeframe. This is followed by an examination of the conceptual metaphors Trump systematically employs to construct these narratives, specifically those in the metaphor themes of WAR, PROPERTY, and NATURE. By performing a Critical Metaphor Analysis, the research demonstrates how these metaphors framed the election as a battle, depicted the results as stolen property, and described the situation as a natural disaster. The findings indicate that these metaphors not only shaped Trump’s supporters’ perceptions of the election outcome but also intensified their emotional responses, leading to increased polarization amongst the electorate. Ultimately, this thesis contributes to a deeper understanding of the role played by discourse in contemporary populism, shedding light on how metaphorical constructions of conspiracy theories and disinformation contribute to political polarization. By examining the mechanisms through which populist leaders shape public discourse, this study offers valuable insights into the challenges posed by the weaponization of disinformation and conspiracy theories in democratic societies.

### Corpus Description
This corpus contains several datasets consisting of tweets posted by Donald Trump’s personal Twitter account, @realDonaldTrump. They are built upon the merging of existing datasets: 

| Source      | License                                  |
| ------------- | -------------------------------------------- |
| [Kaggle Dataset by user 'codebreaker619'](https://www.kaggle.com/datasets/codebreaker619/donald-trump-tweets-dataset)  | Data files © Original |
| [The Trump Twitter Archive](https://www.thetrumparchive.com/) | Data is freely usable as the creator aims to “provide a public resource” |

### File Format and Content
- `.ipynb` Jupyter Notebooks used for merging, cleaning, and saving the data for further analysis. Also used for keyword and context-extraction. The notebooks are stored in the `Notebooks` folder.
- `.csv` Comma-separated values; includes (meta)data of Trump's tweets of interest to my research. The orignal datasets are stored in the folder `Original_Data` and the
- datasets merged, cleaned, and filtered for this research are in the folder `STS_Datasets`.
- `.txt` text-files; includes the cleaned tweets of interest to my research. The txt-files are stores in the `trump_tweets_txts` folder.
- `.pdf` Portable document format; includes the Data Management Plan for this project


### Text Selection Criteria
As this thesis is concerned with Trump's rhetoric after the 2020 election until the Capitol Riots, the first criteria was making sure our data would display this timeframe. First, I downloaded all his tweets and merged the existing datasets together to make sure no tweets were missed by one of them. Then, I could select the timespan of interested namely November 3rd, 2020 until January 6th, 2021. Furthermore, this research is interested in Trump's twitter account @realDonaldTrump The decision to focus on his personal Twitter account instead of the official US President account (@POTUS) stems from how he uses both accounts. More information on this can be found in my thesis. 

### Data Collection Process
The data this thesis works with has been extracted from two sources. The first one is the Trump Twitter Archive. This is a website created in 2016 to record all Trump tweets. Since 2016, it has checked Twitter every sixty seconds and recorded new tweets. They also recorded all Tweets from pre-2016 for the completeness of the database. The data is freely usable and the creator’s aim is to “provide a public resource” [(Brown)](https://www.thetrumparchive.com/faq). The data could be extracted from the website in csv-format and includes the columns id, text, isRetweeted, isDeleted, device, favorites, retweets, date, and isFlagged. The second dataset was found on Kaggle, an online platform where users can share and download datasets. This dataset was uploaded by Kaggle user ‘CodeBreakder619’. Who is an analyst at Deloitte India. The dataset includes all “Day-by-Day Data on Donald Trump Tweets till 8th Jan 2021, before [the] blocking of his twitter account” [(CodeBreaker619)](https://www.kaggle.com/datasets/codebreaker619/donald-trump-tweets-dataset). They published the data under the license Data files © Original Authors. Trump is, of course, the creator of the actual content in the dataset and Twitter provided the extra information, concerning retweets, favorites, etc. He did not record how he created the dataset, however, after inspection of the dataset and the usability score of 10.00 on Kaggle, the dataset did meet the criteria for usage in this thesis. The dataset looked complete and included the columns of interest. The columns of this dataset are the same as the Trump Twitter Archive dataset. This means it includes the columns id, text, isRetweet, isDeleted, device, favorites, retweets, date, and isFlagged. To make sure my research includes all Trump’s tweets from the period of interest, I have decided to combine these datasets.

### Cleaning and Preprocessing
After combining the datasets, the duplicate tweet ids were dropped. Followed by renaming and removing columns where necessary. The data then needed cleaning for a better textual analysis. This involved merging and cleaning the data, organizing it efficiently, and preparing it for analysis in Voyant. For better readability, I decided to rename the columns ‘isRetweet’ and ‘isDeleted’ to ‘is_retweet’ and ‘is_deleted’. Furthermore, I changed the annotation for true and false from ‘t’ and ‘f’ to the full written out ‘True’ and ‘False’. Columns which were no longer of interest, such as ‘device’ and ‘isFlagged’ were then dropped from the dataset. As this thesis works with tweets, it was important to clean these for a better textual analysis. I used a cleaner function to delete the links, hashtags, mentions, emojis, as well as any other signs that could lead to noise in the data. The original tweet was kept and stored under ‘tweet’ whilst the cleaned data was stored under the column ‘text_clean’. If any rows returned empty, as they for example only contained a link in the original data, these were then dropped. As this thesis is interested in how Donald Trump constructed his rhetoric, any retweets he shared from his account were also dropped. Then it was time to filter to the timeframe of interest, namely tweets between the ‘2020-11-03’ and ‘2021-01-06’. After these steps, 814 rows of tweets were left. This thesis is interested in identifying metaphorically constructed disinformation and conpsiracy theory, and therefore works with keyword extraction in Python. To do this sucessfully, this thesis used Natural Language Processing (NLP). After loading in the NLP pipeline and defining a function that runs this pipeline on any given input text, the text could be lemmatized for easier keyword retrieval. All of these steps are documented in the `Nobebooks` in this GitHub repository.

### Column overview

**`1.merged_trump_tweets_clean.csv`**

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

keywords_metaphors: *"antifa", "ballot", "biden", "certify", "conspiracy", "dead", "digital", "dominion", "election", "enemy", "evidence", "fake", "flip", "fraud", "glitch", "hack", "harvest", "hoax", "illegal", "integrity", "justice", "landslide", "legal", "lie", "mail", "observe", "overturn", "poll", "power", "radical", "reject", "rig", "steal", "stop", "trump", "undermine", "verify", "vote", "win", "arizona", "georgia", "michigan", "pennsylvania", "wisconsin"*

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

**`4.all_candidate_metaphor_trump_tweets.csv`**
Filtered to the rows that include a candidate metaphor keyword. 

keywords_metaphors: *"abuse", "ascend", "attack", "battle", "betray", "bleed", "blockbuster", "chapter", "cesspool", "charge", "clean", "concede", "country", "coup", "crooked", "crush", "cure", "death", "defend", "destroy", "destruction", "destruct", "drench", "dump", "fail", "fight", "float", "flow", "flood", "game", "garbage", "goldmine", "harvesting", "hill", "hide", "hiding", "history", "home", "hustle", "inundate", "kill", "killer", "landslide", "lose", "magic", "media", "mountain" "pack", "play", "plague", "pour", "protect", "put", "puppet", "race", "rant", "rot", "route", "run", "save",  "shatter", "shielding", "sick", "silent", "sleepy", "soar", "spearhead", "speed", "steal", "stuff", "suit", "surrender", "swindle", "tank", "thin", "toss", "turtle", "undermine", "usa", "victory", "voice", "war", "waste", "witch"*
    
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

**`5.all_context_candidate_metaphor_trump_tweets.csv`**

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

**`6.all_metaphor_trump_tweets.csv`**

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

