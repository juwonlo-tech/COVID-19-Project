# COVID-19 Project
## Project to predict mortality from COVID-19

The effects of the COVID-19 pandemic have hit every nation and individuals differently. In Canada, the COVID-19-related mortality rate is 1.1%. Since the mortality rate for COVID-19 is very low, it is exceedingly challenging for healthcare professionals to follow up with all the patients who tested positive for the virus due to the daily increase in the number of people testing positive for COVID-19 and limited hospital capacity.  

With the advancement of machine learning technology using historical data, we can predict those that are at high risk of dying due to the virus. This will inform the level of priority given to the care of such individuals. In addition, there has been a lot of misunderstanding regarding the impact of COVID-19 on various age groups and genders. Using data provided by Statistics Canada and some programming, some observations were made and noted.
### The data
The dataset has 2 files which were previewed. They both contain the same data, but df1 is categorical while df2 holds the numerical values which are directly annotated representations of the categories.

Dataset link: https://www150.statcan.gc.ca/n1/pub/13-26-0003/132600032020001-eng.htm

df1 preview:

<img width="902" alt="Screen Shot 2022-09-22 at 1 52 21 PM" src="https://user-images.githubusercontent.com/77176412/191828252-bc678642-320c-456d-9e56-621b6831f30b.png">


df2 preview:

<img width="908" alt="Screen Shot 2022-09-22 at 1 52 50 PM" src="https://user-images.githubusercontent.com/77176412/191828353-aa8bd707-b416-4e8f-b3b0-0e2be9cfa1fd.png">


### Data visualization
Using the df1 dataframe, various questions were answered using the data to examine the distribution of the virus and fatality by Age group, gender, region, and other features.

<img width="960" alt="Screen Shot 2022-09-22 at 1 54 22 PM" src="https://user-images.githubusercontent.com/77176412/191828661-492e0989-2fe3-4c5d-896e-e32a0f68bd18.png">


<img width="960" alt="Screen Shot 2022-09-22 at 1 55 48 PM" src="https://user-images.githubusercontent.com/77176412/191828930-6aaba027-6226-4196-986b-ce58b5a628ab.png">


<img width="958" alt="Screen Shot 2022-09-22 at 1 56 54 PM" src="https://user-images.githubusercontent.com/77176412/191829158-a823c499-6c9f-4f95-bd33-baea5dcff8f6.png">


### Prediction Model Development
The data was split into training and test sets in ratio 70:30.
5 models were created to predict if a person will die or not based on their status in these categories:' Asymptomatic', 'Age group', 'Gender', 'Hospital status', 'Occupation', 'Region', 'Transmission'. The most important features that determine death are the person's age group, hospital status (if they were hospitalized or in the ICU), and if they were asymptomatic. 
The feature importance was determined using a correlation matrix and ExtraTreesClassifier().

<img width="958" alt="Screen Shot 2022-09-22 at 1 57 39 PM" src="https://user-images.githubusercontent.com/77176412/191829339-9788b131-540a-4530-a205-1f8c91d6c871.png">

Confusion matrix for each of the 5 models and their respective accuracy scores are included in the notebook.

### Conclusion
The 5 models and their accuracy score are as follows:
   - Logistic Regression - 98.09%
   - Decision Tree - 98.17%
   - Random Forest - 98.18%
   - K-Nearest Neighbour - 98.08%
   - Support Vector Machine - 98.14%
   
The Random Forest is the most accurate model for predicting mortality in this instance closely followed by the decision tree. A system such as this can help health care workers to identify the patients with the highest risk of death and therefore prioritize their care. While the 98.18% accuracy looks very good, the error rate of 1.82% may be a bit of a concern for the healthcare sector considering human lives are in view. 

The jupyter notebook for this project is available on: https://github.com/juwonlo-tech/COVID-19-Project/blob/main/Covid%20Project.ipynb
