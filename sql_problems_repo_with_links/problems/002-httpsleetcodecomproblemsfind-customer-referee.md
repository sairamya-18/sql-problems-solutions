# Problem Find Customer Referee
🔗 [View Problem](https://leetcode.com/problems/find-customer-referee/)

> Source: `SQL_100_Unique_Problems.xlsx`

## Problem Statement

You are given a table named `Customer` with the following structure:

| Column Name | Type    |
|------------|---------|
| id         | int     |
| name       | varchar |
| referee_id | int     |

- `id` is the primary key.  
- Each row indicates the customer’s id, name, and the id of the customer who referred them (if any).  

**Goal:** Find the names of customers who are either:  
1. Referred by any customer **other than customer with id = 2**  
2. **Not referred by any customer** (i.e., `referee_id` is NULL)  

Return the result table in any order.

## Schema / Sample Data

`Customer` table:

| id | name | referee_id |
|----|------|------------|
| 1  | Will | NULL       |
| 2  | Jane | NULL       |
| 3  | Alex | 2          |
| 4  | Bill | NULL       |
| 5  | Zack | 1          |
| 6  | Mark | 2          |

## Expected Output

| name |
|------|
| Will |
| Jane |
| Bill |
| Zack |

## Solution

```sql
SELECT name
FROM Customer
WHERE referee_id IS NULL OR referee_id != 2;
```

## Explanation
The goal of this problem is to select a name from customer whose referee Id is Null or referee Id is not equal to 2.It uses a select statement with where condition combining the two clauses with OR.

---

### Status
- `status:` Completed
- `completed_on:24-09-25` 
- `difficulty:Easy` 
- `tags:database` 
