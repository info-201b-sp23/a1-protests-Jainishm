# Assignment 1: Protests

During the past few years in the United States, there has been a surge of protests in support of the Black Lives Matter movement, women's rights, trans rights, immigration reform, gun control, the environment, and many other social and political issues.

In this assignment, you will work with data from [CountLove](https://countlove.org/), a group that collects data about protests from across the United States, including information about the purpose of the protests, the location of the protests, as well as how many people attended the protests. This data has often been [cited by the *New York Times*](https://www.nytimes.com/2020/08/28/us/black-lives-matter-protest.html), among other major outlets.

Through this assignment, you will be able to answer questions including:
- What were the most attended and least attended protests in the US in the last 5 years?
- How many protests occurred in Washington state?
- How did the number of protests in 2019 compare to 2020, and why?
- Why are people protesting in the US? What are the biggest motivators?


This assignment is divided into 2 parts. You will complete your coding work in the `analysis.R` file, and you will write short answer responses related to critical analysis and reflection of the data in this `README.md` file. Before getting started on your coding work, you should complete the section **"Critical Analysis & Reflection: Before You Code"** below.

When you are finished with the assignment, be sure to push all changes to your GitHub repository and then submit the link on Canvas.

## Before You Code: Critical Analysis & Reflection

Before diving into this (or any) dataset, it's important to know where the data came from, and it's important to have or to seek out _domain familiarity_ — in other words, knowledge about the subject/topic of the dataset. (We don't want to be "strangers in the dataset," as Catherine D'Ignazio and Lauren Klein describe it.)

To get more familiar, we are going to begin by doing some background reading.

- First, please read [this FAQ](https://countlove.org/faq.html) from the CountLove website and the opening of [this blog post](https://www.tommyleung.com/countLove/index.htm). Based on the information in these pieces, why did the creators start collecting the CountLove data? Please answer in 2-3 sentences (3 points)
 - Answer: Creators started collecting CountLove data so there is a better way to communicate with our elected leaders. Apart from this, CountLove was started by two young engineers who have a passion and interest in civic responsibility and public policy and hence CountLove was started. All in all, the creators passion for data collection and poilical and public causes have led to the creation of CountLove.  

- Next, we would like you to read this [*New York Times* piece, which uses CountLove data](https://www.nytimes.com/interactive/2020/06/13/us/george-floyd-protests-cities-photos.html) (here's a [Google Doc version for anyone who gets paywalled](https://docs.google.com/document/d/1sdjFsA5csYuH4plNEEk7WXT77K5h5ZuyW05CBwYdk6A/edit?usp=sharing)), and which describes the Black Lives Matter protests that occurred in the summer of 2020. Please summarize the main point or argument of this article in 2-3 sentences (3 points)
 - Answer: The main subject in this article is how the Black Lives Matter movement spread across the United States. There were chants, prayers, singing to demonstrate support towards the movement. These peaceful protests were souly fueled by the fact that the peoples's voices should be heard. All in all, the protests whether violent or peaceful were to spread hte message that Black Lives Matter. The statistics and data in the graphs show how rapid the growth and the movement on a whole was. 

Next, we're going to reflect about who collected this data, and what's actually inside it.

- Who collected and shared the CountLove data, and what do they do for a living? Please answer in 1-2 sentences(2 points)
 - Answer: Tommy Leung and Nathan Perkins are the two people who collect and share CountLove data. They are engineers and scientists who have a keen interest in civic responsibility and public policy. 

- As Klein and D'Ignazio remind us, when it comes to data, "what gets counted counts." What types of demonstrations does CountLove include in their data, and what types do they exclude? (3 points)
 - Answer: CountLove counts publicdisplays of protest that are not part of regular business. By "regular business" they imply that any data that relates to awareness events, commemorative celebrations, historic reenactments, fundraising events, townhalls, or poilitical campaign rallies is not projected in CountLove data. 

- How and where does CountLove get their data about the protests? Please answer in 2-3 sentences (2 points)
 - Answer: They collect data from newspaper and television sites on a daily basis. Most of the protest data come from these data/crawls. Apart from this, they have a software that consists of a python backend for crawling and categorizing articles. All the collected data is stored in a MySQL database and covers protest events in the United States from 20 January 2017 to 31 january 2021.

- How does CountLove make their estimates about the number of people who attended a protest? What potential problems might arise from this method of estimation? Please answer in 3-4 sentences (4 points)
 - Answer: CountLove records the most conservative attendance number from the news articles that they link. They interpret “a dozen” as 10, “dozens” as 20, “hundreds” as 100, and so forth. If an article mentions a demonstration but does not include an attendance count, we note the demonstration but leave the count empty. This misrepresentation of count might leave out important information about the protest and the impact of the protest.

## While You Code: Critical Analysis & Reflection

- Reflection 1: Why do you think the mean is higher than the median? Which metric would you use in a report about this data, and why? Please answer in 2-3 sentences (2 points)
 - Answer: Since the mean is greater than the median, this implies that the data is skewed to the right. This means that there are fewer protest with large number of attendees. Therefore this pulls up the mean for the attendees.

- Reflection 2: Before actually calculating the number of protests that occurred in 2018, 2019, 2020, record your guesses for the following questions. (1 point)

  Guess: Do you think there were more protests in 2019 than in 2018? Why or why not? Please answer in 1 or 2 sentences
   - Answer: The protests in 2018 were primarily immigration or civil rights protests whereas in 2019, there were mainly environment protests. Therefore, there was no significant protest or data that would determine which year had the maximum number of protests. It could be possible that there were more protests in 2019 than 2018.

  Guess: Do you think there were more protests in 2020 than in 2019? Why or why not? Please answer in 1 or 2 sentences
   - Answer: In the year the 2020 there were two major event - George Floyd protest and Covid-19. Therefore just by understanding the social state of the country I can say that there were more protests in 2020 than 2019.  The main reason is because there were significant event in the year 2020 than 2019. 

- Reflection 3: Does the change in the number of protests from 2018 to 2019 to 2020 surprise you? Why or why not? What do you think explains the fluctuation? Please answer in 1 or 2 sentences (2 points)
 - Answer: No, the change in the number of protests from 2018 to 2019 to 2020 does not surprise me. This is because every year there are new events that cause a change in the economy/ status of the country. The year 2020 experienced major causes for protest as events in 2020 influenced the status of the country. In general, changes in political economy, government policies, and external factors can cause a change in the number of protests year-to-year. 

- Reflection 4: What is the first and fourth most frequent category of protest? Do these frequencies align with your sense of the major protest movements in the U.S. in the last few years? Why or why not? (3 points)
 - Answer: First most frequent category of protest: Racial Injustice
          Fourth most frequent category of protest: Immigration
  These, to an extent, align with my thought of major protest movements. Racial injectice relates more towards events in 2019-2020 whereas immigration represents the time when there were protests to improve the lives of immigrant communities. The timeline of these events play a crucial role in determining the number of protests in each category.

## After You Code: Critical Analysis & Reflection

In the second chapter of *Data Feminism*, Klein and D'Ignazio describe 4 ways that data scientists can challenge power and take action:
> Taking action can itself take many forms, and in this chapter we offer four starting points:  
> (1) Collect: Compiling counterdata—in the face of missing data or institutional neglect—offers a powerful starting point as we see in the example of the DGEI, or in María Salguero’s femicide maps discussed in chapter 1.  
> (2) Analyze: Challenging power often requires demonstrating inequitable outcomes across groups, and new computational methods are being developed to audit opaque algorithms and hold institutions accountable.  
> (3) Imagine: We cannot only focus on inequitable outcomes, because then we will never get to the root cause of injustice. In order to truly dismantle power, we have to imagine our end point not as “fairness,” but as co-liberation.  
> (4) Teach: The identities of data scientists matter, so how might we engage and empower newcomers to the field in order to shift the demographics and cultivate the next generation of data feminists?  

- How does the CountLove project embody one or more of these 4 forms of challenging power? Please answer in at least 3-4 sentences (3 points)
 - Answer: The CountLove project challenges existing power structures and provide data of underrepresented groups.The data that they collect leads to holding institutions accountable and results in spreading awareness of the different events taking place. They also empower upcoming datra feminists to build on their skills and professional developments in the field of data analysis/science. Hence, CountLove embodies the principle of data feminism. 

- What is the most interesting or surprising thing you learned from this analysis? Please answer in at least 2-3 sentences (2 points)
 - Answer: Analysis of this data has introduced me to how over the years there have been political/social events that have caused a drastic change in the economy. Apart from this the data also how each protest has relates to data feminism and contents in this course.
 
- What is a kind of analysis that you would like to do or that would be interesting to do with the CountLove data that you don't have the time or skills to accomplish at this moment? Please answer in at least 2-3 sentences (2 points)
 - Answer: I am more inclined towards using that data to draw up solutions or different approaches to tackle socio-economic problems. Every data coolected by CountLove has meaning and value to it. Understanding key events from the data can help in drawing conclusions and solutions towards economic probelems. This in turn might lead to fewer protests, violences, and in general make peolpe more aware of their economy. Hence, I would like to be part of this side of the analysis that can have impacts on the future of the economy. 
