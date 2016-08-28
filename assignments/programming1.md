Programming Assignment 1

Due Monday, September 12 at 11:55pm

Naïve Bayes Classification
--

Be advised that this assignment has multiple parts.  It is inadvisable to wait until the last few days to work on it.  If you're having trouble, use the message board and/or come to office hours.

* Download the Iris dataset.  (You can easily find this.)
* Include this in your submission, including any test/train/dev sets you used.
* Write a Naïve Bayes classifier to predict the class of the plant based on the other features.
 * There are continuous values in the feature set.  Figure out how to handle this and incorporate the strategy into your classifier.  Justify your decision in your report.
* To prevent underflow in probability calculations, the standard approach is to perform probability calculations in logspace. That is, instead of calculating *p<sub>1</sub>* * *p<sub>2</sub>*, we take advantage of the fact that log(*ab*) = log *a* + log *b* and calculate log *p<sub>1</sub>* + log *p<sub>2</sub>* instead.  See https://en.wikipedia.org/wiki/Log_probability 
* Convert the data to Vowpal Wabbit's format and run the same experiments with the loss function(s) of your choice, comparing the results.  
* Up to 10 point bonus: Add smoothing.
* Write a report according to the syllabus's guidelines.  Submit a zip (or tar.gz) file to Moodle with all of your materials.  
 
 Your report should *at least* address the following:
 * What is the accuracy on the training data?
 * If you split the data into a training and a test set that is representative of the training set, what is the performance?
 * Is it what you expected?  Why or why not?
 * How does your classifier compare to the one(s) you use in Vowpal Wabbit?  Why do you think this is?
 * How did you handle continuous values?
 * Potential bonus: What are the most informative features?


* If your classifier performs better/worse than expected, try to explain why.
* Your program should run "out-of-the-box."


Hints for reports:

*  Your report should have sections for the Introduction and Conclusion, and whatever you think is necessary in between. 
*  The report should be readable by someone who is not in the class.  I.e., the introductory sections should provide sufficient context for what you are doing and why.
*  Better analysis makes for a better paper.
*  Your report should be less than four pages.  Do not insert filler.  If you can say what you need to say in a page, then that is sufficient for this assignment.

Hints for Implementation:

You may implement the classifier however you wish, but you might find the following to be helpful:

* The Python csv module.
* The collections.defaultdict module.
 * You can make nested defaultdicts with the lambda operator.  For example:
```python
 my_2d_dict = defaultdict(lambda:defaultdict(float))  
 my_2d_dict[x][y] = 0.0
```

Hints for VW:
* You may find the VW validator helpful: http://hunch.net/~vw/validate.html
* If you do multiple passes, be sure to kill your cache with <code>--kill_cache</code> between runs.
  * Also delete your model file between runs.
* Vowpal Wabbit does not report accuracy, but you can output the guesses for each line with <code>--predictions ./predictions.txt</code> and write a short script to calculate this by comparing it to the test file.
* Use <code>--oaa *n*</code> for more than two classes during training, where *n* is the number of classes.
* VW classes (for more than two classes) must be integers (starting at 1).
* You will have to convert the string names to integers.
* Be sure to use <code>-t</code> during testing.  Otherwise, you will update the model while testing!
* Include the commands you used for your VW runs in a script called run.sh

