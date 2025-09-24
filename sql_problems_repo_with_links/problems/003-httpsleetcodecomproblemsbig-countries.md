# Problem Big Countries
🔗 [View Problem](https://leetcode.com/problems/big-countries/)

> Source: `SQL_100_Unique_Problems.xlsx`

## Problem Statement

You are given a table named `World` with the following structure:

| Column Name | Type    |
|------------|---------|
| name       | varchar |
| continent  | varchar |
| area       | int     |
| population | int     |
| gdp        | bigint  |

- `name` is the primary key.  
- Each row contains information about a country: its name, continent, area, population, and GDP.  

**Goal:** A country is considered **big** if:  
1. It has an area of at least 3,000,000 km², **or**  
2. It has a population of at least 25,000,000.  

Write a query to find the `name`, `population`, and `area` of the big countries. Return the result in any order.

## Schema / Sample Data

`World` table:

| name        | continent | area    | population | gdp          |
|------------|-----------|---------|------------|--------------|
| Afghanistan | Asia      | 652230  | 25500100   | 20343000000  |
| Albania     | Europe    | 28748   | 2831741    | 12960000000  |
| Algeria     | Africa    | 2381741 | 37100000   | 188681000000 |
| Andorra     | Europe    | 468     | 78115      | 3712000000   |
| Angola      | Africa    | 1246700 | 20609294   | 100990000000 |

## Expected Output

| name        | population | area    |
|------------|------------|---------|
| Afghanistan | 25500100   | 652230  |
| Algeria     | 37100000   | 2381741 |

## Solution

```sql
SELECT name, population, area
FROM World
WHERE area >= 3000000 OR population >= 25000000;
```

## Explanation
The goal of this problem is to select a name,population and area of the country from world whose area >= 3000000 or  population >= 25000000.The query uses a select statement to retrieve all the columns and WHERE condition with OR to combine two clauses.

---

### Status
- `status:` Completed
- `completed_on:24-09-25` 
- `difficulty:Easy` 
- `tags:database` 
