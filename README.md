﻿# TelcoChurn

### __Understanding the Problem__
_What is Customer Churn?_

> It refers to the rate of attrition at which the customers stop doing business with an entity. In our case, we are interested in finding out the customers who discontinue their subscription services from our telecoms industry.

With this in mind, the report aims to go through the following specific objectives, which shall also serve as guide in the structure of our report:

1. __Define the Problem.__ Measure the customer churning problem at hand in terms of churn rate and revenue churned.
2. __Identify Causes for Churning.__ Determine the causes and intention of customers to discontinue their services.
3. __High-Value Customers vs Churned Customers.__ The former are highly valuable and loyal to the company for their large contribution to revenue generation. An assessment among these two customer types can be conducted to find out how churned customers can be effectively and prospectively converted to high-value customers.
4. __Propose Recommendations.__ Provide recommendations that are consistently valid and justified in line with Steps 2 and 3.

### Dataframe

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Customer ID</th>
      <th>Gender</th>
      <th>Age</th>
      <th>Married</th>
      <th>Number of Dependents</th>
      <th>City</th>
      <th>Zip Code</th>
      <th>Latitude</th>
      <th>Longitude</th>
      <th>Number of Referrals</th>
      <th>...</th>
      <th>Payment Method</th>
      <th>Monthly Charge</th>
      <th>Total Charges</th>
      <th>Total Refunds</th>
      <th>Total Extra Data Charges</th>
      <th>Total Long Distance Charges</th>
      <th>Total Revenue</th>
      <th>Customer Status</th>
      <th>Churn Category</th>
      <th>Churn Reason</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0002-ORFBO</td>
      <td>Female</td>
      <td>37</td>
      <td>Yes</td>
      <td>0</td>
      <td>Frazier Park</td>
      <td>93225</td>
      <td>34.827662</td>
      <td>-118.999073</td>
      <td>2</td>
      <td>...</td>
      <td>Credit Card</td>
      <td>65.6</td>
      <td>593.30</td>
      <td>0.00</td>
      <td>0</td>
      <td>381.51</td>
      <td>974.81</td>
      <td>Stayed</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0003-MKNFE</td>
      <td>Male</td>
      <td>46</td>
      <td>No</td>
      <td>0</td>
      <td>Glendale</td>
      <td>91206</td>
      <td>34.162515</td>
      <td>-118.203869</td>
      <td>0</td>
      <td>...</td>
      <td>Credit Card</td>
      <td>-4.0</td>
      <td>542.40</td>
      <td>38.33</td>
      <td>10</td>
      <td>96.21</td>
      <td>610.28</td>
      <td>Stayed</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0004-TLHLJ</td>
      <td>Male</td>
      <td>50</td>
      <td>No</td>
      <td>0</td>
      <td>Costa Mesa</td>
      <td>92627</td>
      <td>33.645672</td>
      <td>-117.922613</td>
      <td>0</td>
      <td>...</td>
      <td>Bank Withdrawal</td>
      <td>73.9</td>
      <td>280.85</td>
      <td>0.00</td>
      <td>0</td>
      <td>134.60</td>
      <td>415.45</td>
      <td>Churned</td>
      <td>Competitor</td>
      <td>Competitor had better devices</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0011-IGKFF</td>
      <td>Male</td>
      <td>78</td>
      <td>Yes</td>
      <td>0</td>
      <td>Martinez</td>
      <td>94553</td>
      <td>38.014457</td>
      <td>-122.115432</td>
      <td>1</td>
      <td>...</td>
      <td>Bank Withdrawal</td>
      <td>98.0</td>
      <td>1237.85</td>
      <td>0.00</td>
      <td>0</td>
      <td>361.66</td>
      <td>1599.51</td>
      <td>Churned</td>
      <td>Dissatisfaction</td>
      <td>Product dissatisfaction</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0013-EXCHZ</td>
      <td>Female</td>
      <td>75</td>
      <td>Yes</td>
      <td>0</td>
      <td>Camarillo</td>
      <td>93010</td>
      <td>34.227846</td>
      <td>-119.079903</td>
      <td>3</td>
      <td>...</td>
      <td>Credit Card</td>
      <td>83.9</td>
      <td>267.40</td>
      <td>0.00</td>
      <td>0</td>
      <td>22.14</td>
      <td>289.54</td>
      <td>Churned</td>
      <td>Dissatisfaction</td>
      <td>Network reliability</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 38 columns</p>
</div>

