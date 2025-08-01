# TikTok-Data-Understanding-and-Analysis
This project uses a dataset called tiktok_dataset.csv. It contains synthetic data created for this project in partnership with TikTok.  Data analyze, clean, process, data analysis by using Python and its Library pandas and numpy with presentation in Jupyter Notebook. 

![tiktok](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tIktok.png)

## TikTok users have the ability to submit reports that identify videos and comments that contain user claims. These reports identify content that needs to be reviewed by moderators. The process generates a large number of user reports that are challenging to consider in a timely manner. 

## Background on the TikTok scenario

TikTok users have the ability to submit reports that identify videos and comments that contain user claims. These reports identify content that needs to be reviewed by moderators. The process generates a large number of user reports that are challenging to consider in a timely manner. 

TikTok is working on the development of a predictive model that can determine whether a video contains a claim or offers an opinion. With a successful prediction model, TikTok can reduce the backlog of user reports and prioritize them more efficiently.

[TikTok Dataset](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tiktok_dataset.csv)



## Team members at TikTok

**Data team roles**
- Willow Jaffey- Data Science Lead

- Rosie Mae Bradshaw- Data Science Manager

- Orion Rainier- Data Scientist

The members of the data team at TikTok are well versed in data analysis and data science. Messages to these more technical coworkers should be concise and specific.

**Cross-functional team members**
- Mary Joanna Rodgers- Project Management Officer

- Margery Adebowale- Finance Lead, Americas

- Maika Abadi- Operations Lead

Note: The story, all names, characters, and incidents portrayed in this project are fictitious. No identification with actual persons (living or deceased) is intended or should be inferred. And, the data shared in this project has been created for pedagogical purposes. 


## Data dictionary

This project uses a dataset called tiktok_dataset.csv. It contains synthetic data created for this project in partnership with TikTok. 

The dataset contains: 

19,383 rows – Each row represents a different published TikTok video in which a claim/opinion has been made.


## Project background

TikTok’s data team is in the earliest stages of the claims classification project. The following tasks are needed before the team can begin the data analysis process:

- Build a dataframe for the TikTok dataset

- Examine data type of each column

- Gather descriptive statistics


## Project background


TikTok’s data team is in the earliest stages of the claims classification project. The following tasks are needed before the team can begin the data analysis process:

- Build a dataframe for the TikTok dataset

- Examine data type of each column

- Gather descriptive statistics


## Specific project deliverables
 

- Answer the questions in the Jupyter notebook project file

- Complete coding prep work on project’s Jupyter notebook

- Summarize the column Dtypes

- Communicate important findings in the form of an executive summary  

- TikTok's data team needs you to problem-solve and communicate your findings. Good luck on tasks!


## Step by Step Process


**1. Understand the situation**

**2. Understand the data**

**3. Understand the variables**

- Prepare by reading in the data, viewing the data dictionary, and exploring the dataset to identify key variables for the stakeholder.

- Start by importing the packages that you will need to load and explore the dataset. Make sure to use the following import statements:

- Then, load the dataset into a dataframe. Creating a dataframe will help you conduct data manipulation, exploratory data analysis (EDA),   and statistical activities.
 
- View and inspect summary information about the dataframe by coding the following:

data.head(10)
data.info()
data.describe()

- The dataframe contains a collection of categorical, text, and numerical data. Each row represents a distinct TikTok video that presents   either a claim or an opinion and the accompanying metadata about that video.
 
- The dataframe contains five float64s, three int64s, and four objects. There are 19,382 observations, but some of the variables are        missing values, including claim status, the video transcripton, and all of the count variables.

- Many of the count variables seem to have outliers at the high end of the distribution. They have very large standard deviations and       maximum values that are very high compared to their quartile values.

- The counts of each claim status are quite balanced.

Next, examine the engagement trends associated with each different claim status.

- Start by using Boolean masking to filter the data according to claim status, then calculate the mean and median view counts for each      claim status.

- The mean and the median within each claim category are close to one another, but there is a vast discrepancy between view counts for      videos labeled as claims and videos labeled as opinions.

Now, examine trends associated with the ban status of the author.

- Use groupby() to calculate how many videos there are for each combination of categories of claim status and author ban status.

There are many more claim videos with banned authors than there are opinion videos with banned authors. This could mean a number of things, including the possibilities that:

- Claim videos are more strictly policed than opinion videos
  
- Authors must comply with a stricter set of rules if they post a claim than if they post an opinion
  
