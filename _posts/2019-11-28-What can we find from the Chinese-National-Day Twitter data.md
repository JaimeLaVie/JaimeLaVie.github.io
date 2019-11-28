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

##### Aims
I decide to collect and analyze the data because I am interested in whether their is a significant difference in the expressed sentiments on Twitter towards China during such a grand occasion. Also, I want to observe the fluctuation of overall sentiments concerning time and languages.

##### Methods and experiments
To create training and test dataset, 1,000 tweets were randomly selected from each language and four students from different backgrounds were involved in the labeling. The technique used to analyze the general sentiment of the tweets at this stage is a mixed method of dictionary and SVM, which yields satisfactory results while avoid being too complicated. Currently, all the classifiers mentioned below are combinations of a trained SVM and positive-negative dictionaries.

Firstly, a relevance classifier would decide whether a tweet is relevant to the topic. For example, some tweets may be talking about the French National Day or the recent riots and chaos in Hong Kong and were mistakenly collected. These irrelevant tweets shall be excluded from the follow-up steps. Secondly, tweets written in Chinese would be categorized according to their typeface, say,simplified or traditional Chinese. Thirdly, another classifier would judge whether the tweet is simply stating a fact or is expressing certain kinds of affection. Those tweets with an affection would then be sent to the last classifier which determines the sentiment of the tweet. After training on the labeled data set and manually adjusting the dictionaries, all these classifiers have reached an average accuracy of over 90%, with several of them near 100%.

##### Results and Visualization
The analysis of the data is not yet completed, so this section only provides basic facts with graphs and makes no comments.
**Temporal analysis**
**Spatial Analysis**
**Keywords**
For English tweets with positive sentiments towards China, the most frequenly mentioned words are:
![deploy using travis](/assets/img/posts/nationaldaytweets/tweets_pos_en.png){:class="img-fluid"}
For English tweets with negative sentiments towards China, the most frequenly mentioned words are:
![deploy using travis](/assets/img/posts/nationaldaytweets/tweets_neg_en.png){:class="img-fluid"}
Deleting the words that are contained in both graphs, the results would become:
![deploy using travis](/assets/img/posts/nationaldaytweets/tweets_pos_delcom_en.png){:class="img-fluid"}
![deploy using travis](/assets/img/posts/nationaldaytweets/tweets_neg_delcom_en.png){:class="img-fluid"}

##### Future analysis
Analysis from the political aspect may focus on the causes of the phenomenon shown above. A country's relationship with China, its location (e.g. whether located along the Belt and Road), as well as the major laguage used within the country shall all be examined.