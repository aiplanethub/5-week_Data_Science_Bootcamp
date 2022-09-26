## Learning Objectives

* Statistics Refresher
* Cost Function
* Gradient Descent

## Statistics Refresher

* **Mean:** The mean is the [average ](https://www.statisticshowto.com/arithmetic-mean/)of a data set. For example, take a list of numbers: 10, 20, 40, 10, 70  
  Mean = (10 + 20 + 40 + 10 + 70) / 5 = 30

* **Median:** The median is the middle of the set of numbers. To ﬁnd the median, ﬁrst we sort the list of numbers: 10, 10, 20, 40, 70  
  The exact middle number, i.e., 20, is the median.

* **Mode:** The mode is the most common number in a data set.  
  In the above list of numbers, 10 has occurred two times while the other three numbers occurred one time each. So, the mode is 10 here.

* **Range:** The diﬀerence between the highest and lowest values in the data set.  
  For a given list of numbers: 10, 20, 40, 10, 70 the range is 70 - 10 = 60.

* **Variance:** The average of the squared diﬀerences from the mean. Steps to calculate variance:
  * Calculate mean (mean is nothing but average)
  * Find the diﬀerence of each data from mean
  * Square all the diﬀerences
  * Take the average of the squares.

* **Standard Deviation:** It shows you how much your data is spread around the mean. Its symbol is $\sigma$ (the greek letter sigma). **It is the square root of the variance.** Therefore, the variance is often represented as $\sigma^2$.




### Normal Distribution












<iframe width="560" height="315" src="https://www.youtube.com/embed/iMak-EW4HtM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


















<iframe width="560" height="315" src="https://www.youtube.com/embed/1EGtm3ClkIc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










### Unimodal and Multimodal Distribution









<iframe width="560" height="315" src="https://www.youtube.com/embed/7kw9dlAJmA8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>











### Coming back to Linear Regression

**This will be in continuation of our yesterday's topic!**

## Cost Function

**What?**

Now that we built a model, we need to measure its performance, right? and understand if it works well or not. The cost function measures the performance of a Machine Learning model for given data. It quantiﬁes the error between predicted and expected values and presents it as a single real number.

Depending on the problem, the Cost Function can be formed in many diﬀerent ways. The purpose of Cost Function is to be either:

* **Minimized** - the returned value is usually called **cost, loss, or error.** The goal is to ﬁnd the values of model parameters for which Cost Function returns as small a number as possible.
* **Maximized** - the value it yields is named a **reward**. The goal is to ﬁnd values of model parameters for which returned number is as large as possible.
* **Predicted value:** As the name says is the predicted value of your machine learning model.
* **Expected value:** Is the actual value(or the label present in your data)

Often machine learning models are not 100% accurate or perfect; they tend to deviate from the actual or expected value.

**Explaining with an example:** If we are predicting a person's age based on a few input variables or features.

* Our machine learning model predicted the age as 28 years
* However, the actual age of the person is 29 years.
* Here **28 years is the predicted value** and **29 years is the expected or true value.** As data scientists, we try to minimize errors while building models.







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_24ea2598d52347bf9acd4db9bfe8ba74.png)



The diﬀerence between the actual value and the model's predicted value is called **residual.**

### Cost Function Types/Evaluation Metrics

There are three primary metrics used to evaluate linear models (to ﬁnd how well a model is performing):

1. Mean Squared Error:
2. Root Mean Squared Error
3. Mean Absolute Error

* MSE is simply the average of the squared diﬀerence between the true target value and the value predicted by the regression model.
* As it squares the diﬀerences, it **penalizes** (gives some penalty or weight for deviating from the objective) **even a tiny error** which leads to **over-estimation of how bad the model is.**





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_7e01f4a79ea9468d96bef76d91df8ed2.png)




### Root Mean Squared Error (RMSE)

* It is just the square root of the mean square error.
* It is preferred in some cases because the errors are ﬁrst squared before averaging, which poses a high penalty on large errors. This implies that **RMSE is useful when large errors are undesired.**





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3726dfced8a848158386f99dfba5789c.png)





### Mean Absolute Error(MAE)

* MAE is the absolute diﬀerence between the target value and the value predicted by the model.
* MAE **does not penalize the errors as eﬀectively as MSE**, making it unsuitable for use-cases where you want to pay more attention to the outliers.







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_9e50f0a25bf84a0bbd5f5690546c3d57.png)





### Gradient Descent

* As Data Scientists, we always want to optimize our algorithms and go for the best ones. Gradient Descent is one of those optimizers that help us do this!
* Gradient Descent is an optimization technique that minimizes the cost function in the machine learning process. Every machine learning algorithm has a cost function.
* For now, we are not getting too much into how it works. We will learn about it as we proceed. Below is the link to a video for further understanding: [https://www.youtube.com/watch?v=vsWrXfO3wWw](https://www.youtube.com/watch?v=vsWrXfO3wWw)&#x20;

### Recap

* Linear regression is used to predict a value (like the sale price of a house).
* Given a set of data, ﬁrst try to ﬁt a line to it.
* The cost function tells you how good your line is.
* You can use gradient descent to ﬁnd the best line.

### Optional Reading Material

If you are interested to learn more about gradient descent, refer to the below video:

* https://www.youtube.com/watch?v=sDv4f4s2SB8