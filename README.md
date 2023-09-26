# (2023) Analytics of Commercial Real Estate in Moscow. Search for Insights of ML Methods
**Project Type:**  Individual Commercial Project, Machine Learning, MVP  
**Programming Language:** Python 3 (xgboost, difflib, sklearn, BeautifulSoup, cloudscraper, re)  
**Project Сode (main scripts):** [Parser](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/preprocessing/run_preprocessing.ipynb); [ML Insight Extractor](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/modeling/run_modeling.ipynb)  
**Company:** [REVIZOR LLC](https://kupiluki.ru/) (RUS)  
**Project Full Description:** [Presentation](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/EN.pdf)

### I. Motivation
The main goal of the project is MVP development of a fully automated platform for recommending commercial real estate in Moscow.  
Example: AI Realiste for real estate investing in Dubai.

### II. Problem
The task of developing a platform for searching for insights in commercial real estate in Moscow from open sources is considered. As a result of the work, an MVP was developed for uploading insights from cian.ru, an assessment was made of the difficulties of scaling and automation.

### III. Key Results 
* Implemented MVP (parser + ml pipline), with the help of which as minimum 5 objects were found, which were marked by experts as underestimated;
* The key difficulty of implementing a recommendation platform is not related to ML - it is impossible to guarantee the security of a transaction without face-to-face verification.


Thus, it is possible to automate recommendations only for real estate experts. It is related to impossibility of guarantee the security of the transaction. For the implementation of the platform, the bulk of the work will be related to the negotiations and design of the announcement.

### III. Content

![image](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/assets/70639823/67974aa5-54b5-41b3-a3f4-8258d3fea1e1)  
Geographic clusters of commercial advertisements (structures) CIAN in Moscow

Within the framework of the project, 2 main tasks of data analysis were solved:
* CIAN site parser developed, uses xgboost, sklearn, beatifulsoup, re;   
* the concept of the algorithm was developed and tested, which takes into account the professional principles of real estate valuation (feature selection) and the noise in the data (it is solved as a ranking problem).  
The key difficulties of unifying and automating the algorithm for creating a recommendation platform for a large number of users have been identified:
* the algorithm can get stuck on "problem" ads (dilapidated housing, scammers, technical floor, etc.),  
* the algorithm is sensitive to filters, the setting of which requires fresh knowledge of the market.  
The first reason is essentially an indicator of the quality of the algorithm - "problem" ads should be relatively cheap in terms of available factors. Dilapidated housing can often be identified only by appearance. Increasing filters by year of construction leads to a significant reduction in dilapidated housing, but greatly reduces the volume of insights. The list also includes ads from scammers, which also requires manual control (at least it is necessary to ring the ads).



**The project code contains 2 scripts**:
1. [Parser (result - .xlsx dataframe)](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/preprocessing/run_preprocessing.ipynb);  
2. [ML Insight Extractor (result - TOP30 links)](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/modeling/run_modeling.ipynb).

**Project Full Description:** [Presentation](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/EN.pdf)
