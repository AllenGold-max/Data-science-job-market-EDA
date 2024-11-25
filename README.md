# Data Science Job Market EDA and Text Analysis
*By: <a href = 'https://www.linkedin.com/in/Olisa-Oluwatunbi/'>Olisa Oluwatunbi Emmanuel</a>*

## Introduction

I've been actively looking for job in the field of data science. I was wondering what the trend of skills and tools employers are looking for in data science professionals, what the requirements are and know if i already have adequeate skills. So I set out to look for data on this subject. I came across this <a href = 'https://www.kaggle.com/sl6149/data-scientist-job-market-in-the-us'>Kaggle dataset</a> uploaded by ShaShan Lu. He scrapped 7000 job posting from indeed.com with the search term of "Data Science".

I'll approach this data by performing EDA on the general dataset and text analysis on the job description. If you have comments, recommendations and advice on this notebook, it would be much appreciated!

## Data Preparation
This dataset contains 6953 rows with 5 columns which are: Position, Company, Job Description, Review, and Location.

### Data Cleaning
In order to clean the data, I would be checking for the number of NaNs in each column. After doing this i dsicovered that the Review column has the greatest nunber of NaNs. Since the Review column has the greatest number of NaNs, I decided to drop it all together since I won't be doing analysis on it. For the rest of the NaNs, I filtered the data frame to leave out all the rows containing null values.

## Exporatory Data Analysis
In this section, I'll would be answering the following queation using **pandas** and **matplotlib**:

- What is the is the most common job to appear when searching for 'Data Science'?
- Which company hire the most Data Science job?
- From the data, which cities and state hire the most?

### Positions by Job Title
Since position titles are varied from one company to another, the following code block will categorize the titles into 5 groups: Data Scientist, Machine Learning Engineer, Data Analyst, Data Science Manager, and Others.

*Note: I want to give credit to Pramod Manjegowda for the following code block. Pramad followed a machine learning approach toward this data set. You can take a look at his notebook <a href ='https://www.kaggle.com/pramod7/data-science-jobs-opening-in-us-analysis-ml'>here</a>.*



### Positions by Companies 

![Image](assets/image.png)


From the chart, we can see that Amazon.com hire the most candidate, follow by Ball Aerospace, Microsoft and Google.


### Positions by Cities


It appears that the top 5 cities that hire the most data science related job are New York, Seattle, Cambridge, Boston, and San Francisco. It makes sense since those cities are the technology hub of the country. 

### Positions by States

Even though the city with the highest number of positions is New York, the highest number of position by state is California, follows by Massachusetts and Washington.

### Position by State and Job Title 

- For Data Science Manager, Data Scientist and Machine Learning Engineer, California is the state that hire the most position
- For Data Analyst, it seems that New York hires the most position, follow closely by California

## Text Analysis 

In this section, I will focus on the Job Description column of the data. By using libraries like **re, wordcloud, matplotlib**, I hope to gain further insights on the requirements for the field of data science. I will try to answer the following questions:
- What are the companies looking for when hiring?
- How many years of experience do they required?
- What level of education do the companies prefer?

### Word Cloud 

Here are my interpretations from looking at the WordCloud:
- Data Analyst will be doing **research**, **analysis** and **provide** insights to facilitate better **business** decision.
- Data Science Manager will be in charge of **developing** **product** to help **business** serve its **customer** better.
- Data Scientist will be doing **research**, implementing **machine learning** and building **model** to come up with business solution.
- Machine Learning Engineer will **design** and **develop** **software** for business or customer.


