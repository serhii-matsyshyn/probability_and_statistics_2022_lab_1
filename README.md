# Probability and Statistics

# Lab Assignment 1: Naive Bayes Classifier

### Serhii Matsyshyn, Sofiia Yamkova, Mykola Yakovkin
### Team 3; 3 mod 5 = 3 the number of data set (3 - sentiment)

See Lab1_Naive_Bayes_Classifier_Templatee.Rmd for more details

## Conclusions
In this task we had to determine which class each sentence belonged to.  

To do that, we found the probability of each class (number of sentences in the specific class/number of all sentences in data).  
After that we found a probability of each word to appear and having those probabilities, we found the probability of each sentence.  
Now, we should find to which class our sentence belongs.  
Here we used product rule: we multiplied probability of class on probability of sentence.  
We will have 3 probabilities (cause we have 3 classes) and we should choose the largest one, and that will be class, to which our sentence belongs.  
  
To analyze the dataset, we created a bar plot with top 10 words and where they are repeated and the number of sentences in each class.  
We figured out, that train and test datasets are not split correctly (see information at the top of the notebook), therefore we had to split them again normally.  

Using a Naive Bayes classifier is not very efficient because it does not take word order into account.  
Therefore, the maximum accuracy of the model was 71 percent.  

F1 score shows that there is strong connection between sentiments and the amount of data from input dataset.
That is, the basic rule of creating datasets is violated at the provided dataset: the amount of training data of all classes should be approximately the same.
Otherwise, the model will be biased towards the class with the largest amount of data (in our case, it is neutral sentiment).

To improve the model, we can use a different classifier or use a different dataset.
