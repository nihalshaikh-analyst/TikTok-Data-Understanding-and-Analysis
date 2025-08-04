# Exploratory Data Analysis (EDA) of TikTok Data

This project uses a dataset called tiktok_dataset.csv. It contains synthetic data created for this project in partnership with TikTok. Data analyze, clean, process, data analysis by using Python and its Library **pandas, numpy, matplotlib.pyplot and seaborn** with presentation in Jupyter Notebook


![tiktok1](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tiktok1.png)
![tiktok](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tIktok.png)


## Project Overview

**The purpose of this project is to conduct exploratory data analysis on a provided data set. Your mission is to continue the investigation you began in C2 and perform further EDA on this data with the aim of learning more about the variables. Of particular interest is information related to what distinguishes claim videos from opinion videos.**

## Project background

TikTok’s data team is working on the claims classification project.

- EDA and cleaning.

- Select and build visualization(s) type.

- Create plots to visualize variables and relationships between variables.

- Share your results with the TikTok team.

[Dataset](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tiktok_dataset.csv)


## Specific project deliverables

- Strategy Document to consider questions, details, and action items for each stage of the project scenario

- Answer the questions in the Jupyter notebook project file

- Clean your data, perform exploratory data analysis (EDA)

- Create data visualizations

- Create an executive summary to share your results


## Step by Step EDA Process

- Imports, links, and loading

- Data Exploration
  
- Data cleaning

- Build visualizations

- Evaluate and share results

- For EDA of the data, import the packages that would be most helpful, such as pandas, numpy, matplotlib.pyplot, and seaborn.

- Then, load the dataset into a dataframe. Read in the data and store it as a dataframe object.

- Consider functions that help you understand and structure the data.

.head()

.info()

.describe() 

.groupby() 

.sort_values()

- Select data visualization types that will help you understand and explain the data.

Line chart

Box plot

Histogram

Heat map

Scatt graph

Bar cer plot

A geographic map


- The visualizations most helpful for considering the distribution of the data include box plots and histograms. Visualizing the distribution of the data can inform the next steps and considerations in data analysis. For example, data distribution will inform which types of modeling is needed.

- Now that you have assessed your data, it’s time to plot your visualization(s).

- Create a box plot to examine the spread of values in the `video_duration_sec` column.

- Create a histogram of the values in the `video_duration_sec` column to further explore the distribution of this variable.

- All videos are 5-60 seconds in length, and the distribution is uniform.

- Create a box plot to examine the spread of values in the `video_view_count` column.

- Create a histogram of the values in the `video_view_count` column to further explore the distribution of this variable.

- This variable has a very uneven distribution, with more than half the videos receiving fewer than 100,000 views. Distribution of view counts > 100,000 views is uniform.

- Create a box plot to examine the spread of values in the `video_like_count` column.

- Create a histogram of the values in the `video_like_count` column to further explore the distribution of this variable.

- Similar to view count, there are far more videos with < 100,000 likes than there are videos with more. However, in this case, there is more of a taper, as the data skews right, with many videos at the upper extremity of like count.

- Create a box plot to examine the spread of values in the `video_comment_count` column.

- Create a histogram of the values in the `video_comment_count` column to further explore the distribution of this variable.

- Again, the vast majority of videos are grouped at the bottom of the range of values for video comment count. Most videos have fewer than 100 comments. The distribution is very right-skewed.

- Create a box plot to examine the spread of values in the `video_share_count` column.

- Create a histogram of the values in the `video_share_count` column to further explore the distribution of this variable.

- The overwhelming majority of videos had fewer than 10,000 shares. The distribution is very skewed to the right.

- Create a box plot to examine the spread of values in the `video_download_count` column.

- Create a histogram of the values in the `video_download_count` column to further explore the distribution of this variable.

- The majority of videos were downloaded fewer than 500 times, but some were downloaded over 12,000 times. Again, the data is very skewed to the right.

- Now, create a histogram with four bars: one for each combination of claim status and verification status.

