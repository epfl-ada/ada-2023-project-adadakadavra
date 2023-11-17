# Donald Trump's influence during Covid: How bad can be the communication's impact of a leader?

## Abstract :

Donald Trump’s many tweets during the Covid pandemic spread like wildfire, probably making him one of the most
influential figures during the pandemic – but in the end, was he that influential? Will causal analyses of the effect of
Trump’s tweets on Wikipedia and Google Trends pageviews show that he was leading or following online trends? Our
goal is to study the impact an influential leader can have on information spread in a
crisis with a focus on fake news, as an overload of misleading or contradictory
statements (an infodemic, as [WHO](https://www.who.int/health-topics/infodemic#tab=tab_1) calls it) are known to have a detrimental impact on crisis
management. To provide a more comprehensive insight into Trump’s actual influence
on online information spread, we would then like to compare it with that of other
factors such as mobility restrictions or key milestones (e.g. first Covid death). Trump
the Trend Maker or Trump the Follower, that is the question!

## Research questions

- Was Donald Trump a trend maker or a follower: can we spot a correlation or
even causality between his declarations and online trends, i.e. Wikipedia or
Google Trends pageviews?
- Do his tweets have a more significant impact on information spread when
they convey fake news?
- How does Trump’s influence compare with that of other factors such as
mobility restrictions or official announcements?
## Proposed additional datasets

To conduct the analysis, we'll complete the given dataset with the following:

- Donald Trump's tweet between 2019 and
  2021: [Kaggle](https://www.kaggle.com/datasets/codebreaker619/donald-trump-tweets-dataset)
- List of known fake news and their Google trends'
  reference : [GitHub](https://github.com/epfl-dlab/fact-checkers-fact-check/blob/main/data/kg_ids.json)
- Data extracted from Google Trends and Wikipedia

The first dataset is composed of Donald Trump tweets until 2021. It has very few
missing values and also includes information such as the number of likes and
retweets, and whether the tweet has been deleted or not (which could be an
indicator of fake information).
The second addition is a mapping between claim clusters and knowledge graph ids.
Ribeiro et al. regrouped fact-checks from a dataset provided by the IFCN into 39
clusters (e.g. with topic ‘alcohol’), which they matched with entities in Google
Knowledge Graph, allowing us to search time series associated with the claims on
Google Trends.
Finally, we will directly search for pageviews time series for a few specific articles on
Wikipedia or queries on Google Trends to conduct a more fine-grained analysis of
information spread. This will allow us to track the evolution of pageviews for specific
topic such as hydroxychloroquine on Wikipedia for instance.

## Method
The purpose of our analysis is to study the impact of Donald Trump’s tweets on the
popularity of online content. To achieve this, we will take the following steps.
First, we will conduct a causal impact study of Trump’s Covid-related tweets on
Wikipedia and Google Trends pageviews for several topics (e.g. ‘Covid’). In practice,
we will start by gathering all the tweets mentioning for instance
‘hydorxychloroquine’ in the Kaggle tweet dataset mentioned earlier. We will then
study the causal impact of each of these tweets on the associated Wikipedia/Google
Trends timeseries on this topic using the [Causal Impact library](https://google.github.io/CausalImpact/CausalImpact.html). This library allows us to
assess the impact of an intervention, i.e. a tweet by Trump, by comparing the
evolution of the time series of interest with that of a few other control time series.
For the control time series, we chose a set of ten popular non Covid-related topics
such as ‘Google’.
Second, to try to answer the question: ‘Was Trump a trend maker or a follower?’, we
would like to conduct a [Granger causality test](https://en.wikipedia.org/wiki/Granger_causality) to assess whether Trump’s tweets
are a good predictor of online trends or the other way around.
Finally, to give more insight into Trump’s influence, we would like to redo the Causal
Impact/Granger causality analysis using other causal factors such as official
announcements or mobility restrictions. For the former, we will use the interventions
of the Coronawiki dataset (e.g. first Covid case) and manually search for a few key
milestones/announcements if that proves relevant. For the mobility restrictions, we
will use the Apple and Google mobility reports to compute mobility and normality
changepoints in a similar fashion as our reference paper ‘Sudden Attention Shifts on
Wikipedia During the COVID-19 Crisis’.
## Proposed timeline

We organized our team in subgroups of 2 to 3 people working on parts of the
project. We meet twice a week to put our respective contributions to gather and
discuss our progress and future steps.
We propose a timeline structured in two-week intervals until late December (the
people assigned to the task are in italic):
- Nov 17, Milestone 2 submission;
- Dec 1, Discuss feedback from Milestone 2 and apply required changes to
existing notebook (Pietro, Matteo, Michelangelo), gather a list of
topics/news/announcements/key Covid-related events to focus our analysis
on (Sabri, Etienne), learn the basics of website creation (everyone);
- Dec 15, Complete the analysis in the Notebook code with helpfer functions +
graphs (Part 1 with tweets: Pietro, Matteo, Michelangelo; Part 2 with alternative
hypotheses: Sabri, Etienne), Make a first draft of the data story (Visuals/format:
Pietro, Matteo, Michelangelo; Text: Sabri, Etienne);
- Dec 22, Ask for final feedback, detail/clarify the explanations (in English) and
the comments in the Notebook and polish the data story website (For both the
notebook and the data story, Part 1 with tweets: Pietro, Matteo, Michelangelo;
Part 2 with alternative hypotheses: Sabri, Etienne).


## Questions for TAs
- Twitter events and announcements are discrete events, but mobility (provided
by Apple and Google Mobility Reports) is not: should we keep working with
mobility changepoints or would it make more sense to keep the entire time
series?
- We are making fairly strong assumptions by focusing our attention on events
in the United States although the English Wikipedia and Google are used
worldwide. Will it be sufficient to carefully interpret our results, or should we
look for a way to identifiy online trends in the US?
