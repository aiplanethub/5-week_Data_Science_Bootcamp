## Learning Objectives

* Feature Importance & Selection
* Beneﬁts of Feature Selection
* Feature Selection Techniques

## Feature Importance and Feature Selection
**Feature Importance** refers to techniques that assign a score to input features based on how useful they are at predicting a target variable.

**Feature Selection** is the process where you automatically or manually select features which contribute most to your target variable.

In short, Feature Importance Scores are used for performing Feature Selection

Suppose we’re working on the Iris Classiﬁcation. We’ll ﬁrst create a baseline model using Logistic Regression. Now, we want to try out Feature Selection and try to improve our model’s performance. On plotting feature importance scores, we obtain the below graph:









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3cdde50c1f804d94856da9cd19505e61.png)








* Feature Importance Scores tell us that Petal width and height are the the top 2 features. The rest have a much lower importance score.
* We’ll select these 2 features.
* We’ll transform our existing dataset to contain only these 2 features.
* We’ll train our model on this transformed dataset.
* Finally, we’ll compare the evaluation metrics of our initial Logistic Regression model with this new model.

## Why Feature Selection ?

* You already know a number of optimization methods by now and might think what’s the need of reducing our data by feature selection if we can just optimize?
* There’s something known as “_The curse of dimensionality_”. In machine learning,  
“dimensionality” = number of features (i.e. input variables) in your dataset.
* When the number of features is very large relative to the number of observations(rows) in your dataset, certain algorithms struggle to train eﬀective models. This is called the Curse of Dimensionality.














![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_518bcbb29bb84204bde9eea4f6d8a1c4.png)








### Curse of dimensionality analogy

* Let's say you have a straight line 100 yards long and you dropped a penny somewhere on it. It wouldn't be too hard to ﬁnd. You walk along the line and it takes two minutes.
* Now let's say you have a square 100 yards on each side and you dropped a penny somewhere on it. It would be pretty hard, like searching across two football ﬁelds stuck together. It could take days.
* Now a cube 100 yards across. That's like searching a 30-story building the size of a football stadium. Ugh.
* The diﬃculty of searching through the space gets a lot harder as you have more dimensions.

### Benefits of performing Feature Selection

You might’ve gotten an idea of why feature selection is required by now.

Feature Selection helps us with the following:
* **Reduces Overﬁtting:** Less redundant data means less opportunity to make decisions based on noise(irrelevant data).
* **Improves Model Performance:** Less misleading data means our model’s performance improves.
* **Reduces Training Time:** Less data means that algorithms train faster.

### Types of Feature Selection Algorithms

* Filter Methods
  * Filter feature selection methods apply a statistical measure to assign a scoring to each feature. Eg: ANOVA, Chi-Square
* Wrapper Methods
  * Wrapper methods consider the selection of a set of features as a search problem, where diﬀerent combinations are prepared, evaluated and compared to other combinations. Eg: Recursive, Boruta
* Embedded/Intrinsic Methods
  * Embedded methods learn which features best contribute to the accuracy of the model while the model is being created. The most common type of embedded feature selection methods are regularization methods.\
    Eg: Tree Based Models, Elastic Net Regression

## Feature Selection Techniques

* Try and Google ‘Feature Selection Techniques’. You’ll ﬁnd that each article will talk about a diﬀerent set of techniques. The **number of Feature Selection Techniques** are so **extensive** that it is not possible to demonstrate all the techniques on one dataset.
* It is also important to note that **not all techniques will improve the performance of the model.** Sometimes, the main focus is to reduce the dimension even at the cost of some reduction in performance.
* Diﬀerent techniques work well on diﬀerent datasets. It is best to start with a simple technique, see if it improves accuracy and work your way up by trying our more techniques while comparing the improvement in accuracy.
* We’ll implement 4 techniques in the notebook and see how much improvement occurs by comparing each to a baseline model (basic model without any modiﬁcations).
  * Recursive Feature Elimination (RFE)
  * Feature Importance using Random Forest Classiﬁer
  * Boruta
  * XGBoost (this is a slightly advanced technique)

There are many more techniques but the above ones are popular and widely used in the industry.

### **Notebook link:**

* https://dphi.tech/notebooks/896/manish\_kc\_06/feature\_selection\_techniques

### Slides Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1ApRZzBM0JTgdM93iH__dwktzlHnT4qD_8zjdI9NYX2s/edit?usp=sharing).