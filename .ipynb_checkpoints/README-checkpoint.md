
# Problem Statement

XYZ Credit Card company regularly helps it’s merchants understand their data better and take key business decisions accurately by providing machine learning and analytics consulting. ABC is an established Brick & Mortar retailer that frequently conducts marketing campaigns for its diverse product range. As a merchant of XYZ, they have sought XYZ to assist them in their discount marketing process using the power of machine learning.

Discount marketing and coupon usage are very widely used promotional techniques to attract new customers and to retain & reinforce loyalty of existing customers. The measurement of a consumer’s propensity towards coupon usage and the prediction of the redemption behaviour are crucial parameters in assessing the effectiveness of a marketing campaign.

The retailer would like to better understand the customer base which will enable the retailer’s marketing team to develop more precise and targeted marketing strategies.


The data available in this problem contains the following information, including the details of a sample of campaigns and coupons used in previous campaigns -

1. **User Demographic Details**
2. **Campaign and coupon Details**
3. **Product details**
4. **Previous transactions**
5. **Item Details**

Based on previous transaction & performance data from the last 18 campaigns, 

(1) identify the population of customers from train who have been a part of 6 or more campaigns and have redeemed a coupon. Using this population as the 'test' population, identify a control group from the remaining population in train.csv.
(2) Classify the customers into 5 or more segments for enabling targeted marketing approaches

### Dataset Description

Here is the schema for the different data tables available. The detailed data dictionary is provided next.

![title](amex19.png)

You are provided with the following files in train.zip:

**train.csv:** Train data containing the coupons offered to the given customers under the 18 campaigns

| Variable          | Definition                                              |
| ----------------- | ------------------------------------------------------- |
| id                | Unique id for coupon customer impression                |
| campaign_id       | Unique id for a discount campaign                       |
| coupon_id         | Unique id for a discount coupon                         |
| customer_id       | Unique id for a customer                                |
| redemption_status | (target) (0 - Coupon not redeemed, 1 - Coupon redeemed) |


**campaign_data.csv:** Campaign information for each of the 28 campaigns

| Variable      | Definition                        |
| ------------- | --------------------------------- |
| campaign_id   | Unique id for a discount campaign |
| campaign_type | Anonymised Campaign Type (X/Y)    |
| start_date    | Campaign Start Date               |
| end_date      | Campaign End Date                 |


**coupon_item_mapping.csv:** Mapping of coupon and items valid for discount under that coupon

| Variable  | Definition                                                     |
| --------- | -------------------------------------------------------------- |
| coupon_id | Unique id for a discount coupon (no order)                     |
| item_id   | Unique id for items for which given coupon is valid (no order) |


**customer_demographics.csv:** Customer demographic information for some customers

| Variable       | Definition                                                                |
| -------------- | ------------------------------------------------------------------------- |
| customer_id    | Unique id for a customer                                                  |
| age_range      | Age range of customer family in years                                     |
| marital_status | Married/Single                                                            |
| rented         | 0 - not rented accommodation, 1 - rented accommodation                    |
| family_size    | Number of family members                                                  |
| no_of_children | Number of children in the family                                          |
| income_bracket | Label Encoded Income Bracket (Higher income corresponds to higher number) |


**customer_transaction_data.csv:** Transaction data for all customers for duration of campaigns in the train data

| Variable        | Definition                                                           |
| --------------- | -------------------------------------------------------------------- |
| date            | Date of Transaction                                                  |
| customer_id     | Unique id for a customer                                             |
| item_id         | Unique id for item                                                   |
| quantity        | quantity of item bought                                              |
| selling_price   | Sales value of the transaction                                       |
| other_discount  | Discount from other sources such as manufacturer coupon/loyalty card |
| coupon_discount | Discount availed from retailer coupon                                |


**item_data.csv:** Item information for each item sold by the retailer

| Variable   | Definition                     |
| ---------- | ------------------------------ |
| item_id    | Unique id for itemv            |
| brand      | Unique id for item brand       |
| brand_type | Brand Type (local/Established) |
| category   | Item Category                  |


**test.csv:** Contains the coupon customer combination for which redemption status is to be predicted

| Variable    | Definition                               |
| ----------- | ---------------------------------------- |
| id          | Unique id for coupon customer impression |
| campaign_id | Unique id for a discount campaign        |
| coupon_id   | Unique id for a discount coupon          |
| customer_id | Unique id for a customer                 |

