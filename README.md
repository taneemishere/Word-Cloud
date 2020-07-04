# Word Cloud
A python program that makes you the cloud full of words and joy 😛.

## Program Worflow
### Step 1: Importing the Libraries
The first step in any python program will always be on importing the libraries. For this code we will require only three libraries, out of which two should already have been installed in your Python workspace. The only library to be additionally installed before this program is the ‘wordcloud’ library which can be easily installed using the ‘pip’ command. Also keep in mind that if you didn't install the Visual Studio C++ desktop development, chances are high that this wordcloud won't work i-e it won't be install.

### Step 2: Reading the Data File
In the next step, we will read the data file (the .csv file) and store in into a Pandas DataFrame. The pandas data frames are always easier and faster to use when working with large datasets. The column required for our word cloud generation can be easily accessed from the pandas data frame.

### Step 3: Setting the comment and stop words
In this step, we initialize two important strings for our word cloud generation.
The ‘comment_words’ is the string that will be used to store all the words of the CONTENT column in a single line of text
The ‘stop_words’ is used to store all the words that are very commonly used in English language such as ‘the’, ‘a’, ‘an’, ‘in’. These words will be later filtered while generating the word cloud.

### Step 4: Iterating through the data file
Now that we have stored the data file into a pandas dataframe, we now have to convert each row of the ‘CONTENT’ column to a very long, single line of text.
The first step in this will be to split each word in a row ( a comment has a finite number of words) and store it in a variable. separate = i.split()
After splitting the words, for homogeneity of all the words, we convert all the words to lowercase using the .lower() function.
Finally, we join all the words and store it to the variable ‘comment_words’ using the function .join() The variable ‘comment_words’ now contains all the words in a single long text necessary to generate our word cloud.

### Step 5: Creating the Word Cloud
In this step, we finally generate the word cloud using the ‘WordCloud’ function. In this we will be using the two variables ‘stop_words’ and ‘comment_words’. The code is self-explanatory and easy to understand.

### Step 6: Displaying the Word Cloud
The last and final step is to display our word cloud that we just generated using the above code. The ‘matplotlib.pyplot’ library is used to display the word cloud. Take a look at the word cloud generated below!

## The Data
For generating this word cloud, I will be using a data set that was originally created for building a spam comment classifier.
The file 'Youtube05-Shakira.csv' is a data set that consists of 5 columns such as the COMMENT ID, AUTHOR, DATE, CONTENT and CLASS. The ‘CONTENT’ and ‘CLASS’ columns are used to build a machine learning model to classify a message if it is a spam message or not.
For generating our word cloud, I will be using only words in the ‘CONTENT’ column.

## Screenshots
![Sample 1](https://github.com/taneemishere/Word-Cloud/blob/master/sample%201.png)
![Sample 2](https://github.com/taneemishere/Word-Cloud/blob/master/sample%202.png)
