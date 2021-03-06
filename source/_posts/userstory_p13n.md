---
title: User Story for personalization
date: 2017-05-20 13:00:45
tags:
---

# Personalization 

 > Personalization is the key to improve the shopper's engagement and loyalty for e-commerce company. 
 > Good data accuracy make sure you can create a better customer experience on individual level.
 
> This article will only focus on how Griffin helps data accuracy check for personalization data

## Data Accruracy

### Problem

In our personalization platform, it stored all customer's profile and behaviour data which generated by site application.
There is no confidence to do any recommendation if can't provide the data accuracy number.

### Challenge

* The data volume is huge, it's not easy to do data comparision except on hadoop.
* There are many different events (view, search, transaction, listing...) need to be validated, expected have
   a simple way to check accuracy for them.
* Spent more time on Data quality job maintainance.

### Solution

Griffin provide batch measure for accuracy, which simplify the process of data accuracy check and run faster than 
Hive scripts.

#### How Griffin applied on Personalization data accuracy check?

Take the viewitem event as an example, here are detail steps to enable accuracy measure by Griffin.

1. Create hive table for source and target data for viewitem event on hadoop system.
2. Create the batch accuracy measure for each behaviour event as this[sample.](https://github.com/apache/incubator-griffin/blob/master/griffin-doc/measure/measure-batch-sample.md)
3. Add the measure and job in Griffin refer to this[guide.](https://github.com/apache/incubator-griffin/blob/master/griffin-doc/service/api-guide.md)
4. Metrics result should be displayed on Griffin UI.





