Customer Segmentation ReadMe
Objective
This project aims to develop a customer segmentation strategy to provide targeted recommendations such as saving plans, loans, and wealth management based on the usage behavior of approximately 9000 active credit card holders over the last 6 months.

Data Description
The dataset provides a customer-level overview with 18 behavioral variables. Key attributes include:

CUSTID: Identification of Credit Card holder (Categorical)
BALANCE: Balance amount left in the account for purchases
BALANCEFREQUENCY: Frequency of balance updates (score between 0 and 1)
PURCHASES: Amount of purchases made from the account
ONEOFFPURCHASES: Maximum purchase amount done in one-go
INSTALLMENTSPURCHASES: Amount of purchases made in installments
CASHADVANCE: Cash in advance given by the user
PURCHASESFREQUENCY: Frequency of purchases (score between 0 and 1)
ONEOFFPURCHASESFREQUENCY: Frequency of one-off purchases (score between 0 and 1)
PURCHASESINSTALLMENTSFREQUENCY: Frequency of purchases in installments (score between 0 and 1)
CASHADVANCEFREQUENCY: Frequency of cash in advance being paid
CASHADVANCETRX: Number of transactions made with "Cash in Advanced"
PURCHASESTRX: Number of purchase transactions made
CREDITLIMIT: Limit of Credit Card for the user
PAYMENTS: Amount of Payment done by the user
MINIMUM_PAYMENTS: Minimum amount of payments made by the user
PRCFULLPAYMENT: Percent of full payment paid by the user
TENURE: Tenure of credit card service for the user
Data Preprocessing
To enhance clustering accuracy, we performed standardization using the StandardScaler to ensure equal importance of variables.

Identified Strong Correlations
Three pairs of strong correlations were observed:

"PURCHASES" and "ONEOFF_PURCHASES" (0.86)
"PURCHASES_FREQUENCY" and 'PURCHASES_INSTALLMENT_FREQUENCY' (0.85)
"CASH_ADVANCE_TRX" and "CASH_ADVANCE_FREQUENCY" (0.81)
Customer Segmentation Results
1. Transactors (Cluster 1)
Characteristics: Customers paying the least interest charges, cautious with money
Features: Lowest balance ($104), cash advance ($303), Percentage of full payment = 23%
2. Revolvers (Cluster 2)
Characteristics: Use credit card as a loan, most lucrative sector
Features: Highest balance ($5000) and cash advance ($5000), low purchase frequency, high cash advance frequency (0.5), high cash advance transactions (16), low percentage of full payment (3%)
3. VIP/Prime (Cluster 3)
Characteristics: High credit limit ($16K) and highest percentage of full payment
Recommendations: Target for increased credit limit and encourage higher spending habits
4. Low Tenure (Cluster 4)
Characteristics: Customers with low tenure (7 years), low balance
This segmentation provides actionable insights for tailored financial product recommendations.

Usage
Download the dataset from the provided link.
Preprocess the data using the described steps.
Apply clustering algorithms for customer segmentation.
Utilize identified segments for targeted recommendations.
Feel free to explore the code and adapt it to your specific needs.
