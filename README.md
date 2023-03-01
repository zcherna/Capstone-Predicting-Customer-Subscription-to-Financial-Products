![header](./Images/slides_header.png)
# Overview
My goal for this project was to advise a retail bank as to how it may increase its return on investment (ROI) on financial products it sells to clients. Specifically, the bank's objectives were to increase subscription revenue from term deposits while simultaneously decreasing its customer acquisition costs. To help the bank achieve its goals, I first sought to analyze its historical data on term deposits, and gain insight about the customers who sign up for this product. Second, I sought to train a model on their data that could predict future customer subscription. At the end of my analysis, I present a data-driven marketing and sales strategy that should enable the bank to accomplish its goal of increasing term deposit ROI.
# Business Understanding
A term deposit is a financial product whereby a customer agrees to lock up funds with the bank for a fixed period of time, and in doing so they receive a guaranteed rate of return. It’s an important source of bank revenue, but there are a few unique challenges that accompany its growth. Not everyone wants to, or can afford to lock up funds for an extended period of time. Many people live paycheck to paycheck and need to maintain access to liquidity. Additionally, the rate of return for a term deposit tends to be modest, which makes it unattractive to customers who would prefer alternative investments with a greater potential return. Another unique challenge to my stakeholder is that they have historically relied on expensive,  labor-intensive call centers to run telemarketing campaigns. This makes it difficult to grow subscription revenue without growing the customer acquisition costs. Therefore, it is crucial to implement a targeted marketing and sales strategy that optimizes ROI over revenue growth. Fortunately, machine learning and exploratory data analysis can be used to identify which customers should be targeted, and craft an efficient strategy going forward. 
# Data Understanding 
The dataset I used came from Kaggle and can be found here: https://www.kaggle.com/datasets/prakharrathi25/banking-dataset-marketing-targets 
 
It consists of 45,211 rows of data pertaining to customers of a Portuguese retail bank and includes a number of demographic attributes as well as information about a prior telemarketing campaign. The target column in the original dataset is ‘y’, which I renamed ‘made_deposit’ in my analysis. The following is a description of the feature columns:
1 - age (numeric)
2 - job : type of job (categorical: "admin.","unknown","unemployed","management","housemaid","entrepreneur","student",
"blue-collar","self-employed","retired","technician","services")
3 - marital : marital status (categorical: "married","divorced","single"; note: "divorced" means divorced or widowed)
4 - education (categorical: "unknown","secondary","primary","tertiary")
5 - default: has credit in default? (binary: "yes","no")
6 - balance: average yearly balance, in euros (numeric)
7 - housing: has housing loan? (binary: "yes","no")
8 - loan: has personal loan? (binary: "yes","no")
9 - contact: contact communication type (categorical: "unknown","telephone","cellular")
10 - day: last contact day of the month (numeric)
11 - month: last contact month of year (categorical: "jan", "feb", "mar", …, "nov", "dec")
12 - duration: last contact duration, in seconds (numeric)
13 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
14 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric, -1 means client was not previously contacted)
15 - previous: number of contacts performed before this campaign and for this client (numeric)
16 - poutcome: outcome of the previous marketing campaign (categorical: "unknown","other","failure","success")
