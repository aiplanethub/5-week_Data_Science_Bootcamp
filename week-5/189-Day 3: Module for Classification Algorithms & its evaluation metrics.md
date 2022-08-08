## Learning Objectives

* Classiﬁcation Algorithms & Model Evaluation Metrics
* Which evaluation metrics to use when?


## Classiﬁcation Model Evaluation

Evaluation Metrics

1. Accuracy (Not in case of imbalanced classes)
2. Confusion Matrix
3. Precision
4. Recall/ Sensitivity
5. Speciﬁcity
6. F1 Score
7. AUC ROC


### Accuracy

* Classiﬁcation Accuracy is what we usually mean when we use the term accuracy. It is the ratio of the number of correct predictions to the total number of input samples.










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_2e29dbbaeec749008c0b97bcbb9c47a7.png)



### Why not Accuracy?

* Accuracy is very important, but it might not always be the best metric. Let's look at why with an example -:
* Let's say we are building a model which predicts if a transaction is fraudulent or not
* Let's imagine we build a basic model which always predicts that a transaction is not fraudulent. Guess what would be the accuracy of this model.
* **\~99% !!** (You may ask why. Less than 1% of transactions are usually fraudulent, and there is a huge class imbalance. So even if you ﬁt a wrong model that always predicts a transaction to be not fraudulent, the accuracy would remain 99% owing to class imbalance)
* Impressive, right? Well, the probability of a bank buying this model is absolute zero. ????
* In a problem with a significant class imbalance, a model can predict the value of the majority class for all predictions and achieve a high classification accuracy.
* While our model has a stunning accuracy, this is an apt example where accuracy is not the right metric.
* **Watch till 1 min 14 secs to understand why accuracy is a bad metric for model performance**















<iframe width="560" height="315" src="https://www.youtube.com/embed/XeJZbCT84Js" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










**Is the confusion matrix confusing, or does it resolve the confusion? You decide!**

## Confusion Matrix

A confusion matrix is a table often used to describe the performance of a classiﬁcation model (or "classiﬁer") on a set of test data for which the true values are known. The confusion matrix itself is relatively simple to understand, but the related terminology can be confusing.

Let's start with an example confusion matrix for a binary classiﬁer for disease prediction (though it can easily be extended to the case of more than two classes):



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_8bc63a71933f4821b7b5e62a27facf1d.png)




Let's now deﬁne the most basic terms, which are whole numbers (not rates):

* **true positives (TP):** These are cases in which we predicted yes (they have the disease), and they do have the disease.
* **true negatives (TN):** We predicted no, and they don't have the disease.
* **false positives (FP):** We predicted yes, but they don't have the disease. (Also known as a "Type I error.")
* **false negatives (FN):** We predicted no, but they have the disease. (Also known as a "Type II error.")

I know these seem hard to memorize. One thing that has helped me remember these are by putting it in a better way:

**false positives = falsely classiﬁed as being positive.**

**This is a list of rates that are often computed from a confusion matrix for a binary classiﬁer:**

* **Precision:** Correctly predicted as positives compared to total predicted as positives  
Precision = **TP/(TP+FP)** = 100/110 = 0.91

* **Sensitivity/Recall:** Correctly predicted as positives compared to the total number of positives  
Recall = **TP/(TP + FN)** = 100/(100+5) = 0.95

**Note: Mostly, we have to pick one over the other; it's almost impossible to have both high Precision and Recall.**

* **Speciﬁcity:** Correctly predicted as negatives compared to total number of negatives **= TN/(TN + FP)** = 50/(50+10) = 0.83

### Understanding Precision and Recall

* Think about the search box on the Amazon home page.








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_97cfa2427aea4c6f9e02f941a412c6e1.png)








* The precision is the proportion of relevant results( correctly predicted yes) in the list of all returned search results(total predicted yes).
* The recall is the ratio of the relevant results( correctly predicted yes) returned by the search engine to the total number of the relevant results that could have been returned (total actual yes).

## Choosing between Sensitivity and Speciﬁcity

* Often, the sensitivity and speciﬁcity of a test are inversely related. Selecting the optimal balance of sensitivity and speciﬁcity depends on the objective of the problem that needs to be solved.









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_786e79fa4d844178bb7527bee704f25f.png)






* If correctly identifying positive class is crucial, we should choose a model with higher Sensitivity. However, if correctly identifying negative class is more important, we should select speciﬁcity as the measurement metric.

### Sensitivity or Speciﬁcity - an example

* Let's say we are predicting if a patient has cancer or not. The default probability threshold is kept at 0.5, i.e.: 
  * Class 0 (No cancer) – Below 0.5&#x20;
  * Class 1 (Cancer) – Above 0.5









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_12409bc9f03f45cb866a22e564166855.png)



### Case 1: Higher Speciﬁcity

* Suppose we want to predict Class 1 (i.e., the patient has cancer) only if we are VERY conﬁdent. (To avoid giving the patient a shock and to prevent unnecessary treatment)
* We can instead change this threshold to 0.7. Thus, we'll tell someone they have cancer only if we think they have a greater than or equal to 70% chance of having cancer.
* Look at the graph below. Since the threshold has shifted to the right, the number of people correctly guessed as having cancer has decreased. Thus, the speciﬁcity has increased. ( We are being very speciﬁc with declaring patients with cancer).









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_dcfcaf8497ed46cbb3f8e4e21b7ca2fa.png)







### Case 2: Higher Sensitivity

