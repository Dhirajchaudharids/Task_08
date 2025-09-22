# Task_08

Step-by-Step Process

First, I set up a database and an employee table with fields such as name, department, salary, and city. To make the performance test meaningful, I inserted a few sample records and then generated about five thousand rows of additional data. This ensured that the queries would process a large enough dataset to show performance differences.

Next, I ran a query to retrieve employees from a specific city. Without an index, the system performed a full table scan, meaning it had to check every row, which was slower. I then created an index on the city column and re-ran the same query. This time, the database used the index to directly locate the required rows, making the query much faster.

To validate the performance improvement, I used profiling to compare the execution times before and after adding the index. The profiling results confirmed that indexing significantly reduced query execution time.
