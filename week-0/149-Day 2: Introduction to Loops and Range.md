## Learning Objectives

* While loop
* For loop
* Enumerate
* Range


## Loops


* A loop is a sequence of instructions continuously repeated until a specific condition is reached.
* Think about a teacher taking attendance. The teacher calls out a name, and the student responds present.
* The teacher is going through the list of students one by one and calling a name to get "present" if the student is present or "\<<silence\>>" if they are absent.
* This process will only end when the whole list of students is completed. This will be the condition that will break out of the loop.
* Let's look at the types of loops in Python!


## For Loop










<iframe width="560" height="315" src="https://www.youtube.com/embed/OnDr4J2UXSA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>













* "For loop" is used for iterating over a sequence (that can be any data structure - list/tuples or even a string)
* Iteration means performing an action repeatedly
* Syntax:  
```
for variable in sequence:
   expression
```



* Which means "for each variable in sequence, execute the expression"
* Python uses indentation as its method of grouping statements. So all the statements having the same indentation will be considered inside the for loop.


### Looping through a List

* Example:  
Let's say we wish to store the heights of our family members in a list and print them one by one.  
![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_78d2a027c8a645458c8e3d8707a9a1ff.png)





* Internal Working:
  * First, we store all the heights in a list named fam_heights
  * Now, we'll go to each element and print it
  * This action will continue until all the list elements are printed in order.



### Looping through a String

* Even strings are iterable objects; they contain a sequence of characters:





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_726789df6f2048b1bd9a1034f3729343.png)





* As you can see, each string character is printed in a separate line.
* We can even apply string methods in the for loop.





![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_a44db7e745d84708bd4a6d02cd08c3e7.png)







## Enumerate

* With the for loop, you could print the heights of your family members.
* But what if you also want to access the index of each element of the list? Here is where the enumerate function comes into play.
* The enumerate function iterates over the elements of a list and associates an index with them. You need to use two variables (index and height in this case) to store the values given by enumerate.






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_5ec3032622da4df7964241e586047bf7.png)






## While Loop







<iframe width="560" height="315" src="https://www.youtube.com/embed/6TEGxJXLAWQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>











* With the while loop, we can execute a set of statements repeatedly as long as a condition is true.
* Syntax:
```
while condition:
  statement(s)
```
* All the statements indented by the same number of character spaces after a while condition are considered part of a single block of code. Python uses indentation as its method of grouping statements.

* For example:




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3d0a609a2d804634a64d58be1043de78.png)








* Let us understand what is happening in the above program.
  * Value of x is assigned as 1
  * The while loop starts with the condition that x must be less than 4
  * The subsequent two statements have the same indentation and will be considered a part of the while loop
  * The value of x is printed. Initially, x=1
  * The value of x is then increased by 1. So now, x=2
  * Control goes back to the condition line; x is less than 4 (2<4). This means that the following statements will be executed again
  * This continues until x is assigned a value of 4. Then, the condition fails as x is not less than 4
  * The next two statements will not be executed, and the while loop will end.

## range()

* range() allows the user to generate a series of numbers within a given range.
* The user can decide where that series of numbers will begin and end and how big the difference will be between one number and the next.
* range() takes mainly three arguments:
  * A start argument is a starting number of the sequence. i.e., lower limit. By default, it starts with 0 if not specified.
  * A stop argument is an upper limit. i.e., generate numbers up to this number. The range() doesn't include this number in the result.
  * The step is a difference between each number in the result. The default value of the step is one if not specified.
* range() only works with the integers. You can not use float number or any other type in a start, stop and step argument of a range().

You can call the range function in three ways:
* range(stop) takes one argument.
* range(start, stop) takes two arguments.
* range(start, stop, step) takes three arguments.

**Example 1: Using only one argument**



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_010d8999dd964eeb86cb7876a748cb5f.png)





* Output:  
0, 1, 2, 3, 4,
* By default, print statement prints in different lines. You can use the end argument if you want to print the output in the same line. ',' specifies that a comma will separate each output.
* Only a stop argument is passed to range(). So by default, it takes start = 0 and step = 1.

**Example 2: Using two arguments (i.e., start and stop)**



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_6f075918c999401aa590c484bb627e26.png)





* Output:  
5, 6, 7, 8, 9,
* By default, it took the step value as 1.

**Example 3: Using all three arguments**




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_a5ebd1229c7b4b04aa0967173f015f3c.png)






* Output:  
Printing All even numbers between 2 and 10 using range()  
2, 4, 6, 8,
* All three arguments are specified i.e., start = 2, stop = 10, step = 2. The step value is two, so the difference between each number is 2.

### Additional Reading

* A few more concepts like break, continue, and nested loops are commonly used in Python.
* Must learn: Learn about these important concepts from the below cheat sheet:  
https://www.codecademy.com/learn/learn-python-3/modules/learn-python3-loops/cheatsheet  
_Tip: If you are unable to follow, run the code and make out the difference_
* Find out how the range function works with strings and lists.
_Hint: You'll use their lengths instead_

### Let's Practice!
1. Print the First ten natural numbers using a while loop.
1. Iterate over the following list and print the elements:  
list1 = [12, 15, 32, 42, 55, 75, 122, 132, 150, 180, 200]
1. Accept a number n from the user and print its multiplication table
1. Use the enumerate function to print the elements of this list along with the indices:  
grocery = ['bread', 'milk', 'butter']
1. Take a number n from the user and find the sum of all numbers between 1 to n.
1. Create a sequence of numbers from 3 to 5, and print each item in the sequence.
1. Create a sequence of numbers from 3 to 19, but increment by 2
instead of 1.
1. Print the letters of the string "Python" in the same line:
   * Using a simple for loop
   * Using the range function

The above questions are for self-practice and ungraded; you don't need to upload them.

### Slide Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1wn4Bt_yFiT8e6ba2h4YMRGb7A_sTFCAOXU7Buy3AQ5k/edit?usp=sharing).