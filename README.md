# Sentiment-Analyzer

With the 21st generation constantly generating petabytes of data every second on social media using various posts and comments it has become the need of the hour to analyze this big data. This project is a step towards that. I have built a sentiment analyzer using python which can analyze any sentiments of a post with 85% accuracy

In information retrieval or text mining, the TfidVectorizer (also called tf-idf), is a well know method to evaluate how important is a word in a document.In this Project we use tf-idf  to convert the textual representation of information into a Vector Space Model (VSM), or we can say a sparse matrix.It is an algebraic model representing textual information as a vector, the components of this vector could represent the importance of a term (tf–idf) or even the absence or presence  of it in a document.Text is represented as a vector of numbers instead of its original string textual representation.

Process of transforming data into numeric vectors

The first step is to select the data which needs to be modelled for training the analyser.
stop words that are present in almost all documents such as a,an,the,is etc,must be removed from training data.Since they occur in almost every sentence they won't be useful at all for extracting sentiment information from the text
Further Data Preprocessing is done using regex by removing special characters, digits from our documents.
We use term-frequency to represent each term in our vector space. We determine term-frequency which is nothing more than a measure of how many times the terms present in our vocabulary.We can specify many parametrs in Tf-Idf such as Max_df(maximum Document frequency),Lowercase(for converting all characters to lowercase),max_features(specifies No of terms used in building vocabulary).
 		5.we can define the term-frequency as a couting function:

			

ML models used:

I first used Decision Tree algorithm. I got an accuracy of 60% using GINI index which was pretty low. Next I tried using entropy in which case I obtained a accuracy of 70% which also seemed quite low. Then after some considerations i used Stochastic Gradient Descent Classifier from Scikit-Learn  and I obtained a good 85% accuracy. The main reason for this is that for training our data model is that our training data is very large hence it is  sparse, the classifiers in this module easily scale to problems with more than 10^5 training examples and more than 10^5 features.The estimator implements regularized linear models with stochastic gradient descent (SGD) learning: the gradient of the loss is estimated each sample at a time and the model is updated along the way with a decreasing strength schedule (aka learning rate). This results in a better accuracy as the data backpropogates to reduce error.

Testing our Data Model:

We use scikit-learn library and calculate accuracy precision recall and f1 results for the testing data which is the other 25000 reviews. This helps us in determing how good our model has trained for Sentimental Analysis. As mentioned previously the highest accuracy was noted using Stochastic Gradient Descent Classifier which is around  85%. I have also plotted the confusion matrix

Program:

The Program is written in Jupyter Notebook along with proper comments in it.

For any Doubts/Queries regarding the program feel free to comment down and ask it.

