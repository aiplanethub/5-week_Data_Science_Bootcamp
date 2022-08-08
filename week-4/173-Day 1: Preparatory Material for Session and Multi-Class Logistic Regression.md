## Learning Objectives

* Multi-Logistic Classiﬁcation
* Why not Accuracy?
* Evaluating the Performance of Logistic Regression model
* Confusion Matrix

### What is Classiﬁcation?

Let’s learn with some examples:

* In **Classiﬁcation we** classify the outcome
* **Examples:**
  * Predict whether a transaction is fraud or not fraud
  * Predict whether to give loan or not
  * Predict whether to give college admission or not
  * Predict the grade (Grade A, B, C, D)
  * Note: Classiﬁcation can be more than two









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_9b51dd1847984040ab99f13fc680ff9c.png)






## What is Multi-Classiﬁcation?

**It is as simple as dividing waste into 4 categories - plastic, glass, metal, paper**







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_202090da123c47aa8d7baac47d33db7e.png)






### Understanding Multi-Class Logistic Regression










<iframe width="560" height="315" src="https://www.youtube.com/embed/J5bXOOmkopc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










## Evaluating the Performance of Logistic Regression model

* **Model Evaluation is a very important part in any analysis to answer the following questions:** _How well does the model ﬁt the data?, Which predictors are most important?, Are the predictions accurate?_
* **Guess what, evaluating a Classiﬁcation model is not as simple as Linear Regression.**
* But why?
* You must be wondering ‘Can’t we just use accuracy of the model as the holy grail metric?’

### Notebook

* Link to notebook: https://dphi.tech/notebooks/893/manish_kc_06/multiclass_logistic_regression

## Accuracy

* Classiﬁcation Accuracy is what we usually mean, when we use the term accuracy. It is the ratio of number of correct predictions to the total number of input samples.










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_2e29dbbaeec749008c0b97bcbb9c47a7.png)



### Why not Accuracy?

* Accuracy is very important, but it might not be the best metric all the time. Let’s look at why with an example -:
* Let’s say we are building a model which predicts if a transaction is fraudulent or not
* Let’s imagine, we build a basic model which always predicts that a transaction is not fraudulent. Guess what would be the accuracy of this model?
* **\~99% !!** (You may ask why? Well, less than 1% transactions are usually fraudulent and there is a huge class imbalance. So even if you ﬁt a wrong model that always predicts a transaction to be not fraudulent, the accuracy will remain 99% owing to class imbalance)
* Impressive, right? Well, the probability of a bank buying this model is absolute zero. ????
* In a problem where there is a large class imbalance, a model can predict the value of the majority class for all predictions and achieve a high classification accuracy.
* While our model has a stunning accuracy, this is an apt example where accuracy is definitely not the right metric.
* **Watch till 1 min 14 secs to understand why accuracy is bad metric for model performance**















<iframe width="560" height="315" src="https://www.youtube.com/embed/XeJZbCT84Js" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










**Is confusion matrix confusing or it resolves the confusion? You decide!**

## Confusion Matrix

A confusion matrix is a table that is often used to describe the performance of a classiﬁcation model (or "classiﬁer") on a set of test data for which the true values are known. The confusion matrix itself is relatively simple to understand, but the related terminology can be confusing.

Let's start with an example confusion matrix for a binary classiﬁer for disease prediction (though it can easily be extended to the case of more than two classes):



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_8bc63a71933f4821b7b5e62a27facf1d.png)




Let's now deﬁne the most basic terms, which are whole numbers (not rates):

* **true positives (TP):** These are cases in which we predicted yes (they have the disease), and they do have the disease.
* **true negatives (TN):** We predicted no, and they don't have the disease.
* **false positives (FP):** We predicted yes, but they don't actually have the disease. (Also known as a "Type I error.")
* **false negatives (FN):** We predicted no, but they actually do have the disease. (Also known as a "Type II error.")

I know these seem hard to memorise. One thing that has helped me remember these are by putting it in a better way:

**false positives = falsely classiﬁed as being positive.**

**This is a list of rates that are often computed from a confusion matrix for a binary classiﬁer:**

