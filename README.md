##  COVID-19, its impact and the government policy response
Liem Luong

University of Washington

11/5/2020

--------------------------------------------------------------------

### Summary
We are living in a connected world. Each of us play an important role in fighting the COVID together. Tracking the total coronavirus cases daily is important. However, the relationship between the current pandemic and the government policy responses is noteworthy. That can potentially provide an interesting story. Eventually, it benefits the people from human center perspective.

COVID-19 is surely the most search keyword on the internet currently and the most talked topic in the news in 2020. The impact of the coronavirus can be seen everywhere. This is considered the most casualty pandemic in humankind. It touches every corner of the world: people, economy, government, school, and travel.

My motivation to choose this topic is simple: learning something from the past can be helpful for dealing with the future problems. Considering this analysis, I hope it will be a great contribution to the human knowledge. Most importantly, something for the future readers to look back to be well-equipped for future pandemics. In particular, i want to find out the answer for my research qurstion and confirmation of my hypothesis: 
- Research Question: What is the impact of the combination of government policies on the COVID confirmed cases around the world?

- Hypothesis: Containment and closure policies (travel restriction, school closing, restrict public gathering) may help to contain the COVID spreading cases better than health policies (contact tracing and facial covering)

Following the analysis report from the start to end, we will find out the answer for the research question as well as the hypothesis.


### Reproducibility
This research is set up in a way for reproducibility. Sharing knowledge and outcome are essential, making it easy for people to reproduce the same result is critical as well. The repository includes the following components for future readers:
| Components | Description|
| --- | --- |
| README | Overall information about the research project|
| LICENSE | Information about the license of this research on this repository
| Final Project Proposal | Information about the project: motivation, data, methodology, background, etc. |
| Data | folder contains raw data source for the project |
| Image | folder contains visualizations and chart images |
| Analysis | folder contains Jupyter Notebook of the main analysis |


### About the Data
The data source for this analysis is from the University of Oxford - Blavatnik School of Government. In particular, the Oxford COVID-19 Government Response Tracker (OxCGRT) is the main source where it is a comprehensive dataset collected by many volunteers around the world on many diferent common policy responses that governments have taken to respond to the pandemic. It now has data from more than 180 countries.

