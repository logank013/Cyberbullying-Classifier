# Cyberbullying-Classifier
## Data
**Dataset:** https://www.kaggle.com/datasets/andrewmvd/cyberbullying-classification  
This dataset comes from a Kaggle user and contains thousands of tweets categorized into 5 bullying categories as well as 1 non-bullying category. There is an even split among all 6 categories.

## Notebook
This notebook explores this dataset by creating a 6-way classifier. After multiple extra adjustments and additions to a base Naive Bayes classifier, I was able to successfully classify tweets into their 6 respective categories with a success rate of over 79%.

Initially, the base Naive Bayes classifier with Laplace smoothing created an accuracy score of around 49%. It became clear early on that other preprocessing was necessary to increase the accuracy of the classifier.

For the preprocessing step, I started with a couple of basic data cleaning steps by removing non-alphanumeric words and by making all characters lowercase. I then used NLTK (Natural Language Toolkit) to reduce words to their base form with lemmatization and remove stop words (common words in the language). This essentially reduces the number of unique words by removing unnecessary words and combining many similar words into their bases.

## Results
### Initial Classifier
![image](https://github.com/logank013/Cyberbullying-Classifier/assets/44517827/f26726f6-a5f8-4246-bd1b-392e8a9c79c9)

### After Preprocessing
![image](https://github.com/logank013/Cyberbullying-Classifier/assets/44517827/9c5e4fbf-a03a-423b-a306-d92f56d84b19)

All the extra steps of preprocessing proved to greatly improve the accuracy of the final classification. The classifier is not perfect, and the classifier struggles most with the broader categories of "not cyberbullying" and "other cyberbullying". I assume this is because the broader categories contain a larger variety of words. Overall, for a Naive Bayes classifier, I am impressed with the final result. Perhaps a more robust classification method could improve upon the 79.2% final result in the future.
