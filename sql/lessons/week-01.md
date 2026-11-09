# Week 1: SQL for FuelzUs Service Jobs

**Pre-reading (20–30 minutes):**
- [SQLBolt: SELECT queries](https://sqlbolt.com/lesson/select_queries_introduction)
- [SQLBolt: WHERE filters](https://sqlbolt.com/lesson/select_queries_with_constraints)

## Business scenario
FuelzUs needs to answer: Which jobs are open? Which service types are completed? Which jobs generate the most revenue?

Dataset: `datasets/sample-data/fuelzus_jobs.csv`. All records are fictional.

## Core concepts
```sql
SELECT job_id, service_type, status
FROM jobs;

SELECT job_id, service_type, revenue_usd
FROM jobs
WHERE status = 'completed';

SELECT job_id, revenue_usd
FROM jobs
ORDER BY revenue_usd DESC;

SELECT COUNT(*) AS completed_jobs
FROM jobs
WHERE status = 'completed';
```

## Wednesday exercises
1. Show all roadside assistance jobs.
2. Find jobs in Rockland County with status `open`.
3. List completed jobs from highest to lowest revenue.
4. Count all completed jobs.
5. Stretch: calculate total completed revenue by service type using `GROUP BY`.

## Deliverable
Save your working queries as `sql/challenges/week-01-answers.sql` after testing them. Record what you learned in `progress-tracker.md`.

## Optional practice
Use SQLite or another SQL environment; import the CSV as a table named `jobs`. Do not claim the example queries ran until you test them.
