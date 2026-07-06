# journ-124-final-project
Final project for JOURN 124 exploring AI hallucination legal cases.

# 1. Headline


# 2. Dataset Origins and Challenges
For this final project, I will be using [Damien Charlotin's](https://www.damiencharlotin.com/) [AI Hallucination Cases](https://www.damiencharlotin.com/hallucinations/) dataset. This is a dataset which lists legal cases in which an AI tool was used that gave inaccurate information, also known as an AI hallucination. For context of the creator, Damien Charlton works for a firm called Pelekan Data Consulting, where he focuses on collecting data focusing on technology legal cases. He also writes articles on [Artificial Authority](https://artificialauthority.ai/) where he focused on AI and Law. It appears that he created the dataset that I'm analyzing as a tool and reference to use in both his own works and for other people to access publicly. 

This dataset immediately caught my attention as I am extremely interested in how AI is monitored legally. I am a double major in History and Data Science, and am looking to potentially pursue this kind of law after graduation. Thus, when browsing datasets on [Data is Plural](https://www.data-is-plural.com/archive/), this dataset seemed very interesting to me, and I wanted to look into it more.

One major challenge with this dataset is that it is limited in sample size. There are only about 1,700 cases/entries listed as AI law is a very new topic with its recent developments. This is very small compared to other legal data sets that have millions of entries. Additionally, after looking through the provided columns, there is one called "AI Tool" which lists which AI tool presumably made a hallucination. For many of these cases, they were unable to identify what exact AI tool produced a hallucination which makes it difficult to compare different models and the rates at which they hallucinate.

# 3. Data Analysis
<img width="1512" height="799" alt="dataset" src="https://github.com/user-attachments/assets/8b36698d-8bc6-42dc-8890-51d6e443ffe1" />
To begin my data analysis of this set, I attached an image of what it looks like above, and it can also be found [here](https://docs.google.com/spreadsheets/d/14EoyyOJZCJLSAXDNNxF7_i3rH7IV8uqt0tEKWIB0sq4/edit?gid=78572351#gid=78572351). Each entry is a court case with columns such as the name, location, parties involved, dates, and AI involved.

<img width="1512" height="799" alt="pivot1" src="https://github.com/user-attachments/assets/86982153-d79f-46d4-bda2-63de79b44e61" />
I was first interested in location and wanted to see if there were any trends in the number of cases by locations. With this in mind, I created a pivot table with the rows as "State(s)" and the count per state for the value, attaching an image of the table above. I then sorted this by descending counts, finding that the USA has the highest number (1,187) of cases by far. This is likely because of the presence of many AI companies in the US as well as Silicon Valley.

<img width="1512" height="799" alt="pivot2" src="https://github.com/user-attachments/assets/187a6378-3b14-4531-9cf4-d47a14f28ca4" />
Next, I was interested in seeing which AI tool tended to hallucinate the much, so I followed the same pivot strategy as before but with the "AI Tool" column which can be seen in the image above. I found that most cases had an "Implied" AI tool, meaning the presence of AI usage is debated in the case. Next is "Unidentified" which shows that these cases were proven to have used AI, but could not identify which tool was used. The next entry is an actual tool, which is "ChatGPT." I want to note that this is limited in the fact that it does not specify what version/model of Chat GPT was used.

<img width="1512" height="799" alt="pivot3" src="https://github.com/user-attachments/assets/561aaed9-5eb3-426c-ad17-b9b65a86c7b5" />
I was then interested in seeing if there were trends in what courts are overseeing these cases, following the same approach with the count as before applied to the "Court" column. I found that the top two were S.D. New York and SC New York, which is interesting that they are both in the same state. 

<img width="1512" height="799" alt="pivot4" src="https://github.com/user-attachments/assets/6457bad8-98a1-4aa6-b29d-a8ab3011c5bc" />


# 4. Data Visualizations

# 5. Ending Summary, Ethical Concerns, Reporting Process
