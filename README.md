# Accenture Data Analytics and Visualization Virtual Experience - Social Buzz Content Analysis 
<img align="right" alt="Social Buzz Content Analysis" width="1000" height = "500" src="https://user-images.githubusercontent.com/106287208/211251283-a22c9ae7-83ce-4196-acd6-0c2e1bf96eff.png">

---


# Table of Contents

- [Problem Statement](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Problem-Statement)
- [Data Sourcing](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Data-Sourcing)
- [Data Preparation](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Data-Preparation)
- [Data Modeling](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Data-Modeling)
- [Data Visualization and Analysis](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Data-Visualization)
- [Insight](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Insight)
- [Recommendation](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Recommendation)
- [Shareable link](https://github.com/globalsmile/Accenture-Data-Analytics-and-Visualization-Virtual-Experience-Social-Buzz-Content-Analysis#Shareable-Link)


---

# Problem Statement

Social Buzz was founded by two former engineers from a large social media conglomerate, one 
from London and the other from San Francisco. They left in 2008 and both met in San 
Francisco to start their business. They started Social Buzz because they saw an opportunity to 
build on the foundation that their previous company started by creating a new platform where 
content took center stage. Social Buzz emphasizes content by keeping all users anonymous, 
only tracking user reactions on every piece of content. There are over 100 ways that users can 
react to content, spanning beyond the traditional reactions of likes, dislikes, and comments. 
This ensures that trending content, as opposed to individual users, is at the forefront of user 
feeds. 
Over the past 5 years, Social Buzz has reached over 500 million active users each month. 
They have scaled quicker than anticipated and need the help of an advisory firm to oversee 
their scaling process effectively. 
Due to their rapid growth and digital nature of their core product, the amount of data that they 
create, collect and must analyze is huge. Every day over 100,000 pieces of content, ranging 
from text, images, videos and GIFs are posted. All of this data is highly unstructured and 
requires extremely sophisticated and expensive technology to manage and maintain. Out of the 
250 people working at Social Buzz, 200 of them are technical staff working on maintaining this 
highly complex technology.

The purpose of this analysis is to highlight the top 5 content categories with the largest aggregate popularity.

---

# Data Sourcing

The Dataset used for this analysis was provided by [Accenture](https://www.theforage.com/fast-track/data-analytics-virtual-experience/overview) and is available at:

- [Social media buzz datasets](https://drive.google.com/drive/folders/11ClQl1UeFOM8Tan19OXmh1_AIJkUfUu_?usp=share_link)

---

# Data Preparation

Data cleaning and transformation was done in Microsoft Excel and the datasets were loaded into Microsoft Power BI Desktop for modeling and visualization.

There are seven datasets for this project.:

- User
- Profile
- Location
- Session
- Content
- Reaction
- ReactionTypes

The data dictionary containing the features of the data can be found below:

- `User`

| Fields | Description |
| ----------- | ----------- |
| ID | Unique ID of the user (automatically generated) |
| Name | Full name of user |
| Email | Email address of user |

- `Profile`

| Fields | Description |
| ----------- | ----------- |
| User ID | Unique ID of a user that exists in the User table |
| Interests | Interests of the associated user |
| Age | Age of the associated user |


- `Location`

| Fields | Description |
| ----------- | ----------- |
| User ID | Unique ID of a user that exists in the User table |
| Address | Full address of the user |


- `Session`

| Fields | Description |
| ----------- | ----------- |
| User ID | Unique ID of a user that exists in the User table |
| Device | Mobile device that they used for this session on the application |
| Duration | Amount of time in minutes that this user stayed active on the application during this session |

- `Content`

| Fields | Description |
| ----------- | ----------- |
| ID | Unique ID of a user that was uploaded (automatically generated) |
| User ID | Unique ID of a user that exists in the User table |
| Type | A string detailing the type of content that was uploaded |
| Category | A string detailing the category that this content is relevant to |
| URL | Link to the location where this content is stored |


- `Reaction`

| Fields | Description |
| ----------- | ----------- |
| Content ID | Unique ID of a piece of content that was uploaded |
| User ID | Unique ID of a user that exists in the User table |
| Type | A string detailing the type of reaction this user gave |
| Datetime | The date aand time of this reaction |


- `ReactionTypes`

| Fields | Description |
| ----------- | ----------- |
| Type | A string detailing the type of reaction this user gave |
| Sentiment | A string detailing whether this type of reaction is considered as positive negative or neutral |
| Score | This is a number calculated by Social Buzz that quantifies how "popular" each reaction is. A reaction type with a higher score should be considered as a more popular reaction |


The `Reaction` dataset was checked for duplicates, invalid entries, missing values, incorrect data types and issues from data entry.

For numeric columns that had null values, I replaced them with ‘0’. No duplicates were found, and incorrect column data types were 
changed to the appropriate data types, e.g. datetime column having an alphanumeric data type was changed to date and time data types . 
The same process was repeated for all 6 remaining datasets to ensure accuracy in analysis.

---

# Data Modeling

After the dataset was cleaned and transformed, it was ready to be modeled(using Power BI Desktop).


The relationship formed in the data model is shown below:

<img align="right" alt="Data Model" width="1000" height = "400" src="https://user-images.githubusercontent.com/106287208/211252573-a49a496d-14ab-43e1-866b-fd2018c3f509.png">



---

# Data Visualization and Analysis

- The analysis aimed to highlight the top 5  categories of content with the largest aggregate popularity.

To achieve this set goal:-

I created a visualization showing the top 5 categories of content. Animals and science are the two most popular categories of content with over 75k and 71k posts respectively showing that people enjoy “real-life” and “factual” content the most.

![image](https://user-images.githubusercontent.com/106287208/211252846-a8c58d44-fe42-4600-8177-d5153a25cf0d.png)


- Food had an aggregate popularity score of almost 67000. It is very interesting to see both food and cooking within the top 5, it really shows what people enjoy consuming as content. But also, interesting to see culture too. Clearly users favor “real-life” content on this platform.

![image](https://user-images.githubusercontent.com/106287208/211252975-dca549c6-f72f-425a-a2bb-deb94a5cb861.png)


- Furthermore, soccer is an interesting category because there is the European championships being played very soon. This presents a huge opportunity for you to differentiate your platform and to run specific content or events linked to this global spectacle.

---

# Insight

From the data we found that you had a total of 16 unique categories of posts across from datasets. This includes things such as Food, Culture and Sport.
As well as this, there was 1897 posts from just the Animal category alone! People obviously really like real-life content!
And, the most common month for users to post within was january with over 2141 posts, this such a seasonal month with so many holidays 
and events, this is interesting to know that people are most active during this month!

![image](https://user-images.githubusercontent.com/106287208/211253743-a732c675-7eb5-4f58-ab6c-f8efb75535f9.png)


Food is a common theme with the top 5 categories with “Healthy Eating” ranking the highest. This may give an indication to the audience within your userbase.
You could use this insight to create a campaign and work with healthy eating brands to boost user engagement.


---

# Recommendation

This ad-hoc analysis is insightful, but it’s time to take this analysis int large scale production for realtime understanding of your business. I can show you how to do this

---

# Shareable Link

You can interact with the report here: 

[View Report](https://app.powerbi.com/view?r=eyJrIjoiZTYyYTM0YmItYzgxNS00ZjAyLWE0MjItZjBkM2Y5NjZhMjRjIiwidCI6IjQ5ODY4YWYzLWNjNWYtNDIxNC04YjdmLTQwZjM3NDY0OWEwOSJ9)
