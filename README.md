# Bellabeat_Capstone_Project

<h2>Project Summary</h2>

Bellabeat, founded in 2013 by Urška Sršen and Sando Mur, creates health-focused smart products for women, empowering them with insights into their activity, sleep, stress, and reproductive health. The company has grown rapidly, expanding globally and focusing on digital marketing across platforms like Google, Facebook, and YouTube.
In this project, I analyzed Bellabeat's smart device usage data to uncover key trends and provide recommendations to optimize their marketing strategy and drive growth.

Insights and recommendations are provided in the following key areas:

1. What are some trends in smart device usage?
2. How could these trends apply to Bellabeat customers? 
3. How could these trends help influence Bellabeat's marketing strategy? 

Detailed process  [here](https://drive.google.com/file/d/1utoIF88WcAzDPMLjWiuE4lj9CK91vSTr/view?usp=drive_link).

<h2>Prepare Phase</h2>
<h3>Data Source</h3>


The Bellabeat dataset comes from Kaggle, a reputable data science competition platform and an online community. I received CSV file datasets in long format covering three months (3/12/2016 - 4/11/2016)  and (4/12/2016 -  5/12/2016)—the dataset [link](https://www.kaggle.com/datasets/arashnic/fitbit).

<h3>Limitations</h3>

Sample size: The data were collected from 30 Fitbit users; this sample is small and does not accurately represent the larger population.
Bias: The data do not provide the demographic of the 30 users. Therefore, I cannot rule out data bias during data collection. 
Demographics include but are not limited to age, gender, fitness level, occupation, family size, marital status, income, education, and religion.
Outdated information: The data were collected in 2016.


<h2>Process Phase</h2>

<h3>Limitations</h3>

I encountered issues with the big data error "file is too big" when opening a few CSV files directly in Microsoft Excel. I decided to clean the data in Google Sheets and RStudio. Due to sample size, I decided to combine/ merge the dataset to cover 3/12/2016 to 5/12/2016,  Clean Data in Google Sheets.

Out of the 29 data files, only 8 contained either primary, secondary, or relevant information, such as daily activity (one CSV file covering 3/12/2016 to 4/11/2016 and another daily activity CSV file covering 4/12/2016 to 5/12/2016).


I chose to work with the following data:
+ dailyactivity
+ hourlycalories
+ weightloginfo

<h3>Cleaning</h3>
<h4>Google Sheets</h4>

+ Remove blank values.

+ For dailyactivity:
  Insert a new column and name it “Time.” In an empty column, write the function (=MOD(text,1) and use the auto fill handler. Next, copy the MOD result and only paste the value onto “Time”. Delete the column used to execute the MOD function. Next, change the formats of the data column to “Date” and the time to “Time”.

+ Repeat this process for hourlycalories and weightloginfo

+ Delete column “fat” from weightloginfo

+ Convert WeightKb to WeightLb by multiplying the kg value by 2.2.

+ Merge each data onto one single file using ={dailyActivity1_merged!A2:O941; dailyActivity2!A2:O941}.

<h4>RStudio</h4>

The query used can be found [here](https://drive.google.com/file/d/1utoIF88WcAzDPMLjWiuE4lj9CK91vSTr/view?usp=drive_link)

<h2>Executive Summary</h2>

Smartwatch users generally have low activity levels, indicating a lack of daily physical activity. Despite this, they engage in movement at various points throughout the day. Users with higher step counts tend to burn more calories, and activity is highest between 12 PM and 11 PM, especially in the afternoon. To improve health outcomes, I recommend creating a marketing campaign targeting users free during peak hours, encouraging them to increase their daily step count. Additionally, consider adding easy workout tutorials on the smartwatch app to guide less active users in exercising.


![Image](https://github.com/user-attachments/assets/a94e9b18-50bc-43e1-935b-6e866eda585d)


<h2>Recommendation</h2>

I recommend fully automating step recording to ensure accurate, continuous tracking without manual input, improving user experience and data accuracy. I also recommend prompting users to provide key demographic information, such as age, fitness level, occupation, family size, marital status, and income/education, to personalize their experience and offer tailored fitness recommendations. Finally, I recommend encouraging users to set personalized fitness goals and allowing them to update these goals as their progress and fitness levels change, which will increase motivation, engagement, and long-term retention.

PowerPoint presentation [link](https://1drv.ms/p/c/e62f58aaa73df5d9/EQyPaGoATo1HrjxVRm43ADgBRVttRgKUz98Yo7OAs9FnVg?e=7hUOjO).
