## Learning Objectives

* Reading a data file
* Writing a data file

## Reading Data Files

* It is always good to be able to create a dataframe by hand. But, generally, we don't make our data by hand. We work on the data that already exists.
* Data exists in several formats. The most basic of these is the **CSV** file**. CSV stands for comma-separated-value**

### **What is a CSV file?**









![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_d9f0b76fe56547028e47aadd24a72420.png)










* CSV files are normally created by programs that handle large amounts of data. They are a convenient way to export data from spreadsheets and databases and import or use it in other programs.&#x20;
* CSV (Comma Separated Values) is a simple file format that stores tabular data, such as a spreadsheet or database.&#x20;
* A CSV file stores tabular data (numbers and text) in plain text.&#x20;
* Each line of the file is a data record.&#x20;
* Each record consists of one or more fields, separated by commas.&#x20;
* The use of the comma as a field separator is the source of the name for this file format.

### How does CSV look like?










![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3d8387f243f04387b7e26c2dfb87fef2.png)










### Working with CSV files in Python

* For working CSV files in Python, there is an inbuilt function named read\_csv.
* However, a common method for working with CSV files is using Pandas. It makes importing and analyzing data much easier.
* One crucial feature of Pandas is its ability to write and read Excel, CSV, and many other types of files.&#x20;

## Pandas read_csv

* Functions like the Pandas read\_csv() method enable you to work with files effectively.&#x20;
* The read\_csv() function reads the CSV file into a DataFrame object.
* A CSV file is similar to a two-dimensional table, and the DataFrame object represents a two-dimensional tabular view.
* The most basic way to read a CSV file in Pandas:&#x20;






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_05cbcb6e9bd7452ca0a20d6632799f3c.png)





* Now, let's understand how to provide the filename






![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_3ab585b60bf7438388328132eb62eed7.png)





* One can do many other things through this function only to change the returned object completely.&#x20;
* For instance, one can read a CSV file not only locally but from a URL through read_csv or choose what columns are to be imported so that we don't have to edit the array later.
* These modifications can be done by the various arguments it takes.
* We don't need to memorize all the arguments, though. Let's look at a few important ones below.

### Pandas to\_csv with example

* The easiest way to write DataFrames to CSV files is using the Pandas to\_csv function.
* **Syntax:**




![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_f5966255a3954954b00b240424e929c9.png)



* **If you want to export without the index, add index=False**

![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_c2d4878eb34d465f98240d3894801922.png)

* **Example:**



![image.png](https://dphi-live.s3.amazonaws.com/media_uploads/image_35a79b4cb9284d7bab939c655c8bb735.png)

### Comprehensive Tutorial

* Must Read  
A comprehensive tutorial on Pandas for beginners:  
https://www.learndatasci.com/tutorials/python-pandas-tutorial-complete-introduction-for-beginners/

### Slide Download Link

You can download the slides for this topic from [here](https://docs.google.com/presentation/d/1QOGc8ltwHv6SlvVe9beXwSGmEzPmR-dKUsqFa6WBYzg/edit?usp=sharing).