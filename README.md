# (2023) Analytics of Commercial Real Estate in Moscow. Search for Insights of ML Methods
**Project Type:**   Commercial Data Science project, Machine Learning, MVP  
**Programming Language:** Python 3 (xgboost, difflib, sklearn, BeautifulSoup, cloudscraper, re)  
**Project Сode:**  
**Project Full Description** (in Russian):  
**Company:** [REVIZOR LLC](https://kupiluki.ru/) (RUS)  




### I. Motivation
The main goal of the project is MVP development of a fully automated platform for recommending commercial real estate in Moscow.  
Example: AI Realiste for real estate investing in Dubai.

### II. Problem
The task of developing a platform for searching for insights in commercial real estate in Moscow from open sources is considered. As a result of the work, an MVP was developed for uploading insights from cian.ru, an assessment was made of the difficulties of scaling and automation.

### III. Key Results 
* Implemented MVP (parser + ml pipline), with the help of which 5 objects were found, which were marked by experts as underestimated;
* The key difficulty of implementing a recommendation platform is not related to ML - it is impossible to guarantee the security of a transaction without face-to-face verification.


Thus, by means of ML it is possible to obtain only recommendations for real estate experts. It is related to it is impossible to guarantee the security of the transaction. For the implementation of the platform, the bulk of the work will be related to the negotiations and design of the announcement.

### III. Content
Within the framework of the project, 2 main tasks of data analysis were solved:
* CIAN site parser developed, uses xgboost, sklearn, beatifulsoup, re;   
* the concept of the algorithm was developed and tested, which takes into account the professional principles of real estate valuation (feature selection) and the noise in the data (it is solved as a ranking problem).  
The key difficulties of unifying and automating the algorithm for creating a recommendation platform for a large number of users have been identified:
* the algorithm can get stuck on "problem" ads (dilapidated housing, scammers, technical floor, etc.),  
* the algorithm is sensitive to filters, the setting of which requires fresh knowledge of the market.  
The first reason is essentially an indicator of the quality of the algorithm - "problem" ads should be relatively cheap in terms of available factors. Dilapidated housing can often be identified only by appearance. Increasing filters by year of construction leads to a significant reduction in dilapidated housing, but greatly reduces the volume of insights. The list also includes ads from scammers, which also requires manual control (at least it is necessary to ring the ads).

**The project code contains 2 scripts**:
1. Parser (result - .xlsx dataframe);  
2. ML Insight Extractor (result - TOP30 links).
