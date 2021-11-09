#### *Sql_HW_6 which is related to Unit 7*

![Focus on Fraud](Images/credit_card_fraudster.jpg)

# Looking for Suspicious Transactions

This file accompanies Visual Data Analysis notebook being provided to my FinTech Company CFO.

## Goal of This Notebook 
The goal of these analysis tools is to provide information about possible fraud patterns.

### Part I - Vidual Data Analysis

Fraudsters sometimes make several small transactions on a credit card in order to avoid being caught. I isolated those transactions for each cardholder in Sql using the groupby function, and counted the number of transactions for each cardholder. Here are those results:

| ccd_owner_id | number_ignored |
|--------------|----------------|
| 1            | 10             |
| 2            | 11             |
| 3            | 3              |
| 4            | 16             |
| 5            | 14             |
| 6            | 6              |
| 7            | 18             |
| 8            | 15             |
| 9            | 3              |
| 10           | 20             |
| 11           | 21             |
| 12           | 26             |
| 13           | 19             |
| 14           | 9              |
| 15           | 12             |
| 16           | 19             |
| 17           | 4              |
| 18           | 19             |
| 19           | 22             |
| 20           | 18             |
| 21           | 4              |
| 22           | 7              |
| 23           | 16             |
| 24           | 22             |
| 25           | 16             |

Several of the cards do have a large number of those transactions. The card holders with the most small transactions are # 12, # 19 and # 24. The high quantities of small transactions for those card holders suggests that their cards have been hacked. 

The remaining questions in this section are still under investigation.

### Part II - Visual Data Analysis of Fraudulent Transactions

Regarding the transactions of customers with cardholder ids of 2 and 18, their transaction activity over the months in question is plotted here:

![Cardholder 2 Transactions](Images/CH%202%20Trns.png)
![Cardholder 18 Transactions](Images/CH%2018%20Trns.png)

To better contrast the two sets of activity, their plotted together in this diagram:

![Both Cardholders Compared](Images/Both%20CH.png)

My conclusion from the data is that cardholder 2 seems to have only regular transactions, while the transaction record of cardholder 18 does show suspicious spikes. I would suggest that all apppropriate measures be taken by cardholder 18. 

Regarding the transactions of the customer with cardholder id of 25, the date is provided in a boxplot as seen below:

![Cardholder 25 Transactions](Images/CH%2025.png)

From this information, it does appear that her card was used for an expensive purchase once in January, and then again in March. Also in April, May, and multiple times in June. I suggest that she definitely take measures to secure that credit card account as soon as possible. 

Additional measures for fraud detection - including standard deviation analysis and quartile review - are being pursued for further investigations. Results will be provided as soon as possible. 

# Technical Notes

## Libraries
This Jupyter Lab notebook utilizes the following libraries:

os

Pandas

Numpy

dotenv

JSON

Pathlib

Alpaca Trade API

MCForecastTools

matplotlib

## Data Inputs

Besides the elements related to those libraries, additional data to be input by the user includes their currency holdings, their stocks and bonds amounts, and their monthly income amounts.  

# Acknowledgements

I would like to first acknowledge the guidance and teaching of our FinTech Boot Camp Instructor, Garth Mortensen, our TA, Alejandro Esquivel, and out Student Success Manager, Angelica Baraona. I also found the collective Stack Overflow wisdom essential as ever. Regarding postgreSQL and PGAdmin4 overall I utilized information from codemy and the tech website collective in general. In dealing with a new environment combining PyViz and Sql, the RealPython.com's Vritual Environments Primer was interesting. Finally, the SQL books were helpful as I continued my learning process.

