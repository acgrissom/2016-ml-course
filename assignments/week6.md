Weekly Homework #6
==
Due Friday, October 7, at 11:55pm.

A (100 points). If the statement below is false, explain why it is false.  Otherwise, briefly explain why it is true.  You may find Section 3 of this document to be helpful.  https://www.cs.utah.edu/~piyush/teaching/aly05multiclass.pdf

1.  One-vs-all classification decides which label to predict by using the most confident classifiers to vote on the correct answer.

2.  Error correcting code classification constructs multiple binary classifiers for choosing a label.

3. All-vs-all classification selects the classifier with the highest confidence in the correct answer.

4. Standard support vector machines produce probabilities, just like logistic regression and the perceptron.

5. Logistic regression can be viewed as a special case of the perception.

B (100 points). Read the following paper:

https://aclweb.org/anthology/K/K16/K16-1010.pdf

1. What is the objective of this paper?

2. What kind of learning algorithm does this paper use for its computational results?

3. What is a "baseline," and how is it used in this paper?

4. What multi-class classification scheme does the paper use for 50 verbs?

5. What multi-class classification scheme does the paper use for the multiple choice scenario?  Describe how this works.

6. How does the computational performance on the multiple choice data compare with the human performance?

7. What are the feature set and hypothesis space, respectively?

8. In equation 1, what are the prior and the posterior, respectively, and what do they represent? 

9. Why does the paper suggest that the baseline model doesn't work well?

10. What does the paper mean when in Figure 3, when it describes the distribution as "Zipfian?"
  
Bonus (10 pts).  One-vs-all uses multiple binary classifiers and selects the one with the highest confidence.  This is in some sense unprincipled, since the trained models are not necessarily directly comparable.  This paper tracks the confidences of "the classifier" when analyzing of the result.  Does this make sense?  Argue your case.
