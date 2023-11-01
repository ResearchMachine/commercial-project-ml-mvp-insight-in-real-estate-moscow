# (2023) Searching-for Real Estate Insights in Moscow by Boosting Methods
**Project Type:**  Freelance Project, Machine Learning, MVP  
**Programming Language:** Python 3 (xgboost, difflib, sklearn, BeautifulSoup, cloudscraper, re)  
**Project Сode (main scripts):** [Parser](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/preprocessing/run_preprocessing.ipynb); [ML Insight Extractor](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/modeling/run_modeling.ipynb)   
**Project Full Description:** [Presentation](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/EN.pdf)

### I. Motivation
The main goal of the project is MVP development of a fully automated platform for recommending commercial real estate in Moscow from open sources.  


### II. Problem
The task of developing a platform for searching for insights in commercial real estate in Moscow from open sources is considered. As a result of the work, an MVP was developed for uploading insights from cian.ru, an assessment was made of the difficulties of scaling and automation.

### III. Key Results 
* Implemented MVP (parser + ml pipline), with 5 objects were found, which were marked by real estate experts as underestimated;
* Main problems: impossibility to guarantee the security of a transaction without face-to-face verification; .


Thus, it is possible to automate recommendations only for real estate experts. It is related to impossibility of guarantee the security of the transaction. For the implementation of the platform, the bulk of the work will be related to the negotiations and design of the announcement.

### IV. Content

![image](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/assets/70639823/67974aa5-54b5-41b3-a3f4-8258d3fea1e1)  
Geographic clusters of commercial advertisements (structures) CIAN in Moscow

**Results:**
* Top30 (out of over 1500 options) undervalued commercial real estate extractor algorithm was developed for daily monitoring (Moscow, Russia)
* By 40% (to ≈900) was reduced searching area from unwanted objects (duplicates, dilapidated housing, business for sale, etc.) through ads text analysis
* 60-70% accuracy rate of extractor algorithm was achieved based on 5 data annotations from real estate experts (interesting/non-interesting ad)
* 3 properties were identified as rare finds and were confirmed by real estate experts
* Data was extracted from a Russian real estate website (CIAN)


**About Algorithm:**
* Roughly speaking, the algorithm train a predictor on the “average” segment, which predicts the price price_pred for the entire dataset and ranks it by price_fact - price_pred,  
* The algorithm can get stuck on "problem" ads (dilapidated housing, scammers, technical floor, etc.),  
* The algorithm is sensitive to filters, the setting of which requires fresh knowledge of the market.  
The first reason is essentially an indicator of the quality of the algorithm - "problem" ads should be relatively cheap in terms of available factors. Dilapidated housing can often be identified only by appearance. Increasing filters by year of construction leads to a significant reduction in dilapidated housing, but greatly reduces the volume of insights. The list also includes ads from scammers, which also requires manual control (at least it is necessary to ring the ads).


**Key Problem of Scalability to Big Platform:**
1. Realtor Checking. If the realtor turns out to be a scammer, the platform will receive a negative review. This can greatly damage your reputation and we cannot influence it.  
2. Market Knowledge and Explainability for User. We used many manual filters that cannot be obtained without special knowledge about the market. And also, we cannot use deep algorithms, since we must explain to the user why they should buy exactly this object.

**Thus, using ML from open source commercial real estate is profitable only for indiviual using.**

**Project Code**:
1. [Parser (result - .xlsx dataframe)](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/preprocessing/run_preprocessing.ipynb);  
2. [ML Insight Extractor (result - TOP30 links)](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/modeling/run_modeling.ipynb).

**Project Description:** [Presentation](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/EN.pdf)

### IV. Team
Data Scientist (me), 2 Real Estate Experts
