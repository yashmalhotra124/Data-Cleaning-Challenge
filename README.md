# Data-Cleaning-Challenge
This includes the necessary steps that are required for Data cleaning
Data Cleaning Steps 

In order to analyse the data, we need to perform data cleaning and that involves these major 5 steps that I took as a challenge and finished it. Note that the datasets are taken from Kaggle and this is just to show my data analysis skills towards datasets.

 The steps are:

1.	Handling Missing Values – involves checking the missing values by counting the number of null values using the isnull() and sum(). Then I removed all the missing values from the dataset using the dropna(). Here since each row contains atleast 1 missing data all the entries are dropped and thus we remove all the values as per the columns by using dropna(axis = 1). Here axis=1, itself determines that we are specifying the columns ( axis =1 ). Once we drop all the na’s we store it in variable and fill all the na’s with fillna(0). It will replace all the na’s with 0 and we add it back to the dataset. Thus this dataset is equal to the original dataset but with the only change of na’s with 0’s. 

2.	Scaling and Normalization – In scaling, you change the range of the data while in normalization you change the shape of the distribution of the data. Here we have the original data and we use the minmax scaling and plot both the original data and the scaled data. We use stats.boxcox to find the normalized values of the original data. 


3.	Parsing Dates – Parsing the dates means to change the datatype of date. First we check the datatype of the date column in original datasets i.e. object. We then convert Date columns to DateTime and thus the datatype changes from object to datetime.

4.	Character Encodings - Character encodings are particular sets of guidelines for translating raw binary byte sequences (which resemble the following: 0110100001101001) into characters that constitute human-readable text (like "hi"). There are many different encodings, therefore if you tried to read in text using one other than the one it was originally written in, the result was "mojibake," which is jumbled text (said like mo-gee-bah-kay). We use encoding on a string just to check if it works. Later we apply the encoding on the dataset and save the file with the UTF-8 encoding.


5.	Inconsistent Data Entry – here we use fuzzywuzzy library to check any inconsistent data in the csv file. First we sort all the values uniquely and check if there is any inconsistency. Then we use a function and replace all the inconsistent repeated values with just one value of one type. For eg- a dataset might include the data apple and APPLE and we know both are the same and still are counted as two separate values. By removing the inconsistency, it is considered and displayed as 1 unique value.
