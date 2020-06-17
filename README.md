# Spark
This project uses spark to conduct distributed calculation for large dataset, attempts to analyze the stack overflow posts. 
Using RDD, this project:

1, filters out the bad XMLs;

2, aggregates posts by the number of favorite counts, and finds the average score for each number of favorites;

3, for 99 users with the highest reputation, calculates these users answer percentage by calculating answers/(answers+questions), and 
the average answer percentage for all users;

4, finds number of days between account creation and first question for 100 users with the highest reputation;

5, identifies the veterans for users that has answered or asked a questions between 100 and 150 days after account creation; defines the
rest of the users brief users; presents the differences in average score, views, number of answers and number of favorites between these
two types of users; (Veterans have better stats for all measurements here)

Using PySpark DataFrame, this project:

1, applies word2vec as an vectorizer for text data, and finds the top 25 closest synonyms to 'ggplot2' and their similarity scores.

2, builds a machine learning pipeline, takes the body text as the features to predict whether a question contains one of the top ten most
common tags(finds out with MapReduce); removes stopwords, tokenize the texts, uses HashingTF as the transformer and logistic regression as
the estimator; uses cross validation to tune hyper parameters.