- Also, it should be noted that there's no way of knowing if claim videos are inherently more likely than opinion videos to result in       author bans, or if authors who post claim videos are more likely to post videos that violate terms of service.

Finally, while you can use this data to draw conclusions about banned/active authors, you cannot draw conclusions about banned videos. There's no way of determining whether a particular video caused the ban, and banned authors could have posted videos that complied with the terms of service.

- Continue investigating engagement levels, now focusing on author_ban_status.

- Calculate the median video share count of each author ban status.

A few observations stand out:

- Banned authors and those under review get far more views, likes, and shares than active authors.
  
- In most groups, the mean is much greater than the median, which indicates that there are some videos with very high engagement counts.
  
Now, create three new columns to help better understand engagement rates:

- likes_per_view: represents the number of likes divided by the number of views for each video
  
- comments_per_view: represents the number of comments divided by the number of views for each video
  
- shares_per_view: represents the number of shares divided by the number of views for each video

- Use groupby() to compile the information in each of the three newly created columns for each combination of categories of claim status    and author ban status, then use agg() to calculate the count, the mean, and the median of each group.

- We know that videos by banned authors and those under review tend to get far more views, likes, and shares than videos by non-banned      authors. However, when a video does get viewed, its engagement rate is less related to author ban status and more related to its claim    status.

Also, we know that claim videos have a higher view rate than opinion videos, but this tells us that claim videos also have a higher rate of likes on average, so they are more favorably received as well. Furthermore, they receive more engagement via comments and shares than opinion videos.

Note that for claim videos, banned authors have slightly higher likes/view and shares/view rates than active authors or those under review. However, for opinion videos, active authors and those under review both get higher engagement rates than banned authors in all categories.

- Of the 19,382 samples in this dataset, just under 50% are claims—9,608 of them.

- Engagement level is strongly correlated with claim status. This should be a focus of further inquiry.

- Videos with banned authors have significantly higher engagement than videos with active authors. Videos with authors under review fall    between these two categories in terms of engagement levels.



## UNDERSTANDING THE DATA

After reviewing the provided dataset, the variable  claim_status seemed particularly useful, given the client’s proposed project. The following screenshots show important points of analysis required to understand the claim_status variable.

<img width="474" height="146" alt="image" src="https://github.com/user-attachments/assets/4244291f-19d1-4c66-ac07-1c96e3166dee" />

Note: The counts of each claim status are quite balanced. There are 9,608 claims and 9,476 opinions.

## ENGAGEMENT TRENDS

**The data team considered viewer engagement with each video in the claim and opinion categories. In order to understand viewer engagement, the data team considered the view count. The mean and median view count show the impact of each category of video; specifically, the mean and median view counts for both categories show the association between content (claim or opinion) and the video views.**

Claims:
Mean view count claims: 501029.4527477102
Median view count claims: 501555.0

Opinions:
Mean view count opinions: 4956.43224989447
Median view count opinions: 4953.0


## Storytelling, Findings and Presentation

[Presentation](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/TikTok-Insights%20and%20Findings.pptx)


![Tiktok Presentation](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/Tiktok%20Presentation.png)


## Insights

**- There is a near equal balance of opinions versus claims. With this understanding, we can proceed with our future analysis knowing         that there is a fairly balanced amount of claims and opinions for the videos included within this dataset.**

**- With the key variables identified and the initial investigation of the claims classification dataset, the process of exploratory data     analysis can begin.**

Pie chart visualizes the comparison of the count of claims and opinions


<img width="282" height="371" alt="image" src="https://github.com/user-attachments/assets/93761976-9308-4110-8777-0ae71c66b298" />



## Responce

- The data team performed a preliminary investigation of the claims classification dataset with the aim of learning important               relationships between variables.

- Given the ask for a classification of user claims, the data team looked at the counts of claims and opinions in order to understand the   count of each type of video content.


## Impact

**"The impact of this preliminary analysis will be evident in the next steps. In order to understand the impact of user videos, the data team identified two important variables to consider. The variables  video_duration (in seconds) and video_view_count are both important factors to consider for future prediction models."**


## Issue/ Problem


**"The TikTok data team seeks to develop a machine learning model to assist in the classification of claims for user submissions. To begin, the data team needs to organize the raw dataset and prepare it for future exploratory data analysis."**



"Any concerns contact to us  nihalshaikh.analyst@gmail.com


-------Thank you........




