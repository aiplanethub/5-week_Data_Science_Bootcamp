## Data Analysis - An Analogy

### Let's understand Data Analysis with an example

Imagine you own an apple farm and want to know the number of apples you grow, but you are too busy with the farm, so you hire someone to count them. You sell your apples too, and you get your apple counter to keep a record of the number of apples you have at the beginning and the end of the day.&#x20;

Many days and months pass, and you put sheet after sheet of the apple count together, and you discover patterns and trends in the purchasing behavior of your customers.

The trends and patterns help you realize that your output of apples is the same during the colder season, but people buy less than during the summer.&#x20;

You then set out to dig deeper into this trend and find ways to keep the sales of apples consistent throughout the year, beating your competitors at the game and becoming an apple farm tycoon.

**Apples are your data; tracking them is essential, and analysis is key.**

For starters, you will know if your supply of apples matches the market's demand and the consistency of the ratio of demand to supply throughout the year. Pegging the price to each apple and drawing the cost down gives you your profit.&#x20;

You will find trends and patterns in your production when you have enough data. These trends can help you understand your organization better, help you reduce inefficiency and therefore reduce costs.

### What is Data Analysis?

As an apple farmer, you counted the apples at the beginning and end of each day in an organized fashion. In the end, you got some insightful information (i.e., trends and patterns in the sale of apples)  from that data. This is called Data Analysis.

So collecting all the words above, **Data Analysis is a method of collecting and organizing the data and, if required, manipulating the data so that one can derive some useful information from the data.**

### Data Analysis and Pandas

Pandas is a tool in Python that helps you collect (or read) the data from a file, organize it in a tabular format, and manipulate and clean the data to derive insightful information from it.

## Introduction to Pandas

### What is Pandas?

* Officially stands for **Python Data Analysis Library**
* It is an open-source Python library
* It is a tool used by data scientists to:
  * read,
  * write,
  * manipulate, and&#x20;
  * analyze the data.

### Why Pandas?

* It helps you explore and manipulate data in an efficient manner
* It helps you analyze large volumes of data with ease. When we say large volumes, it is in millions of rows/records.

### Why is Pandas so Popular?

* Easy to read and learn
* Extremely fast and powerful
* Integrates well with other visualization libraries

### Importing Pandas

Anytime you want to use a library in Python, your first priority should be to make it accessible.

You can import/load Pandas in your notebook or any other Python IDE in two different ways.

* **import pandas**
* **import pandas as pd**

Just as we use the 'np' shorthand for NumPy, we will use the 'pd' shorthand for Pandas. It simply serves as an alias, and it is easier to use 'pd' instead of writing full form 'pandas' while coding.

In this course, we will use:

`import pandas as pd`

## Series

### Pandas Objects

Before we dive into Series, let's do a quick recap of pandas objects. At the core of the pandas library, there are two fundamental data structures/objects:

* Series
* Data Frames

### What is a Series?

* A one-dimensional labeled array
* Can hold data of any type
* Is like a column in a table

### What can a Series have?

* A Series can have all the elements as numbers in it:






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_d0cedac8c4d14c8c9655af50c4da5baa.png)






* A Series can have all the elements as strings in it:



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_fdc09c325d12430db04f51d5184055eb.png)



* A Series can have its elements as both numbers and strings. 
* But the data type of the Series is always 'object' in this case:




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_c009b262e19442bcba27b0443b9df483.png)




* Series is like a list in Python that can take any value like integers, strings, floats (or decimal values), etc.
* All the items in the Series are labeled with indexes:




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_93dd761ed388443fbf91ccb17b94fecb.png)




* **By default, indexing starts from 0 in Series.** 

### **Human vs. Python Index**

* Indexes that we (humans) understand:


![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_7f29921bb6fe4d89805e73bde9c929ba.png)


* Indexes that Python understands:



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1e0299f3ee16440597df44913e70aba8.png)



**Well, it all starts with '0'. That's the only difference.**

### Create a Series

* Remember to import the library before using it!

  **`import pandas as pd`**

* You can create your own Series using a Python list:





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_b065378a1c3b4c20990cb7a4fc825d2b.png)





* You can also create your own Series using a dictionary:

![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_937099e6513a4788ae90cbaf8c6bb80d.png)

## DataFrame

### What is a DataFrame?

* Two-dimensional table
* Made up of a collection of Series
* Structured with labeled axes (rows and columns)

A data frame looks like a table, as shown in the image here:










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_ebaddd603f8d4917abf0f77bbc358eeb.png)










### Create a DataFrame

* You can create a DataFrame using a Python list or a NumPy array:








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_7365e26062974270be514dc0d7a0963f.png)







* Exercise: Try creating a DataFrame using a NumPy array.
* **Don't like python default index starting from '0'?** Well, you can give your own column and row indexes:






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_cbcd08ba73904b2d882dea2d06283a31.png)





* **You can create a DataFrame using dictionary:**







![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1064cc0cabc74eb985e5d95c7be8c6a0.png)







### A Column is a Series

* A DataFrame is a collection of Series.
* A series is a column in a table or a DataFrame.





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_c26c3dfa04f1419d83d73bbb22a8a446.png)







* There are three series in the given DataFrame - 'Regd. No', 'Names' and 'Marks%'.

### Slide Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1quSvfkJBQfk6-p4DZD_nUqYupgRI5Rjqj98MX5fwqpg/edit?usp=sharing).