##### __1. Define the Problem__
An __revenue loss of 3.68M__ (accounting for 17% of the total revenue) is expected due to __customer churn rate of 26.54%__ (1869 out of 7043 customers). There appears to be significantly more churn among low spending customers.

##### __2. Identify Causes for Churning__
Row labels attributed to customers who 'Joined' will not be included for analysis in order to reduce noise in the visualizations while allowing for effective visual contrast between customers who 'Churned' and those who 'Stayed'.

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/72eaa3c6-34a0-4bf6-9310-ccbedfe4d8cc)

##### Exploratory Data Analysis

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/f92c5e76-ac9c-4142-b84f-1f25e8812624)

__Insights__
* `tenure_in_months`: Customer churn rate is highest within the first few months (5) of subscribing to the service.
* `total_charges and revenue`: In relation to their short duration of subscription, total amount charged to churned customers are relatively low compared to those who stayed, hence, lower revenue garnered.

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/28f3fdc2-6093-4189-9de9-28884a60b036)

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/7a426ffa-9661-44fa-b6f0-5ac8b3a70e96)

__Insights__
* `offer`: Most customers didn't accept marketing offers. The marketing team may want to improve on this low conversion rate. Unfortunately, no information were provided about the complete details of each offer, although we do observe high customer churn rate after subscribing to Offer E.
* `internet_service`. Higher churn rate with subscriptions to internet service. Anecdotally, there are several causes related to internet services that can lead to customer dissatisfaction. One of the most frequent examples include slow internet conncetion.
* `internet_type`: Of the various internet connection types, Fiber Optic is the most popular, for it had the fastest download and upload speeds compared to cable and DSL at the expense of higher prices. However, Fiber Optic users are also the most likely to discontinue the connection service.
* `contract`: It makes sense that contracts set for longer timeframes either up to one or two years discourage the subscribers to discontinue their service. On the contrary, users are likely to churn if they opt to pay at a monthly basis.
Subsribing to any of the additional internet services (i.e. online security, backup, device protection plan, etc.) appears to considerably reduce the customer churn rate by a certain percentage.

##### __3. High-Value Customers vs Churned Customers__
Customers who contributed above the average revenue of the company and those who stayed are treated as high-value and loyal customers.

##### __High-Value Customers Profile__

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/9cacd7b0-95ee-4f5d-b3fd-ff30ca42d26c)

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/af92e102-f7be-4049-a2a8-fc1933f0fd34)

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/bbfc3e9b-861c-47a4-bf7b-1010c1a86ffd)

![image](https://github.com/arduinto/TelcoChurn/assets/142419799/9d9aa38f-72b3-4805-a587-df8cc832d049)

##### Assessment of the Customer Groups
__High Value Customers Profile__

* 67.73% are married.
* They haven't purchased __Offer E__.
* More than half of these customers have subscribed to additional __internet services__ (i.e. backup, security, protection plan, tech support) and __streaming services__ (TV, movies, music).
* Out of the __81.66%__ who are subsribed to long term contracts, 50.39% opted for the two-year contract, and the remaining __31.27%__ went for one year.

__Churned Customers Profile__

* Only 35.79% are married.
* __Offer E__ appears to be the most popular offer around churned customers. Perhaps the company may want to review and look for potential pain points about this offer.
* More than half of churned customers haven't subscribed to additional __internet services and streaming services__.
* __88.55%__ choose to pay their bills at a monthly basis.

__What they have in common?__

* Equal distribution in terms of gender.
* __Fiber optic__ internet service is popular among both customer groups.
* Majority enjoy __unlimited data__.
* Majority prefers to receive __paperless billing__ and pay the bills by __bank withdrawal__.

##### __4. Propose Recommendations__
1. __Concentrate marketing efforts on the highest valuable customers__ (top 33% of the customers). This specific group of customers are known for being big spenders and their loyalty to the company. Consider creating an exclusive loyalty program filled with exclusive rewards just for them.
2. The most common cause for churning is due to the __superiority of the competitors' brand offers and services in terms of price and quality__. This underscores the company's attention to review the components of its value proposition and define its competitive advantage over competitors.
3. __Converting current month-to-month users to long term contract subscribers have been statistically shown to reduce the customer churn rate__. Amplify the conversion rate by providing content about the key functional benefits of applying for the subscription model.
4. __Attractively introduce the additional internet and streaming services to internet users__. There is a higher chance that they will retain and become high value customers after purchasing these add-on offers.
5. __Consider reviewing Offer E and identify its pain points which resulted in high churn rates__. Carefully assess across other related marketing offers that performed well and make pertinent changes and improvements out of it.
