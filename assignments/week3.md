Week 3 Assignments (Work-in-progress)
--

*A.* Writing assignment:

Read the paper *Learning to Detect Malicious Executables in the Wild* (Kolter et al. 2004).  You can find it via Google Scholar, Microsoft Academic Search, or similar services.
Write a brief review of this paper according to the syllabus's guidelines.  There are two versions of this paper: a shorter conference version with double columns, and a longer journal version.
Read the conference version.

*B*.  Written Homework

1.  Regarding the paper assigned for part A, answer the following questions:
2.  
    (a) What is a relevant feature, and how did this paper determine which features are "relevant?"  Do you agree with this?  Why?

    (b) For a binary classification positive, a false positive (FP) is a negative instance incorrectly classified positively, 
    a true positive is a correctly classified positive instance, a false negative is an incorrectly classified negative instance, 
    and a true negative is a correctly classified negative instance.
    
    For example, if a patient has a disease and is tested for it (by a doctor or a classifier), the result of the test are as follows:
    * TP = correctly diagnosed as having the deases
    * FP = incorrectly diagnosed as having the disease
    * TN = correctly diagnosed as not having the disease
    * FN = incorrectly diagnosed as not havaing the disease.
    
    In many problem domains, we use two different metrics to give is a different sense of how well a model performs: precision and recall.
    Precision measures how likely a model's positive predictions are to be correct: 
    TP / (TP + FP) = # correctly classified true examples / # examples model classified as true .  If we have too many false positives
    and not enough true positives, this score decreases.  We can trivially maximize this by by never guessing true, i.e., always guessing -1.  (For simplicity, say that if the denominator is 0, the precision is 1.)
    
    (c) Give an example of a set of $n$-grams for a word that are used in this work.    
    
    This metric is contrasted with recall.  Recall measures how many true positives we manage to capture: 
    TP / (TP + FN) = # correctly classified true examples / # all true examples.  We can trivially maximize this value by always guessing +1.

   In the assigned paper, which is more important?  What would be an application where less than perfect precision or recall are unacceptable?  Justify your answer.
    
    (d)  What are the features used in this paper?
    
    (e) Describe at least two things about the paper that you did not understand.
    
    (f) Are you surprised by the results of this paper?  Why or why not?
   
