# journ-124-final-project
Final project for JOURN 124 exploring AI hallucination legal cases.

# 1. Headline
The number of AI hallucination legal cases have increased by 150% in the past year according to Damien Charlotin's dataset, making it hard to discern what is real and what is not.


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
Last but not least, I looked into what parties were involved in these cases by making a count pivot on the "Party(ies)" column, finding the majority was "Pro Se Litigant." This means that most parties were representing themselves which I thought was a very interesting ocurrance.


# 4. Data Visualizations
<img width="1512" height="799" alt="Screenshot 2026-07-05 at 11 34 14 PM" src="https://github.com/user-attachments/assets/447c5835-4b6f-4167-a79e-58f9395aadc8" />
After getting a good idea of patterns in the data and understanding the content of the dataset, I wanted to make visualizations to see a timeline of cases over time. To do this, I added a new column to the dataset called "Month" to get the month of each entry by using `=IF(D2="", "", DATE(YEAR(D2), MONTH(D2), 1))`. This can be seen in the image above.


<img width="1512" height="799" alt="Screenshot 2026-07-05 at 11 46 06 PM" src="https://github.com/user-attachments/assets/5e821a2e-0532-47f7-b19f-51db6dc27338" />
I then created a pivot table with the rows as the "Month" column ascending and the "Case Name" sum as the values. With this, I created a line chart to visualize a timeline of how many court cases ocurred each month. As seen in the image above, there is a clear increase in AI hallucination cases over the past few months, but a sharp decline in the past month. This increase makes sense as AI has become more normalized in everyday life in the past year. 


<img width="1512" height="799" alt="Screenshot 2026-07-05 at 11 49 36 PM" src="https://github.com/user-attachments/assets/ecd7f09c-6669-4830-b87d-71f2f390bdac" />
I then wanted to look closer at the specific AI tools again to see if a visualization would help show a better view of the top three groups, and made a bar chart off of the top three entries from my previous pivot table. Clearing, there is a great difference between cases using Chat GPT, unidentified tools, and implied AI usage. They appear to have increased by over 150% in the past year. This shows the urgency of this issue as it is very hard to tell what was created by AI and what wasn't, and who's at fault in each case.


# 5. Ending Summary, Ethical Concerns, Reporting Process
Ultimately, from this analysis I found that there is a great increase over the past year in AI hallucination legal cases. It is hard to determine what AI was used to create false information, and if it was even present, making this an urgent issue. This is likely because as AI is trainined, it gets better with every model. This makes it more difficult to see the difference between human made content and AI generated content, making hallucinations more likely to pass into media and public works. However, it is extremely important to recognize how limited this dataset is with under 2,000 entries as this is a very new issue. More entries would be needed to make this a more ethical and stronger dataset.
