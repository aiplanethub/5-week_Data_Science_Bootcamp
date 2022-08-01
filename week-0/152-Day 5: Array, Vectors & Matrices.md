## Learning Objectives

* Understanding keywords
* Arrays
* Lists vs. Arrays
* Vectors
* Matrices



## Understanding Keywords

Before jumping into what arrays are all about, we need to recap what we learned about Lists in the "Introduction to Python Programming" course. In addition, we need to know about some keywords such as "Dimension".

### List

* As the name suggests, **List is an ordered sequence of data. In real life, if you could make a list of things that come to your mind** (or event for any specific purpose), it could be something like this –
  * Brush
  * Leuven
  * 48851964400
  * 3.14
  * Mom
* **You could make your own list & include whatever you want in it.** So, in my list, I have included what I do early in the morning, my city, my mobile number, the value of pi to two digits, and mom.
* If you look at it, my list has different types of data – strings, float, and integer. And this is the kind of flexibility Python List provides. It can hold different types of data types. **Declaring a List is pretty straightforward. You use square brackets (\[]) and separate the items by a comma.** Let me write an example -

    A = \["Brush", "Leuven", 48851964400, 3.14, "Mom"]





### Dimensions

**Now, what are dimensions?** - Let's take an example of a box to explain this. A box has three dimensions - width, length, and depth (or height). Similarly, in data science, we will work in "N" dimensions in a data structure (list, arrays, vectors, etc.). "N" could be any number.









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_e1f41fbda62c47b4ad85a8c1cb22f44b.png)










## Arrays

### What are Arrays?

* Similar to a list, an array is a data structure that can hold more than one value at a time.
* **However, an array can only hold a collection of ordered elements of the same data type.**

### Examples of Arrays & Lists

* [1, 2, 3, 4, 5] is an array of integers
* ['a', 'b', 'c', 'd', 'e'] is an array of strings
* [[1,2,3,4],  
[5,6,7,8]] is a 2-dimensional array.

**Lists - Examples**

* [ 1, 2, 3, 'a', 5 ] is a list containing both integers and a string
* [ 1, 2, 3, 4, ‘b’, [ 1, 2, 3 ] ]

### Why Arrays?

* A combination of Arrays and Python could save you a lot of time. Arrays help reduce the overall size of your code.

### List vs Array

* A list can store values such as integers, strings, etc. Whereas arrays store only single data type values, i.e., you can only have an array of integers, an array of strings, etc.



## Vectors

* A vector, in programming, is a type of array that is one-dimensional.
* For example, \[1, 2, 3, 4, 5] is a vector.

## Matrix

* Matrix is an arrangement of numbers into rows and columns






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_021eec7d3ade466490eb1b427e4ba457.png)









* The matrix A has two rows and three columns

### Shape of Matrix

* Since matrix A has two rows and three columns, we write its shape as 2 X 3, pronounced as 'two by three'.

### Dimension of Matrix

* The shape of the matrix also tells you its dimensions. The dimension of matrix A is two as its shape is 2 X 3.
* If a matrix has its shape as 2 X 3 X 2 (say, for example), the dimension of the matrix would be 3.
* Don't worry if you don't get this point. You will make it as you go along

### Matrix

* Matrix B has three rows and two columns, so it is a 3 X 2 matrix


![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_22262e9d703d4568a00588c88d9deb16.png)


* Whenever you are working with matrix shape, remember rows X columns