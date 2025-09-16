Question 1
Scenario:

This function is supposed to return the square of a number but isn’t working properly.
Prompt Copilot to fix it.

Starter Code:

def square(x):
    return x * x + 1  # Bug here
print(square(5))

Question 2:

ncorrect Factorial Calculation

Scenario:

This function is supposed to return the factorial of a number but gives the wrong result.
Prompt Copilot to fix it.

def factorial(n):
    result = 0
    for i in range(1, n + 1):
        result *= i
    return result

print(factorial(5))  # Expected 120


SQL Injection Vulnerability

Scenario:

This code builds a SQL query unsafely.
Prompt Copilot to refactor using parameterized queries to prevent SQL injection.

import sqlite3

def get_user_data(username):
    conn = sqlite3.connect("users.db")
    cur = conn.cursor()
    query = f"SELECT * FROM users WHERE username='{username}'"  # Vulnerable
    cur.execute(query)
    return cur.fetchall()

print(get_user_data("admin' OR '1'='1"))
