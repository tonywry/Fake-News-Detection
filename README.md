## Fake-News-Detection

This is a project of Text Analysis task on Fake News Detection on a Kaggle Dataset (https://www.kaggle.com/ksaivenketpatro/fake-news-detection-dataset), in which only 10223 records are given, and dataset contains only one short statement and the label.

This Project has been rewarded as the first-runner-up of the HKU Data Mining Hackathon Competition 2019.

### Methods used in this project
Code for Method 1/2 can be found in file - 
Code for Method 3 can be found in file - 
Code for Method 4 can be found in file - 

#### 1. Models based on TF / TF-IDF
        Extract the TF Matrix by normal tokenizing/stemmiing methods, building traditional ML/DL Models on the matrix, models include:
        - Naive Bayes
        - Random Forest
        - ANN
        - CNN
        - LSTM-RNN

#### 2. Models based on Word Embedding
        Feature Extraction by follwing Word Embedding methods
          - LDA
          - Word2vec
        
        Models built on word embedding:
          - Naive Bayes
          - Random Forest
          - SVM
          - Logistic Regression

#### 3. Data Extension by Google search
        1) Assume real news can be spread widely across internet/media, while Fake news not
        2) Applied Google API to search each statement and scraped down the title/url of google searching result (sample data in Folder "Google_Scraped"/"URL_Scraped"). 
        3) Extract feature from the scraped data by following assumtions
           (a) More records/valid links can be found for a true news (num_scrap)
           (b) Scraped titles would be similar to each other for a true news (score)
           (c) Scraped titles for a true news tend to share more common terms with original title (common_term)
           (d) True news usually comes from well-known websites, while fake news not (url_score)
           (e) Among the scraped titles, true news tends to have more similar scraped titles (similar_cnt)
           (f) While conducting “Exact match search”, true news tend to find more records (exact_match)
        4) Build Models by the features.
           (a) Logistic Regression
           (b) Random Forest
           (c) ANN

#### 4. Seperate Models across clusters
        1) Clustering by Word Embedding
        2) Models on each cluster