* Suppose we want to avoid missing too many cases of cancer ( avoid false negatives). If a person with cancer is told that he's well, it can cause a delay in treatment and aﬀect his health badly).
* In this case, we can set a lower threshold, say, 0.25. Even if a patient has a 25% chance of having cancer, we'll inform them.
* Looking at the graph, you can see that the threshold has shifted to the left. Most people with cancer will be detected in advance in this case. We have completely (or almost) eliminated False Negatives. It will thus result in higher Sensitivity/ Recall. (We are sensitive in detecting the disease, i.e., it's a really sensitive test).








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_4820dabdbfd04f0f81e051fd4441145c.png)








You can watch this video from 00:58 to 5:32 explaining the Sensitivity and Specificity trade-off.









<iframe width="560" height="315" src="https://www.youtube.com/embed/yr73lr4W7Mc?start=58" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>










### Confusion Matrix

* Talking about accuracy, our favourite metric!
* Accuracy is deﬁned as the ratio of correctly predicted examples by the total examples.

![](https://lh5.googleusercontent.com/LGSb2pPVXrCTvJMSOwEzH1VIVtUvxldAZP2Ohf5E6DyHGTHkq-m9ipl4f2u4IbRkkFuIWv6dlt6saCNM6soMyjpUt3enakWm4MJ1uN4zxfuoFtrMGg3x-GVY\_\_bgrvBgctf9KKSXEBE)

* **Accuracy:** Overall, how often is the classiﬁer correct?  
**= (TP+TN)/total** = (100+50)/165 = 0.91
* Remember, accuracy is a **very useful metric when all the classes are equally important.**
* But this might not be the case if we are predicting if a patient has cancer. In this example, we can probably tolerate FPs but not FNs.
* If a cancerous patient is wrongly reported as being ﬁne, it can result in delaying of treatment. Which is not good!
* So you’ve already learnt how to calculate Precision and Recall and how changing the threshold can aﬀect their values. (SImilar to Sensitivity, Speciﬁcity threshold)
* But do we necessarily need to spend time on varying the threshold to get the perfect Precision and Recall? Or is there a way to choose this threshold automatically?
* Let’s take 3 algorithms and try to ﬁnd a metric for combining Precision and Recall.
* How about taking an average of Precision and Recall? (P+R)/2

|             | **Precision (P)** | **Recall (R)** | **Average** |
| ----------- | ----------------- | -------------- | ----------- |
| Algorithm 1 | 0.5               | 0.4            | 0.45        |
| Algorithm 2 | 0.7               | 0.1            | 0.4         |
| Algorithm 3 | 0.02              | 1.0            | 0.51        |

* Average tells us that Algorithm 3 is the best (highest value). Whereas Algorithm 3 is a dumb model that predicts y=1 each time and thus gives a recall of 1 (FN =0, TP=1).
* That means average isn’t a good metric.
* Researchers found a metric that solves our purpose: The F1 Score!











![harmonic_mean.gif](https://dphi-live.s3.amazonaws.com/media_uploads/harmonic_mean_f35c261b53f74f4e8ee64080e7b7ad1d.gif)









Let’s apply F1 Score to our problem:

|             | **Precision (P)** | **Recall (R)** | **Average** | **F1 Score** |
| ----------- | ----------------- | -------------- | ----------- | ------------ |
| Algorithm 1 | 0.5               | 0.4            | 0.45        | 0.444        |
| Algorithm 2 | 0.7               | 0.1            | 0.4         | 0.175        |
| Algorithm 3 | 0.02              | 1.0            | 0.51        | 0.0392       |

The F1 score tells us that Algorithm 1 is the best (highest F1 Score).

* **For F1 Score to be large, both P and R need to be large.**
* It’ll be highest(1) when both P and R are 1
* Accuracy can be used when the class distribution is similar while F1-score is a better metric when there are imbalanced classes.

### ROC (Receiver Operator Characteristic) Curve

* An ROC curve is a commonly used way to visualize the performance of a binary classiﬁer, meaning a classiﬁer with two possible output classes.
* It shows the performance of a classiﬁcation model at all threshold values.
* It plots 2 parameters:

1. True positive rate /Recall (TPR)  
![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_b2a9d4c7b256452687044a6c0620be6b.png)

1. False Positive rate (FPR)  
![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_ca084def263544e4afe6fe047b48cf8b.png)

### AUC Curve

* AUC stands for "**Area under the ROC Curve**." That is, AUC measures the entire two-dimensional area underneath the entire ROC curve







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_ad98a7aebbd84abfb93a459164dde690.png)








* AUC provides an aggregate measure of performance across all possible classiﬁcation thresholds.

### ROC and AUC Explained











<iframe width="560" height="315" src="https://www.youtube.com/embed/OAl6eAyP-yo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>









### Reading Material

MUST READ - An excellent article explaining Threshold, ROC and AUC in a simple manner:  
https://towardsdatascience.com/understanding-the-roc-and-auc-curves-a05b68550b69

## Which metrics to use when?

This is an important question and we get used to learning these measures over time. Sharing some resources with you all so that it helps you understand what metrics to be used in the context of solving a regression problem.

* 5 Classiﬁcation Metrics every data scientist must know:  
https://towardsdatascience.com/the-5-classification-evaluation-metrics-you-must-know-aa97784ff226
* https://medium.com/usf-msds/choosing-the-right-metric-for-evaluating-machine-learning-models-part-2-86d5649a5428

### Slides Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1JbZ8wM3xt5p2rk8nh1iFhscXmGFTSl-ZvNQ2smpCyl0/edit?usp=sharing).