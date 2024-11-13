# Loan-Prediction

## Data Dictionary
- **Loan ID:** A unique Identifier for the loan information.
- **Customer ID:** A unique identifier for the customer. Customers may have more than one loan.
- **Loan Status:** A categorical variable indicating if the loan was paid back or defaulted.
- **Current Loan Amount:** This is the loan amount that was either completely paid off, or the amount that was defaulted.
- **Term:** A categorical variable indicating if it is a short term or long term loan.
- **Credit Score:** A value between 0 and 800 indicating the riskiness of the borrowers credit history.
- **Years in current job**: A categorical variable indicating how many years the customer has been in their current job.
- **Home Ownership:** Categorical variable indicating home ownership. Values are "Rent", "Home Mortgage", and "Own". If the value is OWN, then the customer is a home owner with no mortgage
- **Annual Income:** The customer's annual income
- **Purpose:** A description of the purpose of the loan.
- **Monthly Debt:** The customer's monthly payment for their existing loans
- **Years of Credit History:** The years since the first entry in the customer’s credit history
- **Months since last delinquent:** Months since the last loan delinquent payment
- **Number of Open Accounts:** The total number of open credit cards
- **Number of Credit Problems:** The number of credit problems in the customer records.
- **Current Credit Balance:** The current total debt for the customer
- **Maximum Open Credit:** The maximum credit limit for all credit sources.
- **Bankruptcies:** The number of bankruptcies
- **Tax Liens:** The number of tax liens.

  ##  Goals
1. **Business Objective**
    - A financial institution wants us to help them identify customers who have a lesser chance of defaulting on the loan.
    - The company management has asked the data science team to build a predictive model to identify who would be a good customer. Furthermore, they want the team to come up with questions to ask the client, based on the model, when they are applying for loan.
2. **Data Understanding**
    - The dataset resembles a real-world dataset and has many of the same challenges. It has:
    - Missing values
    - Spelling differences
    - Punctuation format
    - Duplicates rows
3. **Data Preparation**
    - Split your data into training and testing
    - Start with Exploratory data analysis
    - Data cleaning
    - Handling the missing values
    - Transform categorical data into numeric
    - Feature Engineering (such as credit utilization)
    - The goal is to clean the dataset and get it ready for the Algorithms
3. **Modeling**
    - Algorithm Selection
    - Depending on the question at hand you can decide which algorithm
    to choose
4. **Classification Question**
    - Pick a classification algorithm
    - Regression based
    - Tree based
    - Distance based
    - Probability based
    - Model Evaluation
    - Evaluation criteria
5. **Modeling:**
    - Pick an algorithm
    - Train the algorithm using training data
    - Evaluate the trained model
    - Use the trained model to predict who is a good customer
    on test data
    - Come up with questions to ask the customer when they
    apply for a loan

  
## Modeling

| Classifier                    | Accuracy Score |
|-------------------------------|----------------|
| Random Forest Classifier      | 0.900403       |
| Decision Tree Classifier      | 0.845341       |
| Gradient Boosting Classifier  | 0.837422       |
| Logistic Regression           | 0.815515       |
| KNeighbors Classifier         | 0.801506       |
| Bernoulli NB                  | 0.690721       |
| Gaussian NB                   | 0.449832       |

Above table shows the accuracy of different classifiers on a dataset:

- **Random Forest (90.04%)** – Highest accuracy, leveraging multiple decision trees to improve predictions.
- **Decision Tree (84.53%)** – Performs well but can overfit without ensemble methods like Random Forest.
- **Gradient Boosting (83.74%)** – Also strong, sequentially improves accuracy but trains slower.
- **Logistic Regression (81.55%)** – Decent baseline, but limited in capturing complex patterns.
- **KNeighbors (80.15%)** – Relies on proximity; good but less robust than other models.
- **Bernoulli NB (69.07%)** – Moderate accuracy; works better with binary/boolean data.
- **Gaussian NB (44.98%)** – Lowest accuracy, likely due to data not fitting Gaussian assumptions.
  
**Random Forest leads, followed by Decision Tree and Gradient Boosting as top performers.**


## Key Questions for Loan Approval Based on Feature Importance

Based on the feature importance shown in the bar chart, we can prioritize questions for the customer that focus on the most influential factors for loan approval. Here’s an interpretation that suggests questions aligned with the top features:

- **Credit Score** - Since credit score is the most significant feature:
    - “What is your current credit score?”
    - “Have you checked your credit report recently for any discrepancies?”
      
- **Current Loan Amount :**
    - “What is the total amount of the loan you are requesting?”
    - “Do you currently have any outstanding loans?”
      
- **Annual Income:**
    - “What is your annual income?”
    - “Are there any additional sources of income?”
      
- **Monthly Debt :**
    - “What is your total monthly debt from all sources (e.g., credit cards, other loans)?”
      
- **Current Credit Balance :**
    - “What is your current balance on credit accounts?”
      
- **Years of Credit History :**
    - “How many years have you had credit?”
      
- **Number of Open Accounts :**
    - “How many credit accounts do you currently have open?”
      
- **Months Since Last Delinquent :**
    - “When was the last time you missed a payment or had a delinquency?”

