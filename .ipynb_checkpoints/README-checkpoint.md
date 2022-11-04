# Mini-project IV - Loan Predictor

### [Assignment](assignment.md)

## Project/Goals
The objective of this project was to create a Supervised Machine Learning model that would streamline Loan Applications and to return a result from the AWS cloud. The goals were to clean, analyse and engineer features for a dataset that contained information collected from an online loan application form and to create an app that could be called from the cloud.

## Hypothesis
My hypotesis is that applicants with higher education level are more likely to get a loan. I tested this through descriptive statistics and comparative plotting.

## EDA 
In my first notebook you will find my EDA where I obtained some insight into the data and identified patterns. Immediately we see that all three monetary features were skewed and contained vaying amounts of outliers. I saw that there were more applicants who were childless, married men, who were graduates, but not self employed wiht a credit history. There were also more successful loan applications than not.

From the boxplots we can more clearly see the outliers. Here are a few patters I noticed:
- Non-Graduate people who successfully got the loan have the same mean (Gender didn't make a difference)
- Male Graduates have a higher Loan Amount than Women Graduates
- Low variance in mean Loan Amount from Women (regardless of education or loan success)

- Self-Employed Graduates have the highest Loan Amount (successful)
- Non-Self-Employed non-grads have the lowest loan Amount (successful)
- High variance in mean Loan Amount for Self-Employed Graduates (successful loans vs non-successful)
- Self-Employed people, regardless of education or success of loan, have higher Loan Amounts

- Rejected loans from rural and semi-urban areas have a higher mean than the successful loans (regardless of education)
- Urban areas have less variance for successful and unsuccessful mean Loan Amounts
- Rural and semi-urbaners are asking for larger loans, but being approved for around the same amounts as urban areas.

- Urban Graduates have a very steady mean Loan Amount (regardless of success or not)

- More graduates apply for loans than non-grads. 70.8% of graduates are successful with their loan applications, only 61.2% of non-grads are successful

## Process

### EDA
Explored the data through descriptive statistics, various plots, and pivot tables
### Pre-Processsing
Data cleaning included imputing missing values. Feature Enginnering inlcuded adding a Total Income feature, applying a log transformation to features with extreme values (Loan Amount, Total Income), and OneHot Encoding categorical values. 
### Model and Pipeline
I chose a Random Forest Classifier as my model. I created a pipeline to include all pre-processign steps for efficiency. I then used Grid Search to fine tune the Random Forest Model.
### Deployment
I then saved my model to a pickle file and created an app python file to be deployed to the AWS cloud. Once deployed the scoring results of the model could be testing within my notebook. 

## Results/Demo
My model's best performance had a score of 0.77. 

## Challanges 
I struggled with custom functions that could be added to my pipeline.

## Future Goals
The target data was slightly skewed, as there were more successful applicants than not. It may be worth considering applying techniques for an unbalanced dataset. 

If I had more time I would implement my custom functions to my pipeline.