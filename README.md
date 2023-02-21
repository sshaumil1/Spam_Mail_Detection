# Spam_Mail_Detection

## Problem Statement
To build a NLP methodology to determine whether a mail is spam or ham.
## Data Gathering & Initial Preprocessing
First I read a csv file and store it in a data frame. Then, I took only relevant features for my further work. After that, I used the LangDetect library to find out the languages in which the reviews were written. After locating the reviews, I translated them with the help of googletrans library. Then I exported the translated reviews in a csv file for further use as translator takes high time for translation.
## EDA
First I checked whether the data is balanced or not by plotting a bar plot. In that way, I found that the data was highly imbalanced, which means I had to do balancing. Then, I checked Unigram, Bigram, Trigram. Following, I plot a wordcloud. Then, I extracted the most common keywords using the Yake Keyword Extractor.
## Preprocessing
I wrote functions to clean the data, including to remove spaces, to expand words, to handle accented characters, to remove stop words, to find root words, etc. Then I applied all the functions one by one on the data. I used different libraries for preprocessing, which were:
- **wordNetLemmatizer:** for finding root word
- **autocorrect library:** for autocorrection
- **unidecode:** for handling accented characters
- **contractions:** for expanding text
- **wordtokenizer:** for making tokens
Then I used replace function to change target variable categories in numerical data and drop the unwanted features.
#### Countvectorizer
First I splitted the data for training as well as testing so that I can avoid the data leakage. Then, I utilised countvectorizer to extract vectors of the documents.
#### Data Balancing 
As I had seen that data was imbalance. So, I used SMOTE to balance the data so that I can avoid duplicacy.
## Model Selection and Training
I used 3 models and check the accuracies and found the Multinomial Naive Bayes had good accuracy. That's why I used this model. After selecting this model, I optimised it by using crossvalidation (Randomised Search CV). Then, I trained the model with best parameters. Lastly, I got the accuracy of 92% on training data and 90% on testing data.  
## Model Testing
Next, I Tested the model whether it was working with the spam mail as well as ham mail. I observed that my model was predicting accurately. 
## Model Exportation for Production
Lastly, I exported both of the models tunned model and Countvectorizer model.  

# Thank You
