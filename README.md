# COSC-320-Project

Our project works by iterating through a tweet and replacing the abbreviated words with the corresponding keywords/phrases. We have designed an algorithm that finds an abbreviated word and then matches it to the corresponding word in the list instead of iterating through each keyword. After finding a match, the abbreviated word is replaced by its full form in the tweet.

**Algorithm Description:-**

First algorithm: 
Using regular expressions, find matches for abbreviations in the tweet. From this, we get the starting index of the first letter of the abbreviation as well as the end index. With the group of abbreviated words found in the tweet, compare the values of the group to a hash table where the full form of all the abbreviations are stored. Use the key value pairs of the has table to return the expanded forms.

Second algorithm: 
The second algorith looks to replace the abbreviated words in the tweets in their full forms after they have been found from the first algorithm. We use the index of the abbreviated word to be replaced, the expanded form of the abbreviation, and the string tweet. We create a doubly linked list from the tweet where each node is a separate word in the tweet. We pass this list as well as the index to the replace method and here we replace the word and shift the elements in the list to account for expanded form of the abbreviation. We return the updated list to the main method and then iterate over the tweet again until we find the next abbreviated word. If none are found, the program ends and we are left with a tweet where the abbreviations have been expanded to their full forms. 

**Algorithm Analysis:-**

First Algorithm: 
Let n = number of words in the string, m = number of elements in the regular expression pattern, i = the number of indixes found to be replaced 
The time complexity for using regex to find abbreviations in the tweet is O(m\*n), the time for hash table lookup is a constant O(1). Hence, the total time complexity for this algorithm is O(m\*n) + O(1). 
Asymptotic runtime - O(m\*n)

Second Algorithm: 
Let n = number of words in the string, i = number of indexes found to be replaced in the string
The time complexity for insertion in a doubly linked list is O(1) and there are i indexes to be replaced which means the effective time complexity for this particular algorithm is O(i).
Asymptotic runtime - O(i)

**Algorithm Graphs:-**

First Algorithm:
As you can see in the graphs, the first one shows the real values generated at differeant input sizes for the tweets. The dataset that we chose contains 925000 tweets so the maximum has been set to that. If we compare our graphs values to the asymptotic runtime that we got for the first algorith of O(m\*n), we can see that the values are consistent with that.
![image1](graph1.png)

Second Algorithm: 
In the second algorithm, it is much of the same as we have again plotted the real values generated for different input sizes of the tweets. The dataset contains over 100000 tweets and hence the maximum has again been set to that. Comparing our graphs to the asymptotic runtime that we have for the second algorithm, we can see that it is also O(i) which is consistent with what we had predicted.
![image2](image.png)

**Dataset Used:-**
https://www.kaggle.com/datasets/tariqsays/sentiment-dataset-with-1-million-tweets

**Video Presentation:-**
https://youtu.be/OZ2kBXunjAE

**Task Separation:-**

Milestone 1:
Problem Formulation - Nikhil, Ishaan, Manroop
Pseudocode - Nikhil
Algorithm Analysis - Ishaan
Unexpected Cases - Manroop

Milestone 2:
Problem Formulation - Nikhil, Ishaan, Manroop
Algorithm Analysis - Nikhil, Ishaan, Manroop
Data Structure - Manroop
Unexpected Cases - Nikhil
Pseudocode - Ishaan

Milestone 3: 
Datasets - Nikhil, Manroop
Implementation - Nikhil, Ishaan, Manroop
Results - Nikhil
Unexpected Cases - Ishaan

Milestone 4:
Code - Nikhil
Report - Ishaan
Video Presentation - Manroop
