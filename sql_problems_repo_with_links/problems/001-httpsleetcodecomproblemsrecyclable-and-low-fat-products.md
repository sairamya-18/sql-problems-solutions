# Problem Recyclable and Low Fat Products: https://leetcode.com/problems/recyclable-and-low-fat-products/

🔗 [View Problem](https://leetcode.com/problems/recyclable-and-low-fat-products/)

> Source: `SQL_100_Unique_Problems.xlsx`

## Problem statement
| Column Name | Type  |
|------------|-------|
| product_id | int   |
| low_fats   | enum  |
| recyclable | enum  |
product_id is the primary key (column with unique values) for this table.
low_fats is an ENUM (category) of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.
recyclable is an ENUM (category) of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.
 

Write a solution to find the ids of products that are both low fat and recyclable.

Return the result table in any order.

The result format is in the following example.

 

## Notes / Hints


## Schema / Sample data
| product_id | low_fats | recyclable |
|------------|----------|------------|
| 0          | Y        | N          |
| 1          | Y        | Y          |
| 2          | N        | Y          |
| 3          | Y        | Y          |
| 4          | N        | N          |

## Expected output

| product_id |
|------------|
| 1          |
| 3          |

## Solution 
```sql
select product_id from Products where low_fats = 'Y' and recyclable = 'Y';
```

## Explanation

In this question, the goal is to select products that are low in fat and recyclable. I used a simple SELECT statement with a WHERE clause combining the two conditions using AND.


### Status
- `status:` Completed
- `completed_on:24-09-25` 
- `difficulty:Easy`
- `tags:` database
