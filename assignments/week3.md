Week 3 Assignments 
--
Due Friday, September 9, 11:55pm.

*A.* Writing assignment:

Read this paper and write a review according to the syllabus's guidelines.   https://dl.packetstormsecurity.net/papers/IDS/hids/Learning-to-Detect-Malicious-Executables-in-the-Wild.pdf 

There are two versions of this paper: a shorter conference version with double columns, and a longer journal version.  Read the conference version provided.
You may find the following helpful for your review. http://www.cs.colostate.edu/~cs656/alan-meier.pdf

*B*.  Written Homework

1.  Regarding the paper assigned for part A, answer the following questions:

    (a) What is a relevant feature, and how did this paper determine which features are "relevant?"  Do you agree with this?  Why?

    (b) For a binary classification, a false positive (FP) is a negative instance incorrectly classified positively, 
    a true positive (TP) is a correctly classified positive instance, a false negative (FN) is an incorrectly classified negative instance, and a true negative (TN) is a correctly classified negative instance.
    
    For example, if a patient has a disease and is tested for it (by a doctor or a classifier), the result of the test are as follows:
    * TP = correctly diagnosed as having the deases
    * FP = incorrectly diagnosed as having the disease
    * TN = correctly diagnosed as not having the disease
    * FN = incorrectly diagnosed as not havaing the disease.
    
    In many problem domains, we use two different metrics to give is a different sense of how well a model performs: precision and recall.
    **Precision** measures how likely a model's positive predictions are to be correct: 
    TP / (TP + FP) = # correctly classified true examples / # examples model classified as true .  If we have too many false positives
    and not enough true positives, this score decreases.  We can trivially maximize this by by never guessing true, i.e., always guessing -1.  (For simplicity, say that if the denominator is 0, the precision is 1.)  Do TP and FP have meanings in a multiclass setting?
    
    (c) Give an example of a set of *n*-grams for a word that are used in this work.    
    
    This metric is contrasted with recall.  **Recall** measures how many true positives we manage to capture: 
    TP / (TP + FN) = # correctly classified true examples / # all true examples.  We can trivially maximize this value by always guessing +1.

   In the assigned paper, which is more important?  What would be an application where less than perfect precision or recall are unacceptable?  Justify your answer.
    
    (d)  Describe the feature space and label space for this problem.
    
    (e) Describe at least two things about the paper that you did not understand.
    
    (f) Are you surprised by the results of this paper?  Why or why not?
    
    (g) What is the IG function and its relationship to entropy?
    
    (h)  What is the prior in the IG function and how is it estimated?
    
    (i)  The arg max function in the Naïve Bayes formula returns C.  What is it?  What would the max function return, if it were used instead of arg max?
    
    (j) What reason do the authors give for the inconclusive results of boosted SVMs?
    
    (k)  In statistics, features are called "dependent variables." In data mining, features are often called "attributes." 
    (1) What criterion is typically used to create splitting nodes in the C4.5 algorithm mentioned in this paper?  (2) What is its relationship to KL-divergence?  And (3), what is this metric's relationship to entropy?
    
2.  What is the loss function of a Naïve Bayes classifier (in words or as a formula)?.  

3.  Does logistic regression have the same problem with 0's as Naïve Bayes, thus requiring smoothing (such as Laplace)?  Why or why not?
