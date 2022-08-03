## Learning Objectives

* Reading a data file
* Writing a data file

## Reading Data Files

* It is always good to be able to create a dataframe by hand. But, generally, we don’t create our own data by hand. We work on the data that already exists.
* Data exists in number of formats. The most basic of these is the **csv** file**. csv stands for comma-separated-value**

### **What is a CSV file?**









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_d9f0b76fe56547028e47aadd24a72420.png)










* CSV files are normally created by programs that handle large amounts of data. They are a convenient way to export data from spreadsheets and databases as well as import or use it in other programs.&#x20;
* CSV (Comma Separated Values) is a simple file format used to store tabular data, such as a spreadsheet or database.&#x20;
* A CSV file stores tabular data (numbers and text) in plain text.&#x20;
* Each line of the file is a data record.&#x20;
* Each record consists of one or more fields, separated by commas.&#x20;
* The use of the comma as a field separator is the source of the name for this file format.

### How does CSV look like?










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3d8387f243f04387b7e26c2dfb87fef2.png)










### Working with CSV files in Python

* For working CSV files in python, there is an inbuilt function named read\_csv.
* However, a common method for working with CSV files is using Pandas. It makes importing and analyzing data much easier.
* One crucial feature of Pandas is its ability to write and read Excel, CSV, and many other types of files.&#x20;

## Pandas read_csv

* Functions like the Pandas read\_csv() method enable you to work with files effectively.&#x20;
* The read\_csv() function reads the CSV file into a DataFrame object.
* A CSV file is similar to a two-dimensional table and the DataFrame object represents two dimensional tabular view.
* The most basic way to read a csv file in Pandas:&#x20;






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_05cbcb6e9bd7452ca0a20d6632799f3c.png)





* Now, let's understand how to provide filename






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3ab585b60bf7438388328132eb62eed7.png)





* There are many other things one can do through this function only to change the returned object completely.&#x20;
* For instance, one can read a csv file not only locally, but from a URL through read\_csv or one can choose what columns needed to export so that we don’t have to edit the array later.
* These modifications can be done by the various arguments it takes.
* We don’t need to memorise all the arguments though, let’s have a look at few important ones in the next two slides.

### Pandas to\_csv with example

* The easiest way to write DataFrames to CSV files is using the Pandas to\_csv function.
* **Syntax:**




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_f5966255a3954954b00b240424e929c9.png)



* **If you want to export without the index, simply add index=False**

![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_c2d4878eb34d465f98240d3894801922.png)

* **Example:**



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_35a79b4cb9284d7bab939c655c8bb735.png)

### Comprehensive Tutorial

* Must Read  
A comprehensive tutorial on Pandas for beginners:  
https://www.learndatasci.com/tutorials/python-pandas-tutorial-complete-introduction-for-beginners/

### Slide Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1QOGc8ltwHv6SlvVe9beXwSGmEzPmR-dKUsqFa6WBYzg/edit?usp=sharing).