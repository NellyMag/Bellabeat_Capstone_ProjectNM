# Bellabeat_Capstone_ProjectNM
Introduction

Hello, I am Nelly, and welcome to my capstone project. I have completed my Google Data Analytics certificate. This project analyzes smart device usage data to gain insight into how consumers use non-Bellabeat smart devices. Contact Me


Project Summary 
Bellabeat, founded in 2013 by Urška Sršen and Sando Mur, creates health-focused smart products for women, empowering them with insights into their activity, sleep, stress, and reproductive health. The company has grown rapidly, expanding globally and focusing on digital marketing across platforms like Google, Facebook, and YouTube.
In this project, I analyzed Bellabeat's smart device usage data to uncover key trends and provide recommendations to optimize their marketing strategy and drive growth.

Insights and recommendations are provided in the following key areas:

1. What are some trends in smart device usage?
2. How could these trends apply to Bellabeat customers? 
3. How could these trends help influence Bellabeat's marketing strategy? 

Prepare Phase
Data Source


The Bellabeat dataset comes from Kaggle, a reputable data science competition platform and an online community. I received CSV file datasets in long format covering three months (3/12/2016 - 4/11/2016)  and (4/12/2016 -  5/12/2016). Here is the Bella data.
Limitations
Sample size: The data were collected from 30 Fitbit users; this sample is small and does not accurately represent the larger population.
Bias: The data do not provide the demographic of the 30 users. Therefore, I cannot rule out data bias during data collection. 
Demographics include but are not limited to age, gender, fitness level, occupation, family size, marital status, income, education, and religion.
Outdated information: The data were collected in 2016.


Process Phase The query used can be found [here](https://drive.google.com/file/d/1uw3-nUHULeLXIV16lpwADqjCsUw75bJ6/view?usp=sharing).


I encountered issues with the big data error "file is too big" when opening a few CSV files directly in Microsoft Excel. I decided to clean the data in Google Sheets and RStudio. Due to sample size, I decided to combine/ merge the dataset to cover 3/12/2016 to 5/12/2016  Clean Data in Google Sheets.
 Out of the 29 data files, only 8 contained either primary, secondary, or relevant information, such as daily activity (one CSV file covering 3/12/2016 to 4/11/2016 and another daily activity CSV file covering 4/12/2016 to 5/12/2016).


I chose to work with the following data:
dailyactivity
hourlycalories
weightloginfo

Google Sheets
Data Cleaning 
Use the filter to remove blank values.

For dailyactivity
Insert a new column and name it “Time.” In an empty column, write the function (=MOD(text,1) and use the auto fill handler. Next, copy the MOD result and only paste the value onto “Time”. Delete the column used to execute the MOD function. Next, change the formats of the data column to “Date” and the time to “Time”.

Repeat this process for hourlycalories and weightloginfo

Delete column “fat” from weightloginfo

Convert WeightKb to WeightLb by multiplying the kg value by 2.2.

Merge each data onto one single file using ={dailyActivity1_merged!A2:O941; dailyActivity2!A2:O941}.






RStudio
Preparation












Analysis






Share 



















For my presentation, I will focus on Bellabeat’s smart watches, which track user activity, sleep, and stress. The Time watch connects to the Bellabeat app to provide insights into daily wellness.
