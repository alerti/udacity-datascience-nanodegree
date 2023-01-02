# Starbucks-Capstone-Challenge


[Medium Blog post](https://medium.com/@mukunzialex47/facts-about-starbucks-offers-15dbcf3d2c8e)

----
# Problem Statement

```Project goals```<br>
Combine transaction, demographic, and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks sells dozens of products.


```Plan:```<br>
✔ Explore and Visualize the Data.<br>
✔ Apply Quick Data Analysis.<br>
✔ Preprocess the data.<br>
✔ Scale the numerical features.<br>
✔ Train Supervised Learning Models.<br>
✔ Evaluate the models using the chosen metric (Accuracy)- then choose the best model among them.<br>
✔ If there are improvement needs, implement GridSearchCV to find the best parameters (to improve the performance of the chosen model).<br>


# Data Sets

The data is contained in three files:

* portfolio.json - containing offer ids and metadata about each offer (duration, type, etc.)
* profile.json - demographic data for each customer
* transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

**portfolio.json**
* id (string) - offer id
* offer_type (string) - the type of offer ie BOGO, discount, informational
* difficulty (int) - the minimum required to spend to complete an offer
* reward (int) - the reward is given for completing an offer
* duration (int) - time for the offer to be open, in days
* channels (list of strings)

**profile.json**
* age (int) - age of the customer 
* became_member_on (int) - the date when the customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

**transcript.json**
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours since the start of the test. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record


`Metrics`
* To evaluate our model's performance, we will use accuracy. This Metric was chosen for the following reasons :
* Since we have a simple classification problem, i.e. either: 
  * offer viewed
  * offer completed.

* It enables us to recognize HOW WELL our model is predicting by comparing the number of correct predictions with the total number of predictions ( the concept of accuracy).

### Data and definitions

### profile.json
Rewards program users (17000 users x 5 fields)

* gender: (categorical) M, F, O, or null
* age: (numeric) missing value encoded as 118
* id: (string/hash)
* became_member_on: (date) format YYYYMMDD
* income: (numeric)

### portfolio.json
Offers sent during the 30-day test period (10 offers x 6 fields)

* reward: (numeric) money awarded for the amount spent
* channels: (list) web, email, mobile, social
* difficulty: (numeric) money required to be spent to receive a reward
* duration: (numeric) time for the offer to be open, in days
* offer_type: (string) BOGO, discount, informational
* id: (string/hash)

### transcript.json
Event log (306648 events x 4 fields)

* person: (string/hash)
* event: (string) offer received, offer viewed, transaction, offer completed
* value: (dictionary) different values depending on event type
  * offer id: (string/hash) not associated with any "transaction"
  * amount: (numeric) money spent in "transaction"
  * reward: (numeric) money gained from "offer completed"
* time: (numeric) hours after start of the test

## File structure
```
Starbucks-Capstone-Challenge/
├── data/
│   ├── portfolio.json
│   ├── profile.json
│   └── transcript.json
├── pic1.png
├── pic2.png
├── README.md
├── Starbucks_Capstone_notebook.html
└── Starbucks_Capstone_notebook.ipynb
```

### Insights
In this Project, I analyzed data sets provided by Starbucks to predict whether a customer would complete the offer or just view it

`Process:`
* Load, analyze and visualize data to get an overall understanding of the data set, data processing took the bigger chunk of the project
* Create latent features; to improve the performance of the model, features extracted from the original existing column:
* Features:
    * age_group
    * income_range
    * member_type

From the quick analysis I managed to garner these insights:
 - Female customers finished ~75% of the offers they viewed, men completed just 58% of the offers they viewed, and female customers finished seeming to be convinced easily
-  On average it takes a customer to complete an offer less than 16 days(~372 hrs)
-  Both gender are interested in BOGOF, they also have similar reactions to informational offers(they seem not to be interested)
-  Gender differences seem not to affect the time to complete an offer, both took 17days to do so
- Most common offer type is BOGO, then discount offers, and informational offers pulling less interest. BOGO seems to be the most attractive compared to others at Starbucks
- There are 2175 missing values, and customers fall into 3 categories ( M — (8484–57%), F — (6129–41%), O— (212))
Customer income ranges : 
— between 30000 and 120000
— most fall between 50,000 and 75000.


The medium article on data analysis can be found in this [medium]


`Acknowledgments and thank you`


 Thank you [Udacity](https://www.udacity.com) & [Starbucks](https://www.starbucks.com/) for the data
 [Bhosle](https://towardsdatascience.com/starbucks-capstone-challenge-35e3b8c6b328)
