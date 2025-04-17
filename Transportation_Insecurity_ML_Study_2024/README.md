# Exploring Transit Insecurity in America via Household Census Data 
### Course: Machine Learning Foundations with Python, Spring 2024, Professor: Gabriela Gongora-Svartzman, Ph.D.
#### Co-Author: Kaia Hu kaiqihu@andrew.cmu.edu and Megan Ty mlty@andrew.cmu.edu

---

## Disclaimer/Sensitive Content
This project was conducted for academic purposes for Heinz College's 90803 course "Machine Learning Foundations with Python" in the Spring 2024 semester. This following project is uses household-level census data to study transit insecurity. The authors recognize that the census data contains data on potentially sensitive information such as race, disability, and gender, which was used to train the recommended models. We understand that including this demographic information in the training data may result in biased outcomes. As such, any findings and predictions from this project will be interpreted with the understanding of the potential effect the biased models may have on stakeholders. The conclusions from this project are not intented to be shared with the general public and are likely not representative of the truth. Rather, it is purely academic work to try and understand the relationship between demographics and transit insecurity, and to explore how this problem may be addressed with machine learning methods. 

## Running the Project and Getting Started
1.  Download *ahs2017n.csv* from this Googe Drive folder: https://drive.google.com/drive/folders/15649B-cW7-rvLvS6K0zMiRDctqWqiH7-?usp=sharing. Ensure that it is in your working folder. 
2.  Ensure the following essential packages are installed: pandas, numpy, sklearn, seaborn, matplotlib, yellowbrick
3.  Clean data using *data_cleaning.ipynb*, which should generate an output file named *occupied_features_clean.csv*. Relevant features and their metadata is listed in *data_dictionary.md*. If you are interested in running the model training notebooks, ensure that this output file is in the same working folder. If you are interested in looking at some data visualizations, this is where you can visit *data_viz.ipynb*. 
4.  The following notebooks are associated with each question and are independent of each other: *Q1_TransCostLoad.ipynb*, *Q2_InsecurityMetrics.ipynb*, *Q3_UnsupervisedLearning.ipynb*

## Project Details
### Problem Description/Context
Transit insecurity is defined as the inability to travel in a “safe and timely manner” because of lacking “materials, economic, or social resources” [1]. This predominantly affects marginalized communities (e.g., low-income, elderly, POC), and usually affects their neighborhoods [2]. Transit insecurity is measured through various indicators such as cost burden of transportation, transit availability, and commuting times to key places like work, school, and medical appointments [3]. We were interested in this topic because public transportation is important to us - we use it every day, and when it works well it can be beneficial to everyone in society. However, when it does not work well, it can be pretty harmful and prevent people from accessing opportunities and perpetuating inequality.

With this topic, we address three questions listed below to see the feasibility and performance of using census data to understand transit insecurity. If useful insights are able to be uncovered by this data, then it would be a useful method to get information crucial for designing policies related to transportation. 

### Key Questions to Answer
> **Question 1**: Can census data be used to build a regression model that  predicts transportation cost load (% of household income that goes to transportation) and what factors within the census data significantly influence transportation costs?


> **Question 2**: Can census data be used to build a regression model that accurately predicts non-finance related transportation insecurity and what factors within the census data significantly influence insecurity?


> **Question 3**: Can clustering analysis of census data effectively identify distinct demographic groups with different transportation accessibility and security levels?

### Dataset
Data is the American Housing Unit survey. Original webpage is listed here:  https://www.census.gov/programs-surveys/ahs/data/2017/ahs-2017-public-use-file--puf-/ahs-2017-national-public-use-file--puf-.html. This data comes in a CSV file. There is relevant metadata information in an accompanying XLSX file (same link) which goes over the variables and meaning of possible data entries. This data contains household-level information on housing units for the U.S. in 2017. High level variables include housing unit characteristics, rooms/size amenities, heating/air conditioning/appliances, disposal, housing problems, household demographics, housing costs, commuting mode, and annual commuting costs.

For further information on what was included in the model training data, please see *data_dictionary.md*. 

### Models Used and Model Evaluation

> For **Question 1**, the main performance metric will be MSE. It is a regression question and as such, MSE is the most appropriate performance metric. The plan is to start from a simplified base linear model and build on top of it (+ Standardized Data, + Normalized Data, + Sequential Feature Selector, + Regularization (Lasso)), eventually moving to decision tree and ensemble learning methods (Random Forest and Gradient Boosting). The main metric we will use is Test MSE (best = lowest MSE Test), but we will also look at R2 train and R2 test and compare them to gague overfitting. 


> For **Question 2**, the main performance metric will also be MSE for the same above reason. We will also consider R2 to look at overall model fit. The plan is similar as before. 


> For **Question 3**, we will generate an evaluation metrics comparison table where readers can see the general data distribution for different clusters. We will also develop a series of visualizations to identify potential clusters or groups of households that demonstrate unique features that could be used to explain their trasportation preference or security level. We will use the silhouette score to evaluate the clustering model. If possible, we will integrate some supervised learning to the end of my unsupervised learning model and then see if the prediction model can be improved (in this case I will look at metrics such as MSE and accuracy)

### Ethical Consideration

Some ethical considerations related to the problem include:
* Data for prediction in Questions 1 and 2 includes some race and demographic data. This may create biases that ascribe certain outcomes to certain demographic groups.
* Data for feature variables may be limited. This means the algorithm will be biased towards outcomes with many instances in the dataset.
* Some ensemble learning methods would not be transparent. The methods should be transparent and undestandable to users and stakeholders.
* Data contains some very specific information. It's essential to protect individuals' privacy rights and comply with relevant data protection regulations, possibly via anonymizing data. 

### Additional Models

We looked at an additional question instead - please see above for details on Question 3. 

### Policy Implications 
Transportation security is crucial in building a smart city as well as bridging historically disadvantaged communities. In the context of the United States, many communities and neighborhoods suffer from historical redlining and poor development on transit network. This study will inform policy-makers on ways to improve household transportation insecurity by providing insights on both financial and non-financial insecurity, as well as taking an exploratory approach on identifying potential groups with unique transit-related features. 


## References 

[1] “Social Determinants of Health”, National Coordinator for Health Information Technology (ONC), Jan 9, 2021.https://www.healthit.gov/isa/uscdi-data/transportation-insecurity#:~:text=Data%20Element-,Transportation%20Insecurity,social%20resources%20necessary%20for%20transportation. [Accessed: March 1, 2024]. 

[2]  D. Carrol, “Transit inequity increased during pandemic”, CMU Engineering News, Jan 7, 20224. https://engineering.cmu.edu/news-events/news/2022/01/07-transit-inequality.html. [Accessed: March 1, 2024]. 

[3] “Transportation Insecurity Analysis Tool”, U.S. Department of Transportation, n.d.  https://www.transportation.gov/priorities/equity/justice40/transportation-insecurity-analysis-tool. [Accessed: March 1, 2024]. 
