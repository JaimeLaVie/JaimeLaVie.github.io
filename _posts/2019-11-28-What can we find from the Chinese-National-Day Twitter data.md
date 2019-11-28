---
layout: post
title: What can we find from the Chinese-National-Day Twitter data
author: XU Yekai
date: '2019-11-28 10:16:58 +0800'
category: Social Media & Politics
summary: Using twitter data to analyze the public opinions of different countries towards China during the 2019 Chinese National Day.
thumbnail: map.png
---

Hi, there! This is my first academic blog. What I'm going to introduce is the twmporal and spatial analysis of over **270 thousand 2019-Chinese-Natioinal-Day-related** tweets written in **English and Chinese**. These data was collected using Twitter API from 30 September to 3 October. The data of 29 September as well as from 5 October to 8 October was also separately collected.

<br>

##### 1. Aims
I decide to collect and analyze the data because I am interested in whether their is a significant difference in the expressed sentiments on Twitter towards China during such a grand occasion. Also, I want to observe the fluctuation of overall sentiments concerning time and languages.

<br>

##### 2. Methods and experiments
To create training and test dataset, 1,000 tweets were randomly selected from each language and four students from different backgrounds were involved in the labeling. The technique used to analyze the general sentiment of the tweets at this stage is a mixed method of dictionary and SVM, which yields satisfactory results while avoid being too complicated. Currently, all the classifiers mentioned below are combinations of a trained SVM and positive-negative dictionaries.

Firstly, a relevance classifier would decide whether a tweet is relevant to the topic. For example, some tweets may be talking about the French National Day or the recent riots and chaos in Hong Kong and were mistakenly collected. These irrelevant tweets shall be excluded from the follow-up steps. Secondly, tweets written in Chinese would be categorized according to their typeface, say,simplified or traditional Chinese. Thirdly, another classifier would judge whether the tweet is simply stating a fact or is expressing certain kinds of affection. Those tweets with an affection would then be sent to the last classifier which determines the sentiment of the tweet. After training on the labeled data set and manually adjusting the dictionaries, all these classifiers have reached an average accuracy of over 90%, with several of them near 100%.

<br>

##### 3. Results and Visualization
The analysis of the data is not yet completed, so this section only provides basic facts with graphs and makes no comments.

**3.1 Temporal analysis**

Please aware that in this part, the data collected in Sept 29, Sept 30 - Oct 3, and Oct 5 - Oct 8 are **combined**.

**3.1.1** The number of English tweets concerning the Chinese National Day are shown below. The peak is around 18h, Oct 1:

![](/assets/img/posts/nationaldaytweets/Number_of_Tweets_by_Time_(English).jpg){:height="200px" width="800px"}

The number of Chinese tweets concerning the Chinese National Day are shown below. The peaks is include 22h Sept 30, 10h Oct 1, 20h Oct 1, 7h Oct 7, etc:

![](/assets/img/posts/nationaldaytweets/Number_of_Tweets_by_Time_(Chinese).jpg){:height="200px" width="800px"}

**3.1.2** The absolute sentiments towards China are calculated by subtracting the number of negative tweets from the number of positive tweets. And the result for English tweets are shown below. The lowest point is around 18h Oct 1:

![](/assets/img/posts/nationaldaytweets/Sentiment_of_Tweets_by_Time_(English).jpg){:height="200px" width="800px"}

The result for Chinese tweets are shown below. The peaks are 1h, 4h, 10h, and 20h Oct 1:

![](/assets/img/posts/nationaldaytweets/Sentiment_of_Tweets_by_Time_(Chinese).jpg){:height="200px" width="800px"}

**3.1.3** The normalized positive sentiments are obtained by dividing the number of positive tweets within a time period by the number of all the tweets collected within this time period. The normalized negative sentiments can be calculated in the same way. And the normalized sentiments is the difference between the normalized positive sentiments and the normalized negative sentiments. The result for English tweets are: (The blue, green, and red lines are the normalized positive sentiments, the normalized negative sentiments, and the normalized overall sentiments, respectively)

![](/assets/img/posts/nationaldaytweets/Normalized Sentiment of Tweets by Time (English).jpg){:height="200px" width="800px"}

The result for Chinese tweets are:

![](/assets/img/posts/nationaldaytweets/Normalized Sentiment of Tweets by Time (Chinese).jpg){:height="200px" width="800px"}

**3.2 Spatial Analysis**

[打开链接]</assets/img/posts/nationaldaytweets/map_pos_en.html>

**3.3 Keywords**

**3.3.1** For English tweets with positive sentiments towards China, the most frequenly mentioned words are shown bottom left, and the negtive bottom right:

![](/assets/img/posts/nationaldaytweets/tweets_pos_en.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_en.png){:height="350px" width="350px"}

Deleting the words that are contained in both graphs, the results would become:

![](/assets/img/posts/nationaldaytweets/tweets_pos_delcom_en.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_delcom_en.png){:height="350px" width="350px"}


**3.3.2** For Chinese (including both simplified and traditional Chinese) tweets with positive sentiments towards China, the most frequenly mentioned words are shown bottom left, and the negtive bottom right:

![](/assets/img/posts/nationaldaytweets/tweets_pos_zh.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_zh.png){:height="350px" width="350px"}

Deleting the words that are contained in both graphs, the results would become:

![](/assets/img/posts/nationaldaytweets/tweets_pos_delcom_zh.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_delcom_zh.png){:height="350px" width="350px"}


**3.3.3** For simplified Chinese tweets with positive sentiments towards China, the most frequenly mentioned words are shown bottom left, and the negtive bottom right:

![](/assets/img/posts/nationaldaytweets/tweets_pos_zhs.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_zhs.png){:height="350px" width="350px"}

Deleting the words that are contained in both graphs, the results would become:

![](/assets/img/posts/nationaldaytweets/tweets_pos_delcom_zhs.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_delcom_zhs.png){:height="350px" width="350px"}


**3.3.4** For traditional Chinese tweets with positive sentiments towards China, the most frequenly mentioned words are shown bottom left, and the negtive bottom right:

![](/assets/img/posts/nationaldaytweets/tweets_pos_zht.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_zht.png){:height="350px" width="350px"}

Deleting the words that are contained in both graphs, the results would become:

![](/assets/img/posts/nationaldaytweets/tweets_pos_delcom_zht.png){:height="350px" width="350px"} ![](/assets/img/posts/nationaldaytweets/tweets_neg_delcom_zht.png){:height="350px" width="350px"}

<br>

##### 4. Future analysis
Analysis from the political aspect may focus on the causes of the phenomenon shown above. A country's relationship with China, its location (e.g. whether located along the Belt and Road), as well as the major laguage used within the country shall all be examined.