#### About the Oxford COVID Tracker:
> [Oxford COVID-19 Government Response Tracker](https://www.bsg.ox.ac.uk/research/research-projects/coronavirus-government-response-tracker)

#### The dataset:
> Dataset is updated daily and can be acquired from here or from the data folder on this repository:
> [OxCGRT latest CSV file](https://raw.githubusercontent.com/OxCGRT/covid-policy-tracker/master/data/OxCGRT_latest.csv)

#### Data use policy:
> Creative Commons Attribution CC BY standard. This data is provided free of charge.

#### Recommended citation:
> Thomas Hale, Tilbe Atav, Laura Hallas, Beatriz Kira, Toby Phillips, Anna Petherick, Annalena Pott. Variation in US states’ responses to COVID-19. Blavatnik School of Government

The dataset contains the indicators in four groups. For the purpose of this analysis, we concentrate on the relationship of containment & closure policies and health system policies.
- C - containment and closure policies
- H - health system policies

#### Containment & Closure Policies
| ID | Name | Description | Measurement | Coding |
| --- | --- | --- | --- | --- |
| C1 | `C1_School closing` | Record closings of schools and universities | Ordinal scale | 0 - no measures <br/>1 - recommend closing or all schools open with alterations resulting in significant differences compared to non-Covid-19 operations <br/>2 - require closing (only some levels or categories, eg just high school, or just public schools) <br/>3 - require closing all levels <br/>Blank - no data |
| C2 | `C2_Workplace closing` | Record closings of workplaces | Ordinal scale | 0 - no measures <br/>1 - recommend closing (or recommend work from home) <br/>2 - require closing (or work from home) for some sectors or categories of workers <br/>3 - require closing (or work from home) for all-but-essential workplaces (eg grocery stores, doctors) <br/>Blank - no data |
| C3 | `C3_Cancel public events` | Record cancelling public events | Ordinal scale | 0 - no measures <br/>1 - recommend cancelling <br/>2 - require cancelling <br/>Blank - no data |
| C4 | `C4_Restrictions on gatherings` | Record limits on private gatherings | Ordinal scale | 0 - no restrictions <br/>1 - restrictions on very large gatherings (the limit is above 1000 people) <br/>2 - restrictions on gatherings between 101-1000 people <br/>3 - restrictions on gatherings between 11-100 people <br/>4 - restrictions on gatherings of 10 people or less <br/>Blank - no data |
| C5 | `C5_Close public transport` | Record closing of public transport | Ordinal scale | 0 - no measures <br/>1 - recommend closing (or significantly reduce volume/route/means of transport available) <br/>2 - require closing (or prohibit most citizens from using it) <br/>Blank - no data |
| C6 | `C6_Stay at home requirements` | Record orders to "shelter-in-place" and otherwise confine to the home | Ordinal scale | 0 - no measures <br/>1 - recommend not leaving house <br/>2 - require not leaving house with exceptions for daily exercise, grocery shopping, and 'essential' trips <br/>3 - require not leaving house with minimal exceptions (eg allowed to leave once a week, or only one person can leave at a time, etc) <br/>Blank - no data |
| C7 | `C7_Restrictions on internal movement` | Record restrictions on internal movement between cities/regions | Ordinal scale | 0 - no measures <br/>1 - recommend not to travel between regions/cities <br/>2 - internal movement restrictions in place <br/>Blank - no data |
| C8 | `C8_International travel controls` | Record restrictions on international travel <br/><br/>Note: this records policy for foreign travellers, not citizens | Ordinal scale | 0 - no restrictions <br/>1 - screening arrivals <br/>2 - quarantine arrivals from some or all regions <br/>3 - ban arrivals from some regions <br/>4 - ban on all regions or total border closure <br/>Blank - no data |

#### Health System Policies
| ID | Name | Description | Measurement | Coding |
| --- | --- | --- | --- | --- |
| H1 | `H1_Public information campaigns` | Record presence of public info campaigns | Ordinal scale | 0 - no Covid-19 public information campaign <br/>1 - public officials urging caution about Covid-19 <br/>2- coordinated public information campaign (eg across traditional and social media) <br/>Blank - no data |
| H2 | `H2_Testing policy` | Record government policy on who has access to testing <br/><br/>Note: this records policies about testing for current infection (PCR tests) not testing for immunity (antibody test) | Ordinal scale | 0 - no testing policy <br/>1 - only those who both (a) have symptoms AND (b) meet specific criteria (eg key workers, admitted to hospital, came into contact with a known case, returned from overseas) <br/>2 - testing of anyone showing Covid-19 symptoms <br/>3 - open public testing (eg "drive through" testing available to asymptomatic people) <br/>Blank - no data |
| H3 | `H3_Contact tracing` | Record government policy on contact tracing after a positive diagnosis <br/><br/>Note: we are looking for policies that would identify all people potentially exposed to Covid-19; voluntary bluetooth apps are unlikely to achieve this | Ordinal scale | 0 - no contact tracing <br/>1 - limited contact tracing; not done for all cases <br/>2 - comprehensive contact tracing; done for all identified cases |
| H4 | `H4_Emergency investment in healthcare` | Announced short term spending on healthcare system, eg hospitals, masks, etc <br/><br/>Note: only record amount additional to previously announced spending | USD | Record monetary value in USD <br/>0 - no new spending that day <br/>Blank - no data |
| H5 | `H5_Investment in vaccines` | Announced public spending on Covid-19 vaccine development <br/><br/>Note: only record amount additional to previously announced spending | USD | Record monetary value in USD <br/>0 - no new spending that day <br/>Blank - no data |
| H6 | `H6_Facial Coverings` | Record policies on the use of facial coverings outside the home <br/> | Ordinal scale | 0 - No policy <br/>1 - Recommended <br/>2 - Required in some specified shared/public spaces outside the home with other people present, or some situations when social distancing not possible <br/>3 - Required in all shared/public spaces outside the home with other people present or all situations when social distancing not possible <br/>4 - Required outside the home at all times regardless of location or presence of other people |

#### Stringency and Policy Indices
OxCGRT collects publicly available information of government responses. The data from the indicators is aggregated into a set of four common indices, reporting a number between 1 and 100 to reflect the level of government action on the topics in question:

- An overall government response index (which records how the response of governments has varied over all indicators in the database, becoming stronger or weaker over the course of the outbreak);
- A containment and health index (which combines ‘lockdown’ restrictions and closures with measures such as testing policy and contact tracing, short term investment in healthcare, as well investments in vaccine)
- An economic support index (which records measures such as income support and debt relief)
- The original stringency index (which records the strictness of ‘lockdown style’ policies that primarily restrict people’s behaviour).

### How to run the Jupyter Notebook
This analysis is conducted using the Python Jupyter Notebook. You should have Anaconda software installed on your machine. The software is free and available for download on the website [Anaconda](https://www.anaconda.com/)

The Jupyter Notebook has all the detail steps by steps showing the analysis. It also has the comment markup text throughtout the notebook. This will ensure, the instruction is clear and the process is straightforward so that future users can reproduce this analysis easily. 

### Helpful Notes
- This is an ongoing data collection of live data around the world. Every country has different reporting structure, therefore, not all countries have the same updates on the same pace. Where there are delays, the dataset reflects the missing data respectively.

- This dataset is updated daily by a great team of contribution from people around the world. Our world changes rapidly as well as data throughout this crisis, there is a chance of inaccuracies in the underlying data. If you notice any incorrect data, you can report this directly to the team at [Oxford COVID 19 Tracker](https://forms.office.com/Pages/ResponsePage.aspx?id=G96VzPWXk0-0uv5ouFLPkVPwT6t5-mtCnZ6_s5yQ4ppUME9NOUtYRkxLVldLUVFERTRTMEJSRkZITC4u)

- Note that these stringency indices simply record the number and strictness of government policies, and should not be interpreted as ‘scoring’ the appropriateness or effectiveness of a country’s response. A higher position in an index does not necessarily mean that a country's response is ‘better’ than others lower on the index.
