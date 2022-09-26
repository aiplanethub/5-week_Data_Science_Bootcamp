## Learning Objectives

* Input variables
* Target variable
* Train and Test data intuition
* Building an ML Model

In this module, we will give a quick recap that will help you solidify the concepts you have learned so far with some intuitive examples. This will be focused more on Model Building.

## Building a ML Model (Quick Recap)

### Data Science Modelling Process










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_b4fc783f5f0247f4802faf66ca3b907d.png)





**Credits:** https://towardsdatascience.com/data-science-modeling-process-fa6e8e45bf02

## Problem Solving steps

* Deﬁne Objective or understand the problem statement
* Data Requirements
* Data Collection/Preparation
* Exploratory Data Analysis
* Data Pre-processing
* Build a model
  * Understand whether it is a regression or classiﬁcation problem
* Evaluate
* Optimise
* Production
* Monitor
* You keep Optimising it every now and then







### Problem Statement

HR department wanted to seek the support of the analytics team to get possible salary predictions given they have information about employees' Career Seniority Levels and years of experience.

In other words, they need a machine learning model that would predict the possible salary that one should be provided if they feed information about their seniority level and years of experience.



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_9251cda1ba074f48b0e512cebb10658b.png)


### Data Preparation

* Given: we have to predict a person's salary based on years of experience.
* We have a dataset that looks like this:









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_16cfd9a411b845f3ae831878464ef2c9.png)







* What features do we have here?
* We have 3 features: Seniority\_Level, Years\_of\_Experience, and Salary.
* What will our target variable(value to be predicted) be in this case?
* Since Salary needs to be predicted, our model will take that to be the target variable and the rest (Seniority\_Level, Years\_of\_Experience) as input variables.
* In short, we’ll predict the target variable using input variables.







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_6b205862d6c64036ba6738a847b24f99.png)






### Separating input and target variable

* Now how do you actually separate the input and target variables?
* Since there’s only one target variable in the DataFrame, we can simply drop it and choose the rest of the variables. We do this using the drop( ) function by simply providing column name inside it.




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_33639263e90b41128d96dd13401ec367.png)




### Train and Test Data

* Another data splitting that we need to do is dividing the data into Train and Test Sets.
* Imagine drawing a horizontal line between the table, let’s say, after the 8th entry. That’s what Train Test Split looks like. The whole table is now divided into 4 parts.
* PLEASE NOTE: The dataset should always be shuﬄed before splitting. We’ve used an unshuﬄed version here just for explanation.








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_037ad102b2d74dc5a163d42ac53eaa6a.png)







* The upper part of the table becomes the Train Set which consists of X\_train (The input variables) and y\_train (The output variable).







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_a42d41e3dc2544c9b1871c88fbe0a9a5.png)







* The lower part of the table becomes the Test Set which consists of X\_test (The input variables) and y\_test (The output variable).




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_09241cc72c1f4299ad9af11dead9bd14.png)




* The sklearn’s function used for splitting the dataset is known as train\_test\_split

![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1bf724835e4846b68be333a4d6a71494.png)

* The 4 variables that we learned about in the previous slides are assigned values using the above piece of code. Let’s understand what the values inside the brackets mean:
  * **X** = Input variables
  * **y** = Target variable
  * **test\_size** = The ratio of the dataset that’ll be used in test set. If there are 100 rows, 70 rows will be used in train set and 30 in test set.
  * **random\_state** = It is provided just for the sake of obtaining the same result every time we run the code. It ensures that the rows in train and test set remain same each time.

### Model Building

Let’s build the simplest of all regression models using Linear Regression now.

* Import the model from sklearn
* Initialise and store the model in a variable (linear\_regressor in this case)
* Train the model on Train Data(X\_train and y\_train) using the ﬁt method.






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_d21de0c6393f4bc4a4cf714c12765575.png)



### Understanding the type of Problem

* For understanding the type of problem, we need to see the target variable we are dealing with.
* What kind of variable is Salary? Does it have classes? No, right?
* Salary is numerical and diﬀerent salaries are not divided into classes but are rather continuous values.
* The technique used for determining relationship between the input and target variables where the target variable is numerical (or continuous) is known as **Regression.**

### Model Evaluation

* Our model has been created! But how do we know if it works well? By testing it on the Test Data we created.
* Remember the test data is also split into 2 parts - X\_test and y\_test?
* We’ll ﬁrst put the X\_test(input variables) in our model and see what Salary predicts for those input values. The actual values of the salaries(y\_test) are not shown to the model.






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_17e30e945b124de18e2c3ea1215f9ef2.png)



* Let’s say our model predicts the following salaries:


![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_5c1e72a0d88c4d43b448f55abe364518.png)


* This prediction is done using the predict function of sklearn. Inside the predict function, we’ll provide X\_test to the model.

![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_c90b501d4f6444d9b65f4127419ab0a6.png)

* To know how good these predictions (y\_pred) are, we’ll have to compare them to the actual salary values (y\_test).

| ACTUAL VALUES | PREDICTED VALUES |
| --- | --- |
| ![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_7ac7adb4de8a423281b62c8e9c562bc4.png) | ![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_2a9da57cd9484275b263f881c0ac8041.png) |


* There are a lot of evaluation metrics for regression problems. Let’s use Root Mean Squared Error for this case.

### Root Mean Squared Error (RMSE)

* It is just the square root of the mean square error.
* It is preferred more in some cases because the errors are ﬁrst squared before averaging which poses a high penalty on large errors. This implies that **RMSE is useful when large errors are undesired.**



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1fbcbf5cc1744c839630b25548adc76d.png)




* For using RMSE, we’ll ﬁrst import metrics library from sklearn.
```
# import metrics library
from sklearn import metrics
```

* RMSE is not present as a function in sklearn. So we’ll just use the mean\_squared\_error function and take its square root . The main thing to note is what we provide inside the function - y\_test (actual value) and y\_pred(predictions made by our model).
```
# print results of RMSE
print(np.sqrt(metrics.mean_squared_error(y_test, y_pred)))
```




### Video Tutorial











<iframe width="560" height="315" src="https://www.youtube.com/embed/y_SdBb2_Hiw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










### Transformations on Train and Test

* Now let’s say we performed some feature selection techniques and found out that Seniority\_Level is not an important feature, the model can perform better when only Years\_of\_Experience is used.
* We’ll then transform our train data to a dataset with only Years\_of\_Experience as input variable to predict our target variable Salary.
* Now what about test data? Should we remove the Seniority\_Level feature from that as well?
* The answer is yes.
* The **Train and Test data must undergo the same data preparation steps**. Otherwise, the predictive model will not make sense. This means that the number of features for both the training and test set should be the same and represent the same thing.
* Similarly, **if normalization is required, then it should be done on both the train and test sets.**

### Slides Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1laaCx6cPS011ARjeY2OemtuyFtX37UlhKIIm_ciqWvg/edit?usp=sharing).