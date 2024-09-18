Logistic Regression
Implementing Logistic Regression
In this exercise you must implement logistic regression and test it on text classification. We have provided starter code in the file logistic_regression.py. Here you should complete the following methods to implement a Logistic Regression Classifier.

logistic
predict
score
cost_grad
fit
where predict, score, cost_grad, fit are class methods of the classifier you must implement. The interface for each function is described in the file.

All needed equations can be found in the slides.

You can test your implementation by running python logistic_regression.py. This is a small non-exhaustive test. You should consider writing your own test cases.

Cost and gradient computations sometimes suffer from numerical issues if we are not careful. Exponentation of large numbers and log of small numbers can lead to numerical issues. It is possible to implement the algorithm to be more numerically stable if you do not compute numbers you do not need. The algorithm should work well enough even if you are not so careful and it is not a requirement for passing the hand-in to make the ultimate numerically stable algorithm.
Applying Logistic Regression
You will test your implementation on a real-life data set obtained from the danish central business register (CVR). The data set consists of text descriptions of the purpose of a company, such as:

"Selskabets formål er at drive restaurant og dertil knyttet virksomhed."

together with a label indicating the so-called industry code, e.g. 561010 is the code for "Restauranter" and 620100 is the code for "Computerprogrammering".

We have already written code that transforms a text description into a feature vector, so you do not need to worry about this translation. We will see later in the course how to do so. In this exercise, you will train a logistic regression classifier to classify descriptions of company purposes into the two classes "Restauranter" and "Computerprogrammering". If you want to have a look at the data, you can unzip "branchekoder_formal.gzip" and open it as a text file (keep the .gzip file in the directory). We are only extracting companies falling in the two categories 561010 and 620100.

Run python logistic_test.py and see your in-sample and test accuracy on text classification of industry codes (real data)

The code automatically saves the generated plot to include in your report. With a correct implementation and setting of learning rate, batch_size, epochs you should get above 95 percent test accuracy.