* **Precision:** Correctly predicted as positives compared to total predicted as positives  
Precision = **TP/(TP+FP)** = 100/110 = 0.91

* **Sensitivity/Recall:** Correctly predicted as positives compared to total number of positives  
Recall = **TP/(TP + FN)** = 100/(100+5) = 0.95

**Note: Mostly we have to pick one over other, it’s almost impossible to have both high Precision and Recall.**

* **Speciﬁcity:** Correctly predicted as negatives compared to total number of negatives **= TN/(TN + FP)** = 50/(50+10) = 0.83

### Understanding Precision and Recall

* Think about the search box on Amazon home page.








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_97cfa2427aea4c6f9e02f941a412c6e1.png)








* The precision is the proportion of relevant results( correctly predicted yes) in the list of all returned search results(total predicted yes).
* The recall is the ratio of the relevant results( correctly predicted yes) returned by the search engine to the total number of the relevant results that could have been returned (total actual yes).

## Choosing between Sensitivity and Speciﬁcity

* Often, the sensitivity and speciﬁcity of a test are inversely related. Selecting the optimal balance of sensitivity and speciﬁcity depends on the objective of the problem that needs to be solved.









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_786e79fa4d844178bb7527bee704f25f.png)






* If correctly identifying positive class is important for us, then we should choose a model with higher Sensitivity. However, if correctly identifying negative class is more important, then we should choose speciﬁcity as the measurement metric.

### Sensitivity or Speciﬁcity - an example

* Let’s say we are predicting if a patient has cancer or not. The default probability threshold is kept at 0.5 i.e&#x20;
  * Class 0 (No cancer) – Below 0.5&#x20;
  * Class 1 (Cancer) – Above 0.5









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_12409bc9f03f45cb866a22e564166855.png)



### Case 1: Higher Speciﬁcity

* Suppose we want to predict Class 1 (i.e patient has cancer) only if we are VERY conﬁdent. (To avoid giving the patient a shock and to avoid unnecessary treatment)
* We can instead change this threshold to 0.7. Thus, we’ll tell someone they have cancer only if we think they have greater than or equal to 70% chance of having a cancer.
* Look at the graph below. SInce the threshold has shifted to the right, so the number of people correctly guessed as having cancer have decreased. Thus, the speciﬁcity has increased. ( We are being very speciﬁc with declaring patients with cancer).









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_dcfcaf8497ed46cbb3f8e4e21b7ca2fa.png)







### Case 2: Higher Sensitivity

* Suppose we want to avoid missing too many cases of cancer ( avoid false negatives). If a person with cancer is told that he’s well, it can cause a delay in treatment and aﬀect the health badly).
* In this case we can set a lower threshold, say 0.25. Even if a patient has 25% chance of having cancer, we’ll inform him/her.
* Looking at the graph you can see that the threshold has shifted to the left. Most of the people with cancer will be detected in advance in this case. We have completely (or almost) eliminated False Negatives. It will thus result in higher Sensitivity/ Recall. (We are being sensitive in detecting a disease i.e a really sensitive test).








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_4820dabdbfd04f0f81e051fd4441145c.png)





You can watch this video from 00:58 to 5:32 explaining the Sensitivity and Specificity trade off












<iframe width="560" height="315" src="https://www.youtube.com/embed/yr73lr4W7Mc?start=58" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










### Confusion Matrix

* Talking about accuracy, our favourite metric!
* Accuracy is deﬁned as the ratio of correctly predicted examples by the total examples.



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_8bd0e3e92c6a4fb6947588ecb2df97b2.png)

* **Accuracy:** Overall, how often is the classiﬁer correct?  
**= (TP+TN)/total** = (100+50)/165 = 0.91
* Remember, accuracy is a **very useful metric when all the classes are equally important.**
* But this might not be the case if we are predicting if a patient has cancer. In this example, we can probably tolerate FPs but not FNs.
* If a cancerous patient is wrongly reported as being ﬁne, it can result in delaying of treatment. Which is not good!

### Slides Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1_3HAVN1BooheCPzn0K8VCGyOk61jxP88NH1_p5DS9OE/edit?usp=sharing).