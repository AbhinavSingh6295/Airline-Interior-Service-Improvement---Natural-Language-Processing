# Natural Language Processing Project

## Airline-Interior-Services-Hackathon

### Goal and Objective 
The goal of this project was to design new airplane interior services based on user reviews to improve the customer experience during the flight. 
The objective was to collect the data about the customer experience in airplanes and develop topic-modelling algorithm as well as sentiment analysis 
to extract key insights from the data.

### Methodology
- **Web-Scrapping** - Extracted the data from websites like Skytrax and Tripadvisor using BeatifulSoup/Selenium library of python. 
These libraries help in extracting data from HTML or XML files. We extracted around 3,000 reviews from Skytrax website and around 17,000 reviews from 
Tripadvisor (Seatguru), to create a corpus of 20,000 reivews for analysis. In addition to customer reviews and ratings, we extracted the Airline name 
and aircraft type for each review.

- **Text Pre-processing** - Reviews extracted from the websites required pre-processing before performing any analysis. For pre-processing, 
we cleaned (remove punctuations, numbers and lower case) the text using regular expression, after that removed the stopwords using the nltk corpus of 
english stopwords, and finally, using POS tagging, removed all the unnecessary words from reviews and kept only Noun, Verb, Adjective and Adverbs.

- **Topic Modelling** - 
  - **LDA** - Applied this most popular technique for topic analysis, but the top 10 words of topics were not giving clear pictures of the theme of the topic.
  - **BERTopic** - Applied this transformer based topic modelling. It has 3 steps - applied BERT Embedding to the documents, form the cluster using UMAP and 
  HDBSCAN, and applied c-TF IDF to identify topic within cluster. Results were really good, although lot of reviews went to 'outlier' category.
  
- **Sentiment Analysis** - Used transformer based Hugging face pre-trained model to assign the positive and negative sentiments to the sentences.

- **Insights** - For identifying the key area of concern for each airline, we identified the topics associated with most negative sentiments and 
highlighted them in our final presentation.

### Results
Major issues that we identified that were common with almost all the airlines were 'seat recline', 'overhead storage, 'engine noise' & 'toilet proximity'.

<img src="https://github.com/AbhinavSingh6295/Airline-Interior-Services-Hackathon/blob/main/Improvement%20Areas.PNG" />



