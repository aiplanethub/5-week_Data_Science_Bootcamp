## Learning Objectives

* Data Splitting Recap
* Logistic Regression

### Quick recap of some keywords! Back to basics ;)

* **Features or Variables:** These are the most common terms we will come across from now on.
* **Features and Variables are the same in a dataset**; they are often interchangeably used. So there is no need to worry about it!





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_8866b8db74d9448fb28d65034d1e46a8.png)




* Remember the Standard Metropolitan Areas Data used previously? In that dataset, **we might be curious to predict "crime\_rate" in future**, so that becomes our target variable, and the rest of the variables become input variables for building a machine learning model.




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_c8dd95cce225485b9b822e2b8d4cf994.png)



### Train and Test Set






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_198938fd57a541c68f50b53655fba45b.png)








## Data Splitting

1. We **separate the data into input and target variable**
2. We further **divide them into train and test datasets**






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_e93c7cdb203346c3bc4c822f14f3ecbe.png)






* Let's consider the following data with 10 entries, and our objective is to predict whether someone has purchased a product or not, i.e., the "ProductPurchase" column = Yes or No




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_ae5277b4212f4c5e84bca7edc8c9e6c7.png)




Here, **Country, Age, and Salary are the Input variables** used to predict the **target variable - ProductPurchase**.

### Separate Input and Target Variables

* We separate the dataset into two new datasets, one with input variables - X (Country, Age, and Salary) and the other with the target variable - y (ProductPurchase).
* Adding a snippet from that we used in [our ﬁrst model building exercise](https://github.com/dphi-official/First\_ML\_Model/blob/master/ML\_with\_titanic\_data.ipynb).

![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_f58900f01f704dd388c2de31e5a3a0ee.png)

* We'll now split the x dataset into two sets — X\_train and X\_test.
* Similarly, we'll split the dataset y into two sets — y\_train and y\_test.


![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_8bd3c4ab38f742eab2d425124460345a.png)

* Reference here: https://dphi.tech/notebooks/858/manish\_kc\_06/day-1-notebooks-ml-with-titanic-dataset

## Logistic Regression!

* Thing to note! Never jump the gun!












![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_ef7f1dd96cd04d108f1b7bb2cfd6dbe6.png)









* We can take baby steps and learn things over time!








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1f23032af56b481a97bff0b6c86cb86a.png)







### What's next?

* We learned to build our ﬁrst machine learning and about the two other ML models (Linear and Logistic Regression). This means we are already in the game and know how to build models.
* Of course, there will be ifs and buts; we might be confused because of too many terminologies, models, etc. That is totally common!
* Now, let's take some baby steps to understand Logistic Regression. We learn the intuition behind the algorithm ﬁrst, and once we know it well, we ourselves would be curious to learn the maths behind it over time.

**Please note:** Getting overwhelmed with maths, coding, or tools shouldn't be a blocker to learning data science!

### What is Classification?

Let's learn with some examples:

* In **Classiﬁcation, we** classify the outcome
* **Examples:**
  * Predict whether a transaction is fraudulent or not
  * Predict whether to give a loan or not
  * Predict whether to give college admission or not
  * Predict the grade (Grade A, B, C, D)
  * Note: Classiﬁcation can be more than two








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1cce805aa67a41728efcc623cb737f9d.png)






### Logistic Regression

* Logistic Regression is one of the primary and popular algorithms for solving binary classification problems
* For each input, logistic regression outputs a probability that this input belongs to one of the two classes
  * Set a probability threshold boundary that determines which class the input belongs to
* Binary classification problems (2 classes):
  * Emails (Spam / Not Spam)
  * Credit Card Transactions (Fraudulent / Not Fraudulent)
  * Loan Default (Yes / No)
* Now, you may ask, why don't we use Linear Regression? Why do we need a new algorithm?
* Well, you will ﬁnd all the answers in the video below.
* The video below is a must-watch; the instructor has brilliantly explained logistic regression!

### **Must Watch:** Understanding Logistic Regression
















<iframe width="560" height="315" src="https://www.youtube.com/embed/zM4VZR0px8E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>











### Linear Regression vs Logistic

* Linear regression is used to solve regression problems with continuous values
* Logistic regression is used to solve classification problems with discrete categories
  * Binary classification (Classes 0 and 1)
  * Examples: Emails (Spam / Not Spam), Credit Card Transactions (Fraudulent / Not Fraudulent), Loan Default (Yes / No)
