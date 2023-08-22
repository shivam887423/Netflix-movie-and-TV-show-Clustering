# Netflix Movies and TV Shows Clustering & Netflix Recommender System
![netflix-netflix-and-chill](https://github.com/shivam887423/Netflix-movie-and-TV-show-Clustering/assets/119883273/f3c1c3cd-a2d5-446a-8733-a0884dab3a20)

This repository contains the code and resources for analyzing the Netflix dataset of movies and TV shows until 2019. The dataset was sourced from the third-party search engine Flixable and includes information about various attributes of the content available on Netflix. The goal of this project is to uncover insights, trends, and patterns within the dataset and develop a content-based recommender system using natural language processing (NLP) techniques.

# Problem Statement
The problem at hand involves exploring the Netflix dataset to gain insights into the content available on the platform. The dataset provides information about movies and TV shows, their attributes, and their availability in different countries. By integrating this dataset with external sources such as IMDB ratings and Rotten Tomatoes, we can extract further valuable information.

The specific tasks to be performed in this project include:

Exploratory Data Analysis (EDA): Cleaned the data, unnested the Netflix content and tackled the null/missing values and conduct a thorough analysis of the dataset to uncover trends, patterns, and correlations among different attributes.
Understanding Content Availability: Determine the types of content available in different countries and identify any variations or preferences.
Analyzing Netflix's Focus: Investigate whether Netflix has been increasingly focusing on TV shows rather than movies in recent years.
Clustering Similar Content: Utilize text-based features to cluster similar content, enabling the development of a content-based recommender system.

# Data Summery

This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Fixable which is a third-party Netflix search engine. In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset. Integrating this dataset with other external datasets such as IMDB ratings, rotten tomatoes can also provide many interesting findings.

show_id : Unique ID for every Movie / Tv Show

type : Identifier - A Movie or TV Show

title : Title of the Movie / Tv Show

director : Director of the Movie

cast : Actors involved in the movie / show

country : Country where the movie / show was produced

date_added : Date it was added on Netflix

release_year : Actual Release Year of the movie / show

rating : TV Rating of the movie / show

duration : Total Duration - in minutes or number of seasons

listed_in : Genere

description: The Summary description

# Data Pipeline

Know Your Data: The first step in this project was to examine the various features of the dataset, understand the structure of the data and identify any patterns or trends. We looked at the shape of the data, the data types of each feature, and a statistical summary.

**Exploratory Data Analysis**: We conducted an exploratory analysis of the data to identify patterns and dependencies, and to draw conclusions that would be useful for further processing.

**Data Cleaning**: We checked for duplicated values in the dataset and then addressed any null values and outliers by imputing empty strings and dropping some of the null rows.

**Textual Data Preprocessing**: We used techniques such as stop word removal, punctuation removal, conversion to lowercase, stemming, tokenization, and word vectorization to prepare the textual data for clustering. We also used Principal Component Analysis (PCA) to handle the curse of dimensionality.

**Cluster Implementation**: We used K-Means and Agglomerative Hierarchical clustering algorithms to cluster the movies and determine the optimal number of clusters.

**Content-Based Recommendation System**: We built a content-based recommendation system using the similarity matrix obtained from cosine similarity, which will provide the user with 10 recommendations based on the type of movie/show they have watched.

# Project Structure

    ├── README.md
    ├── Dataset 
    ├── Problem Statement
    │
    ├── Understanding Data
    │
    ├── EDA
    │   ├── Numeric & Categoric features
    │   ├── Univariate Analysis
    │   ├── Bivariate Analysis
    │   ├── Multivariate Analysis
    ├──Data Cleaning
    │   ├── Duplicated values
    │   ├── NaN/Missing values
    │   ├── Treating Outlier 
    │
    ├── Textual Data Preprocessing
    │   ├── Clustering Attributes
    |   ├── Removing Stopwords
    |   ├── Lowercasing words
    |   ├── Removing Punctuation
    |   ├── Stemming
    │       ├── Snowball Stemmer
    |   ├── Word Vectorization
    |       ├── TF-IDF (Term Frequency - Inverse Document Frequency)
    |   ├── Dimenssionality Reduction
    |       ├── PCA (Principle Component Analysis)
    │
    ├── Model Building
    |   ├── Clustering Implemention
    |       ├── K-Means Clustering
    |           ├── Elbow Method
    |           ├── Silhoutte Score Analysis
    |       ├── Agglomerative Hierarchical Clustering
    |           ├── Dendogram
    ├── Content Based Recommendation System
    |
    │   
    ├── Report
    ├── Presentation
    ├── Result
    └── Reference

# Conclusion

In this project, we tackled a text clustering problem in which we had to categorize and group Netflix shows into specific clusters in such a way that shows in the same cluster are similar to one another and shows in different clusters are not.

- There were approximately 7787 records and 11 attributes in the dataset.
  
- We started by working on the missing values in the dataset and conducting exploratory data analysis (EDA).
  
- It was discovered that Netflix hosts more movies than television shows on its platform, and the total number of shows added to Netflix is expanding at an 
exponential rate. Additionally, most of the shows were made in the United States.

- The attributes were chosen as the basis for the clustering of the data: cast, country, genre, director, rating, and description The TFIDF vectorizer was 
used to tokenize, preprocess, and vectorize the values in these attributes.

- 10000 attributes in total were created by TFIDF vectorization.
- 
- The problem of dimensionality was dealt with through the use of Principal Component Analysis (PCA). Because 3000 components were able to account for more than 
80% of the variance, the total number of components was limited to 3000.
  
- Utilizing the K-Means Clustering algorithm, we first constructed clusters, and the optimal number of clusters was determined to be 6. The elbow method and 
Silhouette score analysis were used to get this.

- The Agglomerative clustering algorithm was then used to create clusters, and the optimal number of clusters was determined to be 7. This was obtained after 
visualizing the dendrogram.

- The similarity matrix generated by applying cosine similarity was used to construct a content-based recommender system. The user will receive ten 
recommendations from this recommender system based on the type of show they watched.

<a href="https://www.linkedin.com/in/shivam-pandey2//" rel="nofollow"><img src="https://camo.githubusercontent.com/a80d00f23720d0bc9f55481cfcd77ab79e141606829cf16ec43f8cacc7741e46/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c696e6b6564496e2d3030373742353f7374796c653d666f722d7468652d6261646765266c6f676f3d6c696e6b6564696e266c6f676f436f6c6f723d7768697465" alt="LinkedIn Badge" data-canonical-src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white" style="max-width: 100%;">
</a>
<a href="https://github.com/shivam887423/"><img src="https://camo.githubusercontent.com/fbc3df79ffe1a99e482b154b29262ecbb10d6ee4ed22faa82683aa653d72c4e1/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4769744875622d3130303030303f7374796c653d666f722d7468652d6261646765266c6f676f3d676974687562266c6f676f436f6c6f723d7768697465" alt="GitHub Badge" data-canonical-src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&amp;logo=github&amp;logoColor=white" style="max-width: 100%;"></a>