- There are far fewer verified users than unverified users, but if a user *is* verified, they are much more likely to post opinions.

- The previous course used a `groupby()` statement to examine the count of each claim status for each author ban status. Now, use a histogram to communicate the same information.

- For both claims and opinions, there are many more active authors than banned authors or authors under review; however, the proportion of active authors is far greater for opinion videos than for claim videos. Again, it seems that authors who post claim videos are more likely to come under review and/or get banned.

- Create a bar plot with three bars: one for each author ban status. The height of each bar should correspond with the median number of views for all videos with that author ban status.

- The median view counts for non-active authors are many times greater than the median view count for active authors. Since you know that non-active authors are more likely to post claims, and that videos by non-active authors get far more views on aggregate than videos by active authors, then `video_view_count` might be a good indicator of claim status.

- Create a pie graph that depicts the proportions of total views for claim videos and total views for opinion videos.

- The overall view count is dominated by claim videos even though there are roughly the same number of each video in the dataset.

- Write a for loop that iterates over the column names of each count variable. For each iteration:
1. Calculate the IQR of the column
2. Calculate the median of the column
3. Calculate the outlier threshold (median + 1.5 * IQR)
4. Calculate the numer of videos with a count in that column that exceeds the outlier threshold
5. Print "Number of outliers, {column name}: {outlier count}"




## Jupyter Notebook

[Notebook](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/EDA%20of%20TikTok.ipynb)


**EDA is important because ...**
**EDA helps a data professional to get to know the data, understand its outliers, clean its missing values, and prepare it for future modeling.**
**Visualizations helped me understand ..**
**That we will need to make decisions on certain considerations prior to designing a model. (for example, what to do with outliers, duplicate values, or missing data)**


## Storytelling and Problem Solveing

**A key component of this project’s exploratory data analysis involves visualizing the data. As illustrated in the following histograms, it is clear that the vast majority of videos are grouped at the bottom of the range of values for three variables that showcase TikTok users (video viewers’) engagement with the videos included in this dataset.**

![TikTok EDA Presentation](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/TikTok%20EDA%20Presentation.png)


## Response

**The TikTok data team conducted exploratory data analysis at this stage. The purpose of the exploratory data analysis was to understand the impact that videos have on TikTok users. To do so, the TikTok data team analyzed variables that would showcase user engagement: view, like, and comment count.**


<img width="365" height="217" alt="image" src="https://github.com/user-attachments/assets/6dac727e-ae72-4c27-984b-234714bcfcb0" />

The view count variable has a very uneven distribution, with more than half the videos receiving fewer than 100,000 views. Distribution of view counts > 100,000 views is uniform.


<img width="341" height="253" alt="image" src="https://github.com/user-attachments/assets/ff140bdc-4698-4886-9204-aa68c62bf885" />

Similar to view count, there are far more videos with < 100,000 likes than there are videos with more. 
<img width="955" height="45" alt="image" src="https://github.com/user-attachments/assets/d1b3d1d2-279c-4244-a3f4-406daed02cbc" />

<img width="424" height="253" alt="image" src="https://github.com/user-attachments/assets/63370dfe-e80b-4ab6-a38f-a432dd887a7c" />

Again, the vast majority of videos are grouped at the bottom of the range of values for video comment count. Most videos have fewer than 100 comments. The distribution is very right-skewed.
<img width="1776" height="45" alt="image" src="https://github.com/user-attachments/assets/3171bb66-6788-45d3-925d-2bc23fd0aa81" />



## Impact

**"According to the findings from the exploratory data analysis, the future claim classification model will need to account for null values and imbalance in opinion video counts by incorporating them into the model parameters."**


## Issue / Problem

**"The TikTok data team seeks to develop a machine learning model to assist in the classification of claims for user submissions. In this part of the project, the data needs to be analyzed, explored, cleaned, and structured prior to any model building."**
<img width="2737" height="53" alt="image" src="https://github.com/user-attachments/assets/10a9a7a1-cd99-45f5-8ab8-6714fc0484ec" />

