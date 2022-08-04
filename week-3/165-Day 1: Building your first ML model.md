## Machine Learning Classiﬁcation Vs. Regression






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_0d2959fff7144ee78170c5072358f022.png)







## Data Science Modeling Process







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_ebd5bd4ac4b14d61a05c615a12340ad5.png)






### Problem Solving

* Deﬁne Objective or understand the problem statement
* Data Requirements
* Data Collection
* Exploratory Data Analysis
* Data Pre-processing
* Build a model
  * Understand whether it is a regression or classiﬁcation problem
* Evaluate
* Optimise
* Production
* Monitor
* You keep Optimising it every now and then

### Objective/Problem Statement

* The goal of the model is to **predict whether a passenger survived or not in the Titanic disaster**, given their age, class and a few other features.








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3affea93b5c04929b183dfa0ea125f11.png)






### Data

* We have the data!

### Understanding the Data

* PassengerId - this is a just a generated Id
* Pclass - which class did the passenger ride - ﬁrst, second or third
* Name - self explanatory
* Sex - male or female
* Age
* SibSp - were the passenger's spouse or siblings with them on the ship
* Parch - were the passenger's parents or children with them on the ship
* Ticket - ticket number
* Fare - ticket price
* Cabin
* Embarked - port of embarkation
* Survived - did the passenger survive the sinking of the Titanic?

### Explore the data

* Let’s get to the notebook:  
https://github.com/dphi-official/Data_Science_Bootcamp/tree/master/Week3

### Omitting Irrelevant Variables/Columns

* You shouldn’t drop columns or variables just like that! Unless there is a strong premise.
* Id, port, cabin and name

### Split the data into train and test







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_4997cda76f45432fb1f5e7ec5160c2d8.png)








### Model Building - Decision Tree

* Now what is this decision tree?
* Well, we all might have seen it by now!
* Decision Tree Examples








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1aebc92a755e49bf9b902d60f9b5814c.png)











![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_8d58873618714692b784e9a8752993d4.png)








### Now what next?







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_897e00eab415432bb8464c095ddd90c5.png)






Let’s do it!

### Model Evaluation

* **Evaluate on test dataset to check the performance!**
* Well, we build a model on historical data and expose them to new data that we would see in future. Technically they will be exposed to unseen data

### Overﬁtting - Underﬁtting






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_051dbea42dbb4774b01c22f764138d6b.png)










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_9e9683b5f735495d81ea0c59e8e0793c.png)






### Model Evaluation

We are not done yet, We can improve it signiﬁcantly.

How? It will follow in due course!

### What else can be done in general?

* Feature Selection
* Cross validation
* Applying diﬀerent ML Models
* Hyper parameter tuning etc

And as data scientist we must keep optimising and building better models that derives meaningful results.