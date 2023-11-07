# (2023) Data Mining of Real Estate in Moscow 
**Project Type:**  Freelance Project, Machine Learning, MVP  
**Programming Language:** Python 3 (xgboost, difflib, sklearn, BeautifulSoup, cloudscraper, re)  
**Project Сode (main scripts):** [Parser](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/preprocessing/run_preprocessing.ipynb); [ML Insight Extractor](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/modeling/run_modeling.ipynb)   
<!--- **Project Full Description:** [Presentation](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/EN.pdf) --->



### I. Problem
Parse special segment data from Russian real estate website (CIAN) and conduct exploratory data analysis.

### II. Key Results 
* Data was extracted from a Russian real estate website (CIAN)
* By 40% (to ≈900) was reduced searching area from unwanted objects (duplicates, dilapidated housing, business for sale, etc.) through ads text analysis
* Top30 (out of over 1500 options) undervalued commercial real estate extractor algorithm was developed for daily monitoring (Moscow, Russia)
* 60-70% accuracy rate of extractor algorithm was achieved based on 5 data annotations from real estate experts (interesting/non-interesting ad)
* 3 properties for 1 month of MVP work were identified as rare finds and were confirmed by real estate experts 



### III. Content
**About Algorithm:**
* Roughly speaking, the algorithm train a predictor on the “average” segment, which predicts the price price_pred for the entire dataset and ranks it by price_fact - price_pred,
* The algorithm uses only factors of professional real estate assessment (object parameters, geoparameters), which eliminates the possibility of retraining on ad factors (when a realtor was online for ex.)
* The algorithm can get stuck on "problem" ads (dilapidated housing, scammers, technical floor, etc.),  
* The algorithm is sensitive to filters, the setting of which requires fresh knowledge of the market.  
The first reason is essentially an indicator of the quality of the algorithm. Some unwanted ads should be relatively cheap in terms of available factors (large warehouse for ex.). Dilapidated housing can often be identified only by appearance. Increasing filters by year of construction leads to a significant reduction in dilapidated housing, but greatly reduces the volume of insights. The list also includes ads from scammers, which also requires manual control (at least it is necessary to ring the ads).

![image](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/assets/70639823/67974aa5-54b5-41b3-a3f4-8258d3fea1e1)  
Geographic clusters of commercial advertisements (structures) CIAN in Moscow



<!--- 
**Key Problems of Scalability to Big Platform:**
1. Realtor Checking. If the realtor turns out to be a scammer, the platform will receive a negative review. This can greatly damage platform reputation and we cannot influence it.  
2. Market Knowledge and Explainability for User. We used many manual filters that cannot be obtained without special knowledge about the market. And also, we cannot use deep algorithms, since we must explain to the user why they should buy exactly this object.  
**Thus, using Data Analysis from open source commercial real estate in Moscow is profitable only for indiviual using.**--->

**Project Code**:
1. [Parser (result - .xlsx dataframe)](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/preprocessing/run_preprocessing.ipynb);  
2. [ML Insight Extractor (result - TOP30 links)](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/modeling/run_modeling.ipynb).
<!--- **Project Description:** [Presentation](https://github.com/ResearchMachine/commercial-project-ml-mvp-insight-in-real-estate-moscow/blob/main/EN.pdf) --->

### IV. Team
Data Scientist (me), Real Estate Analytic
