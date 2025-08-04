To go from beginner to advanced in data engineering within 3 months, you should focus on building proficiency in several core technical areas and reinforce each area with hands-on exercises and projects. Here are the core skills and suggested exercises, organized by theme and mapped to each phase of your learning journey:

**1. Programming Foundations and Computing Basics**
- Skill: Python for data manipulation, scripting, and automation.
- Exercises: 
  - Write Python scripts to parse, clean, and transform CSV and JSON files.
  - Automate small ETL jobs using built-in modules and libraries (like pandas)[1].

**2. Data and Database Fundamentals**
- Skill: SQL mastery for querying and managing data.
- Exercises:
  - Practice SELECT, JOIN, GROUP BY, and window functions on sample datasets.
  - Design and normalize a relational database schema (e.g., in PostgreSQL or MySQL)[1][4].
- Skill: Understanding data structures and algorithms.
  - Exercises: Solve classic coding and data structure problems (sorting, searching, hash tables)[1].

**3. Data Modeling & Database Ecosystems**
- Skill: Schema design and data warehousing.
- Exercises:
  - Build a normalized schema with primary/foreign keys.
  - Construct data marts and star/snowflake schemas for analytics[1][5].
- Skill: NoSQL and non-relational databases.
  - Exercises: Store and query semi-structured data (e.g., documents in MongoDB)[1].

**4. Data Processing (ETL/ELT) and Pipelines**
- Skill: Build data pipelines for extraction, transformation, and loading.
- Exercises:
  - Create an ETL pipeline using pandas (for small data) or PySpark (for bigger data).
  - Schedule and orchestrate batch operations using Python scripts[1][2].

**5. Workflow Orchestration and Automation**
- Skill: Workflow orchestration with tools like Apache Airflow.
- Exercises:
  - Define and run simple DAGs (Directed Acyclic Graphs) in Airflow to automate multi-step ETL[2].

**6. Cloud Platforms and Big Data Tools**
- Skill: Familiarity with storage and compute in AWS, GCP, or Azure.
- Exercises:
  - Upload, query, and manage data in cloud storage (e.g., AWS S3, Google Cloud Storage).
  - Deploy a sample pipeline using managed warehouse services (Redshift, BigQuery)[2][4].
- Skill: Big data processing and distributed computation (Hadoop, Spark).
  - Exercises: Run simple batch and streaming jobs in Spark (local or cloud cluster)[1].

**7. Data Quality, Governance, and Monitoring**
- Skill: Apply practices for data validation, testing, and quality assurance.
- Exercises:
  - Use programmatic checks (e.g., assertions or Great Expectations) within ETL jobs.
  - Monitor pipeline runs and generate basic alerts for failures[1].

**8. Real-World/Portfolio Projects**
- Beginner project: Web scraping and storing results in a database. Clean data and generate summary reports.
- Intermediate project: Build and schedule an ETL pipeline that ingests, validates, transforms, and loads data from multiple sources into a data warehouse.
- Advanced project: End-to-end data platform: Batch and streaming ETL, analytical reporting, and dashboard on cloud infrastructure, with monitoring and version control[1][2][5].

**Summary Table of Core Skills and Example Exercises**

| Core Skill               | Example Exercise                                                 |
|--------------------------|-----------------------------------------------------------------|
| Python fundamentals      | Data cleaning with pandas; file parsing scripts                 |
| SQL                      | Design and query normalized schema; leetcode SQL challenge      |
| Data modeling            | Star schema for reporting; project-based schema design          |
| NoSQL databases          | Store and retrieve JSON docs in MongoDB                         |
| ETL pipelines            | Build batch/streaming jobs with pandas/PySpark                  |
| Orchestration (Airflow)  | Schedule a multi-step ETL workflow as a DAG                     |
| Cloud platforms          | Move data to S3, query with Athena; deploy pipeline on GCP      |
| Big Data tools           | Ability to process 1M+ records with Spark                       |
| Data quality             | Write data validation/assertion unit tests                      |
| Project/Portfolio        | End-to-end pipeline from ingest to analytics dashboard          |

This roadmap ensures a strong foundation, practical experience with orchestration, analytics, and deployment, as well as exposure to modern cloud and Big Data ecosystems, matching what most advanced data engineering roles demand[1][2][3][4][5].

[1] https://www.geeksforgeeks.org/blogs/data-engineering-roadmap/
[2] https://towardsdatascience.com/5-simple-projects-to-start-today-a-learning-roadmap-for-data-engineering-940ecbad6b5f/
[3] https://blog.det.life/a-non-beginner-data-engineering-roadmap-2025-edition-2b39d865dd0b
[4] https://zerotomastery.io/blog/how-to-become-a-data-engineer/
[5] https://www.youtube.com/watch?v=1VBQmmdRQfM
[6] https://www.youtube.com/watch?v=IGraly_Lvvg
[7] https://herovired.com/learning-hub/blogs/data-engineer-roadmap/