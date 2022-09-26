## Learning Objectives

* Decision Trees

## Understanding Decision Trees

* The following video clearly explains a decision tree and how it works with many live examples.
* Alongside, it will talk about mathematical aspects such as Gini impurity. It would be good to understand them in the long run, though you may not want to overwhelm yourself with too much jargon at the moment.










<iframe width="560" height="315" src="https://www.youtube.com/embed/7VeUPuFGJHk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










* A simple non-technical explanation of the decision tree:  
https://towardsdatascience.com/a-beginners-guide-to-decision-tree-classification-6d3209353ea
* A comprehensive article on decision trees that talks about optimization criteria, pros and cons, etc.:  
https://www.datacamp.com/community/tutorials/decision-tree-classification-python

### Let’s do some practice

* Now we know how to build a simple decision tree model on one of the datasets that we used previously.
* **Objective:** Imagine you were hired as a Data Scientist/Analyst by the Central Police Oﬃce of Metropolitan areas, and your job is now to create a predictive model for crime_rate. For now, let’s focus on building a simple decision tree.
* **Link to the Dataset:**  
https://docs.google.com/spreadsheets/d/1rruRHMCALDpWSSzKIHTl9Yello4y-xsWaIL1V8b9dwU/edit?usp=sharing
* Download the dataset as a CSV file.

### Hints

* This is a regression problem as the outcome variable is continuous. Hence, you need to use a Regressor instead of a classifier in the below lines of code. A reference example of the regressor problem can be found [here](https://www.kaggle.com/dansbecker/your-first-machine-learning-model).
* from sklearn.tree import DecisionTree**Classifier**  
model = DecisionTree**Classifier**()  
model.fit(X\_train, y\_train)

### What next?

* If you were able to build a model, then don’t forget to share it [here](https://dphi.tech/notebooks/all-notebooks/) with fellow learners!
* **You surely deserve praise for your first Machine Learning Model!**