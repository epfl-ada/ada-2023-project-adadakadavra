# Donald Trump's influence during Covid: How bad can be the communication's impact of a leader?

## Abstract :

Donald Trump was influential during Covid, wasn’t he? All the fake news that he spread are now very well documented.
This project proposes to study the impact of his communication during Covid. By focusing on his tweets, we want to know
if we can spot a causality between his declaration and the trends on Google and Wikipedia. If Donald Trump was not only
tweeting Fake News, he was also tweeting about Vaccines and Lockdown, as comparison with the fake news, did these
declarations had an impact? To do so, we'll focus on his tweets, analyzed through a list of known fake news, on Google
and wikipedia trends and mobility reports. Finally, we'd like to assess how bad was a mixed communication between the
official instances (such as FDA) and their leader. Knowing that this can a logical impact on vaccination and infection
rate.

## Research questions

- Was Donald Trump a trend maker or a follower?
- Can we spot correlation and even causality between his declarations and online trends?
- Can we assess how bad the impact of his communcation was?
- Finally, could we spot correlation with infections or vaccination rates ? (TO KEEP?)

## Proposed additional datasets

To conduct the analysis, we'll complete the given dataset with the following:

- Donald Trump's tweet between 2019 and
  2021: [Kaggle](https://www.kaggle.com/datasets/codebreaker619/donald-trump-tweets-dataset)
- List of known fake news and their Google trends'
  reference : [GitHub](https://github.com/epfl-dlab/fact-checkers-fact-check/blob/main/data/kg_ids.json)
- Data extracted from Google Trends and Wikipedia

The first dataset is composed of DT tweets until 2021, it has very few missing datas and also includes the number of
retweets, if the tweet has been deleted or not (which could be an indication of fake information).

## Method

To study DT influence, we want to study causality between his tweets and the trends. This starts by studying the
correlation between the time he tweets on a topic and the trends. Then, we have to draw causalities between time series.
To do so, and depending on what causal link we want to show, we need some baseline time series, this can be DT's tweets
not related to Covid, average of trends on Wikipedia pages or tweets related to Covid but by another instance (let's
saty the FDA). Further, the causality between time series can be assessed via a Granger causality test. This should give
the answer to our first question, whether DT was making or following the trend. Finally, we would like to look for
alternative hypothesis to mitigate the impact of DT tweets. This can be done by reconducting the same analysis now with
announcements times, mobility report or any other source that could explain the trends.

## Proposed timeline
We propose a timeline based on a 2-weeks assessment basis until late December:
- Nov 17, Milestone 2 submission
- Dec 1,
- Dec 15,
- Dec 22, Milestone 3 submission

## Organization within the team

We organized the team as subteams (2 to 3 people) working on parts of the project. We meet twice a week to gather the
work on different parts. Our organization follows this idea of dividing the tasks:

-

## Questions for TAs
-


## questions

Readme.md file containing the detailed project proposal (up to 1000 words). Your README.md should contain:
Title
Abstract: A 150 word description of the project idea and goals. What’s the motivation behind your project? What story
would you like to tell, and why?
Research Questions: A list of research questions you would like to address during the project.
Proposed additional datasets (if any): List the additional dataset(s) you want to use (if any), and some ideas on how
you expect to get, manage, process, and enrich it/them. Show us that you’ve read the docs and some examples, and that
you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check
that what you propose is feasible.
Methods
Proposed timeline
Organization within the team: A list of internal milestones up until project Milestone P3.
Questions for TAs (optional): Add here any questions you have for us related to the proposed project.
Notebook containing initial analyses and data handling pipelines. We will grade the correctness, quality of code, and
quality of textual descriptions.
