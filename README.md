# Case Study Document: Danny's Diner

**Prepared by:** Vijay Adithya B K

**Experience:** 3 Years as Data Analyst

**Portfolio:** [Your Portfolio Link]

# Pizza Runner Case Study

## Introduction

Did you know that over 115 million kilograms of pizza is consumed daily worldwide? (According to Wikipedia, anyway!)

Danny, inspired by the fusion of 80s retro styling and pizza delivery, founded **Pizza Runner**. To make it stand out, Danny combined the concept with Uber-like delivery operations. He recruited runners and invested in a mobile app to accept orders from customers.

### Available Data

Danny, being a data scientist, understood the importance of data collection for his business growth. He has provided us with a database schema and raw datasets to clean and analyze.

### Entity Relationship Diagram

![ERD](https://github.com/VijayAdithyaBK/Pizza_Runner/blob/main/pizza_runner_erd.png)

Below is the structure of the database schema used for this case study:

- **runners**: Details about each runner and their registration date.
- **customer_orders**: Captures pizza orders, including exclusions and extras.
- **runner_orders**: Tracks order assignments, cancellations, and delivery details.
- **pizza_names**: List of available pizzas.
- **pizza_recipes**: Ingredients used for each pizza.
- **pizza_toppings**: Details of each topping and its ID.

---

## Schema Overview

### Table 1: `runners`
| runner_id | registration_date |
|-----------|-------------------|
| 1         | 2021-01-01        |
| 2         | 2021-01-03        |
| 3         | 2021-01-08        |
| 4         | 2021-01-15        |

### Table 2: `customer_orders`
| order_id | customer_id | pizza_id | exclusions | extras | order_time           |
|----------|-------------|----------|------------|--------|----------------------|
| 1        | 101         | 1        |            |        | 2021-01-01 18:05:02 |
| 2        | 101         | 1        |            |        | 2021-01-01 19:00:52 |
| ...      | ...         | ...      | ...        | ...    | ...                  |

### Table 3: `runner_orders`
| order_id | runner_id | pickup_time         | distance | duration  | cancellation          |
|----------|-----------|---------------------|----------|-----------|-----------------------|
| 1        | 1         | 2021-01-01 18:15:34| 20km     | 32 minutes|                       |
| 2        | 1         | 2021-01-01 19:10:54| 20km     | 27 minutes|                       |
| ...      | ...       | ...                 | ...      | ...       | ...                   |

### Table 4: `pizza_names`
| pizza_id | pizza_name    |
|----------|---------------|
| 1        | Meat Lovers   |
| 2        | Vegetarian    |

### Table 5: `pizza_recipes`
| pizza_id | toppings               |
|----------|------------------------|
| 1        | 1, 2, 3, 4, 5, 6, 8, 10|
| 2        | 4, 6, 7, 9, 11, 12     |

### Table 6: `pizza_toppings`
| topping_id | topping_name  |
|------------|---------------|
| 1          | Bacon         |
| 2          | BBQ Sauce     |
| ...        | ...           |

---

## Case Study Questions

The case study is divided into multiple focus areas:

### A. Pizza Metrics
1. How many pizzas were ordered?
2. How many unique customer orders were made?
3. How many successful orders were delivered by each runner?
4. How many of each type of pizza was delivered?
5. How many Vegetarian and Meat Lovers pizzas were ordered by each customer?
6. What was the maximum number of pizzas delivered in a single order?
7. For each customer, how many delivered pizzas had at least 1 change and how many had no changes?
8. How many pizzas were delivered that had both exclusions and extras?
9. What was the total volume of pizzas ordered for each hour of the day?
10. What was the volume of orders for each day of the week?

### B. Runner and Customer Experience
1. How many runners signed up for each 1-week period?
2. What was the average time in minutes for each runner to arrive at the Pizza Runner HQ?
3. Is there a relationship between the number of pizzas and how long the order takes to prepare?
4. What was the average distance traveled for each customer?
5. What was the difference between the longest and shortest delivery times?
6. What was the average speed for each runner?
7. What is the successful delivery percentage for each runner?

### C. Ingredient Optimization
1. What are the standard ingredients for each pizza?
2. What was the most commonly added extra?
3. What was the most common exclusion?
4. Generate a descriptive order item for each record in the `customer_orders` table.
5. Generate an alphabetically ordered, comma-separated ingredient list for each pizza order.
6. What is the total quantity of each ingredient used in all delivered pizzas?

### D. Pricing and Ratings
1. How much revenue has Pizza Runner made without additional charges?
2. How much revenue has Pizza Runner made if there is a $1 charge for extras?
3. Design a ratings system and generate a schema for this dataset.
4. Combine delivery data, customer ratings, and other metrics into a single table.
5. Calculate the profit after deducting runner fees.

### E. Bonus Challenges
1. How would the data design change if new pizza options were added?
2. Write an `INSERT` statement for adding a new "Supreme" pizza with all toppings.

---

## Data Cleanup Recommendations

- Handle `NULL` values in the `customer_orders` and `runner_orders` tables.
- Standardize inconsistent data formats for columns like `distance` and `duration`.
- Ensure proper data types are assigned during analysis.

---

## How to Run

### Setup
1. Use PostgreSQL or any SQL platform.
2. Import the schema and data provided into your SQL environment.

### Execution
- Execute SQL queries to answer each case study question.
- Validate outputs with sample data provided.

---

## Conclusion

This case study provides valuable experience in SQL data cleaning, querying, and reporting. It covers various real-world scenarios, including pizza delivery logistics, customer experience, and revenue optimization. Have fun exploring Pizza Runner's data!

---

## Author - Vijay Adithya B K

This project is part of my portfolio, showcasing the SQL skills essential for data analyst roles. If you have any questions, feedback, or would like to collaborate, feel free to get in touch!

- **LinkedIn**: [Connect with me professionally](https://www.linkedin.com/in/vijayadithyabk/)
