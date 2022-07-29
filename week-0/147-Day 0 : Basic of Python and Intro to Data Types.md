## Comments

* When writing code in Python, it's important to ensure that your code can be easily understood by others, say by your friend who wants to see your code.
* Python ignores everything after the hash mark and up to the end of the line. You can insert them anywhere in your code!
* A shortcut for adding comments is by using CTRL + /






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_29ee7fa9db7547e7a27a0b594f0b6439.png)




## Operators

* Operators perform simple additions, comparisons, etc., on variables and values.
* Python supports the following types of operators; we will look at some commonly used operators.





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_81ee485f7f764adab348953571221415.png)



### Arithmetic Operator

Using Python, we can perform some basic arithmetic operations such as additions, subtraction, multiplication, etc.

Example:\
\
x = 2\
y = 3\
x +  y # addition\
x \* y  # multiplication






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_1c070481598b4573a0df27c077255ce7.png)





### Comparison Operator

* These are used to compare two values
* Gives a boolean result (True/False)






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_42a835cf9eaa47e3acab3d8df987ab48.png)









## Variables

* A variable can be considered as a storage container for data.
* Every variable will have a name.
* It is a good way to store information while making it easy to refer to that information in our code later.




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_10ab1536fee048fb832c6af2ec522c23.png)



* For instance, instead of working with the number 3.14, we can assign it to a variable pi and use it as many times as we want in our code (wherever required).
* The equal sign (=) is used to assign values to variables.
* The syntax for assigning values to a variable is as follows: Variable name = value or information.
* Example:
  * x = 5
  * y = "John"




## Input and Output

### Print Function




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_fd546348d9234eb595442f9b8aac3c74.png)






### Input Function








![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_a2bcf202d29042a799cfd7e5cce5489a.png)












![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_01facc263b48463f95c6da48a1c35c40.png)




## Data Structures and Data Types

* If you're learning Python from multiple sources, you might encounter the terms data structures and data types being used interchangeably.
* **Definition:** Data structure is a general computer science concept. Its definition reads as follows on Wikipedia:
* **Data structure is a data organization, management, and storage format that enables efficient access and modification.** More precisely, a data structure is a collection of data values, their relationships, and the functions or operations that can be applied to the data.
* Whereas Data type is a concept specific to a programming language. In a way, it is a concrete implementation of a data structure in a particular programming language (Python or any other language).
* \*\*The definition of what constitutes a "type" varies among programming languages. \*\*Talking about Python, there are basic data types like int, float, string, etc. You can use the built-in types like list, set, etc., which we will cover in this session.
* Calling these data types as data structures won't be wrong because there is no significant difference between the two in Python.



### Data Types in Python

*   Before we proceed to discuss what data types in Python are, there are some basic questions that we would discuss. **What is data?**
* Let's say you are going to meet a friend at her office. When you go to visit her office, the security guard asks you to make an entry in the register before you enter the office. A typical entry register asks for the following information –



|                    |                            |                       |                |
| ------------------ | -------------------------- | --------------------- | -------------- |
| **Visitor's name** | **Visitor's phone number** | **Visitor's address** | **Entry time** |
| **Karen**          | **32 000 000**             | **Leuven**            | **8:30 AM**    |


* The above information that you just provided is data.
* We see that the data entered in the previous slide has different varieties:
  * Some are English letters,
  * Some are numerical digits, and
  * There are some special characters, dash (-) and colon ( : ).
  * In this example, our data is divided into four categories – name, phone number, address, and time.
  *   This\*\* categorization of data, **based on their characteristic & our need,** is called data types.

*   Some of the data types in Python include:

    * Integer: whole numbers, positive or negative numbers. E.g.: 100
    * Float: Floating-point numbers are real numbers, rational or irrational. In most cases, this means numbers with decimal fractions. Example: 123.45

    * String: Strings are sequences of characters, or text, enclosed in quotes. Example: "any text", "Karen" \\
* For further reading:
  * [operators and data types](https://www.dummies.com/programming/python/python-all-in-one-for-dummies-cheat-sheet/)
* For practice and different data type examples, visit: [https://www.w3schools.com/python/python\_datatypes.asp](https://www.w3schools.com/python/python\_datatypes.asp)



### Getting the Data Type

You can get the data type of any object by using the type( ) function:

* **Numerical Types:** int (integer), float (decimal)
* **Text Type:** str (string)
* **Boolean Type:** bool (True or False)










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_b7a4571d7ffc429582b4a1ee5f456801.png)






## Strings

### Sequence Types

* Sequences allow you to store multiple values in an **organized and efficient way**.&#x20;
* There are seven sequence types: strings, Unicode strings, lists, tuples, bytearrays, buffers, and xrange objects.&#x20;
* _Nothing to worry about looking at this long list; you will get to know it gradually._



### Python Strings

* Strings are a sequence of characters.&#x20;
* Let us see some examples of String: My name is Rahul, Rahul, Go home. All these are examples of String.&#x20;
* In Python, Strings are called str.&#x20;
* There is a specific way of defining String in Python – it is defined within single quotes (') or double quotes ("), or even triple quotes ("').&#x20;

### Accessing String Elements

* Square brackets can be used to access elements of the string.
* **Remember that the first character has index 0.**
* Index refers to the position of a character in a string. In python index number starts from 0.
* Example:  
  ```
  a = "Hello, World!"
  print(a[1])
  ```
* &#x20;**Will give an output e. Can you understand why?**




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3f6d824115394b55b5c582052a908ed5.png)




* Hope you got the answer to the previous question now!







### String Slicing

* We can also call out a range of characters from the string using string slicing.
* Specify the start and end indexes separated by a colon to return a part of the string. Note that the character of the end index is not included.
* Suppose we want to print World from the string "Hello World". We can do so as below:






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_0f7e306deae647419d9331fcb255011c.png)



### Negative Indexing

* If we have a long string and we want to pinpoint an item towards the end, we can also count backward from the end of the string, starting at the index number -1
*   Printing 'r' from the string :
    ```
    a = "Hello, World!"
    print(a[-4])
    ```
* Get the characters from position -5 to position -1, starting the count from the end of the string: 
  `print(a[-5:-2])`
* Will give an output: orl

### String Concatenation

* String concatenation means adding strings together.
* Use the + character to add a variable to another variable:
*   Example:

    






    ![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_f27b66852169453691f72348f9f8ed61.png)
* Another example:
  ```
  x = "Python is "
  y = "awesome"
  z =  x + y
  print(z)
  ```
* **Output: Python is awesome**




### String Length

* To get the length of a string, use the len( ) function.
*   Getting the length of the string a :

    'a = "Hello, World!"`

    `print(len(a))`
* **Output: 13**






### String Methods

* Python has a set of built-in methods you can use on strings.
* Must learn: Learn about important string methods from the below cheatsheet: [https://www.codecademy.com/learn/learn-python-3/modules/learn-python3-strings/cheatsheet](https://www.codecademy.com/learn/learn-python-3/modules/learn-python3-strings/cheatsheet)&#x20;
* Tip: If you cannot follow, run the code and make the difference.