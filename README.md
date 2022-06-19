# Natural Language Processing

## Airline-Interior-Services-Hackathon

### Goal and Objective 
The goal of this project was to design new airplane interior services based on user reviews to improve the customer experience during the flight. 
The objective was to collect the data about the customer experience in airplanes and develop a topic-modelling algorithm as well as sentiment analysis 
to extract key insights from the data.

### Methodology
- **Web-Scrapping** - Extracted the data from websites like Skytrax and Tripadvisor using BeatifulSoup/Selenium library (to extract data from HTML or XML files) of python. 
We extracted around 3,000 reviews from the Skytrax website and around 17,000 reviews from 
Tripadvisor (Seatguru), to create a corpus of 20,000 reviews for analysis. In addition to customer reviews and ratings, we extracted the airline name 
and aircraft type for each review.

- **Text Pre-processing** - For pre-processing, we cleaned (remove punctuations, numbers, and lower case) the text using a regular expression, after that, we removed the stopwords using the NLTK corpus of English stopwords, and finally, using POS (Part of Speech) tagging, removed all the unnecessary words from reviews and kept only noun, verb, adjective and adverbs.

- **Topic Modelling** - 
  - **LDA** - This is one of the most popular technique for topic analysis, but the top 10 words of topics were not giving clear pictures about the theme of the topic.
  - **BERTopic** - Applied this transformer based topic modelling model provided by Hugging Face. It involves 3 steps - applies BERT-Embedding to the documents, forms the cluster using UMAP and HDBSCAN, and applies c-TF IDF to identify top words within a cluster. Results were really good, although lot of reviews went to 'outlier' category.
  
- **Sentiment Analysis** - Used transformer based pre-trained model from Hugging Face, to assign the positive, negative or neutral sentiment to the each sentence.

- **Insights** - For identifying the key area of concern for each airline, we identified the topics associated with most negative sentiments and 
highlighted them in our final presentation.

### Results
Major issues that we identified, that were common with almost all the airlines, were 'seat recline', 'overhead storage, 'engine noise' & 'toilet proximity'.

<img src="https://github.com/AbhinavSingh6295/Airline-Interior-Services-Hackathon/blob/main/Improvement%20Areas.PNG" />