* Let's say a data scientist named John wants to predict whether a customer will buy insurance or not
* Remember that linear regression is used to predict a continuous value where the output (y) may vary between +∞ (positive infinity) to -∞ (negative infinity). In contrast, in this case, the target variable (y) takes only two discrete values, 0 (No insurance) and 1 (Yes, got the insurance).
* John decides to extend the concepts of linear regression to fulfill his requirement. One approach is to take the linear regression output and map it between 0 and 1. If the resultant output is below a certain threshold (say 0.5), classify it as No (didn't buy the insurance), whereas if the resulting output is above a certain threshold, classify it as bought the insurance (yes)
* We then plot a simple linear regression line and set the threshold as 0.5
  * Negative class (Insurance = No)– Age on the left side
  * Positive class (Insurance = Yes) – Age on the right side














![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_f2c0864e3ce04418b2e4f83b84223649.png)





**Imagine there is an outlier towards the right**





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_0373ee7e00e04ba7933946c6f976f057.png)




* As we can see, an outlier in the data will distort the whole linear regression line.
* Clearly, the line is unable to diﬀerentiate the classes with the linear line fit
* The line should have been at the vertical yellow line, which can divide the positive and negative classes, i.e., yes or no for insurance

**Well, life would be much simpler if we had an algorithm that would fit the points like below, right? It is a much better fit compared to the regression line!**







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_14f92535c46c4dab9a855e4180885625.png)





### Solution

* Solution – Transform linear regression to a logistic regression curve
* Logistic regression is a Sigmoid function
* Now, what does this sigmoid function do?
  * Sigmoid function takes in any real value and gives an output probability between 0 and 1








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_ea7cee4fca594e6abf99126153496744.png)







### What are we doing in Logistic Regression?

* We will use the real-valued output obtained from a linear regression model between 0 and 1 and classify a new example based on a threshold value. The function used to perform this mapping is the **sigmoid function**
* The Sigmoid Function is represented by the formula:




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_756f623aa7c640b28e5d1ac6be262fe4.png)



* There's no need to go into the depth of how we obtained this formula right now.

### Sigmoid Function (Logistic Function/ Logit)

* Take the linear regression function and put it into the Sigmoid function
* Sigmoid function outputs probability between 0 and 1







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_32449fe29f284ee9863b8cecc382bb7c.png)





* Sigmoid function outputs probability between 0 and 1 (y-axis)
* Default probability threshold is set at 0.5 typically&#x20;
  * Class 0 – Below 0.5
  * Class 1 – Above 0.5





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_79f1845e8b994253a9767895f349156e.png)




### Types of Logistic Regression

The logistic regression model can be classiﬁed into three groups based on the target variable categories:

* **Binary Logistic Regression**
  * The target variable has two possible categories.
  * Common examples : 0 or 1, yes or no, true or false, spam or no spam, pass or fail, Transactions (Fraudulent / Not Fraudulent), Medical Condition (Diseased/ Not diseased)
* **Multi-Class Logistic Regression**
  * **Multinomial Logistic Regression**
    * The target variable has three or more categories that are not in any particular order. So, there are three or more nominal categories.
    * Examples: Fruits (apple, mango, orange, and banana), profession (e.g., with ﬁve groups: surgeon, doctor, nurse, dentist, therapist)
* **Ordinal Logistic Regression**
  * The target variable has three or more ordinal categories. So, there is intrinsic order involved with the categories.
  * Student performance can be categorized as poor, average, good, and excellent.

We will be discussing Multi-Class Logistic Regression in the next module!

### Notebook on Logistic Regression

* https://dphi.tech/notebooks/891/manish\_kc\_06/logistic\_regression\_insurance

### Let's do some practice

**Instruction:**

* Use the raw data GitHub link: https://raw.githubusercontent.com/dphi-official/Datasets/master/HR_comma_sep.csv
* Or you can download it from [here](https://www.kaggle.com/giripujar/hr-analytics).

**Exercise:**

* Load libraries and data.
* Do some exploratory data analysis to ﬁgure out which variables have a direct and clear impact on employee retention (i.e., whether they leave the company or continue to work)
* Plot bar charts showing the impact of employee salaries on retention
* See the correlation between department and employee retention
* Separate dependent and independent variables.
* Split the data into train set and test set
* Now build a Logistic Regression model and make predictions for test data
* Measure the accuracy of the model