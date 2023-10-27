# WeRateDogs Data Wrangling Report

## Introduction
This report provides a comprehensive overview of my data wrangling process for the WeRateDogs project. Data was collected from various sources, including the WeRateDogs Twitter archive, image prediction files, and Twitter API data.

## Data Gathering
### WeRateDogs Twitter Archive
I initiated the data collection process by importing the WeRateDogs Twitter archive from the 'twitter-archive-enhanced.csv' file. This dataset served as the foundation for my analysis.

### Image Predictions
The image prediction data was acquired programmatically, utilizing a provided URL, and was subsequently stored as 'image-predictions.tsv'. This data is instrumental in my project for making predictions based on the images associated with the tweets.

### Twitter API Data
To enrich my dataset, I queried Twitter's API using the Tweepy library. This allowed me to retrieve essential information, including retweet counts and favorite counts for each tweet. The data from the Twitter API served as a valuable addition to my analysis.

## Data Assessment
### Quality Issues
My assessment revealed several quality issues in the data, which I addressed methodically:

**Twitter Archive (wrd) Dataset:**
- Data type inconsistencies were identified in the 'timestamp' and 'retweeted_status_timestamp' columns and were rectified to datetime format.
- To ensure the dataset exclusively consisted of original tweets, retweets and replies were filtered out.
- Null objects were transformed into NaN in several columns to maintain data integrity.
- Corrected data types for columns like 'tweet_id', 'in_reply_to_status_id', 'in_reply_to_user_id', 'retweeted_status_id', and 'retweeted_status_user_id'.
- Managed invalid values in the 'rating_numerator' and 'rating_denominator' columns.
- Undertook measures to address non-standard dog names, such as 'a', 'an', and 'o'.
- Removed extraneous columns from the Twitter archive (wrd) dataset, streamlining it for more focused analysis.

**Image Dataset:**
- Transformed the 'tweet_id' column to the object data type for consistency.
- Improved the clarity of the dataset by assigning more descriptive column names.

### Tidiness Issues
My assessment also unveiled tidiness issues, which were resolved as follows:

- I harmonized the datasets by combining data from various sources.
- Simplified the dog stage information by creating a single column and subsequently dropping the superfluous ones.

## Data Cleaning
The data cleaning process involved a series of structured actions:

- Identified and replaced one-letter dog names with NaN to maintain data consistency.
- Converted the 'timestamp' column into a datetime data type for accurate date-time analysis.
- Merged dog stages into a single column while eliminating the now-redundant ones.
- Replaced 'None' values with NaN in the 'stage' and 'name' columns to enhance dataset integrity.
- Normalized 'rating_numerator' and 'rating_denominator' columns to ensure meaningful analysis.
- Filtered out retweets and replies, ensuring that the data exclusively comprised original tweets.
- Removed unnecessary columns in the Twitter archive (wrd) dataset to streamline it for subsequent analysis.
- Merged the datasets and removed surplus columns, ensuring that the dataset was ready for further analysis.
- Provided descriptive column names for clarity.
- Adjusted the data type of the 'tweet_id' column to string from int64 for consistency.

## Conclusion
The data wrangling process was an essential foundation for my analysis, facilitating data accuracy and completeness. The resulting dataset, 'twitter_archive_master.csv,' is prepared for in-depth analysis and visualization. These meticulous data wrangling efforts are a crucial precursor to obtaining accurate and meaningful insights in the next phases of my project.
