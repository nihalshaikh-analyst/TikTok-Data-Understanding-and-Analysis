# Statistical Analysis of TikTok

This project uses a dataset called tiktok_dataset.csv. It contains synthetic data created for this project in partnership with TikTok. Data analyze, clean, process, data analysis by using Python and its **Library pandas, numpy, matplotlib.pyplot** and **seaborn** and **A/B testing, hypothesis testing** with presentation in Jupyter Notebook

![tiktok1](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tiktok1.png)
![tiktok](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tIktok.png)


## Project Overview

**The TikTok data team seeks to develop a machine learning model to assist in the classification of claims for user submissions. In this part of the project, the data team will conduct a hypothesis test to analyze the relationship between verified_status and video_view_count.**


## Project background

**TikTok’s data team is working on the claims classification project. The following tasks are needed at this stage of the project:**

- Explore the project data

- Implement a hypothesis test

- Communicate insights with stakeholders within TikTok


[Dataset](https://github.com/nihalshaikh-analyst/TikTok-Data-Understanding-and-Analysis/blob/main/tiktok_dataset.csv)



## Specific project deliverables

- Strategy Document to consider questions, details, and action items for each stage of the project scenario

- Answer the questions in the Jupyter notebook project file

- Consider the different groups of data represented in the dataset

- Implement a hypothesis test

- Create an executive summary to share your results


## Jupyter Notebook

[Notebook](https://github.com/nihalshaikh-analyst/TikTok-Data-Understsnding-EDA-Statistical-Regression-ML-Models/blob/main/Statistical%20Analysis%20of%20TikTok.ipynb)


## Storytelling and Problem Solving

#### Details

- The TikTok data team considered the relationship between verified_status and video_view_count.
  
- One approach conducted was to examine the mean values of video_view_count for each group of verified_status in the sample data. The findings showed that unverified accounts have a mean of 265,663 views vs. 91,439 views for verified accounts


- The second approach was a two-sample hypothesis test. Aligned with preliminary findings from the mean values, this statistical analysis shows that any observed difference in the sample data is due to an actual difference in the corresponding population means.


[Presentations](https://github.com/nihalshaikh-analyst/TikTok-Data-Understsnding-EDA-Statistical-Regression-ML-Models/blob/main/Statistics%20of%20TikTok%20Findings.pptx)


![presentation](https://github.com/nihalshaikh-analyst/TikTok-Data-Understsnding-EDA-Statistical-Regression-ML-Models/blob/main/Statistics%20of%20TikTok%20Presentation.png)


## Insights

- The analysis shows that there is a difference in number of views between TikTok videos posted by verified accounts and TikTok videos posted by unverified accounts. 

- As a result, these findings suggest there might be fundamental behavioral differences between these two groups of accounts: verified and unverified. 

- It would be interesting to investigate the root cause of this behavioral difference. For example, consider: 

- Do unverified accounts tend to post more engaging videos? Is that engaging content a claim or opinion? 

- Or, are unverified accounts associated with spam bots that help inflate view counts?


## Next Step

#### The team suggests moving forward and building a regression model on verified status. 

#### A regression model for verified_status can help analyze user behavior in this group of verified users. Then, this context can be used to consider results from a claim classification model that will be created afterwards.


## Step by Step Process

-  Imports and data loading

-  Conduct hypothesis testing

-  Communicate insights with stakeholders

-  1. Imports and Data Loading
Import packages and libraries needed to compute descriptive statistics and conduct a hypothesis test.

- Load the dataset.

-  2. Data exploration
Use descriptive statistics to conduct Exploratory Data Analysis (EDA).

- Inspect the first five rows of the dataframe.

-  3. Hypothesis testing
 
- Null hypothesis: There is no difference in number of views between TikTok videos posted by verified accounts and TikTok videos posted by unverified accounts (any observed difference in the sample data is due to chance or sampling variability).

- Alternative hypothesis: There is a difference in number of views between TikTok videos posted by verified accounts and TikTok videos posted by unverified accounts (any observed difference in the sample data is due to an actual difference in the corresponding population means).

- State the null hypothesis and the alternative hypothesis

- Choose a signficance level

- Find the p-value

- Reject or fail to reject the null hypothesis

- 𝐻0
 : There is no difference in number of views between TikTok videos posted by verified accounts and TikTok videos posted by unverified accounts (any observed difference in the sample data is due to chance or sampling variability).

- 𝐻𝐴
: There is a difference in number of views between TikTok videos posted by verified accounts and TikTok videos posted by unverified accounts (any observed difference in the sample data is due to an actual difference in the corresponding population means).

- 4. Communicate insights with stakeholders

- The analysis shows that there is a statistically significant difference in the average view counts between videos from verified accounts and videos from unverified accounts. This suggests there might be fundamental behavioral differences between these two groups of accounts.

- It would be interesting to investigate the root cause of this behavioral difference. For example, do unverified accounts tend to post more clickbait-y videos? Or are unverified accounts associated with spam bots that help inflate view counts?

- The next step will be to build a regression model on verified_status. A regression model is the natural next step because the end goal is to make predictions on claim status. A regression model for verified_status can help analyze user behavior in this group of verified users. Technical note to prepare regression model: because the data is skewed, and there is a significant difference in account types, it will be key to build a logistic regression model.



Any query connect nihalshaikh.analyst@gmail.com


--------------Thank you................
