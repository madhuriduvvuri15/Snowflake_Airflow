This project demonstrates the creation of an ELT (Extract, Load, Transform) pipeline integrating dbt, Snowflake and Airflow. It is designed to streamline the process of data extraction, loading and transformation, providing a robust solution for handling complex data workflows efficiently.

## Project Overview

The pipeline utilizes:
- **Snowflake**: For data warehousing, leveraging its powerful computing capabilities to manage and execute large-scale data operations.
- **dbt (data build tool)**: For transforming data directly in your data warehouse through simple SQL scripts.
- **Airflow**: For orchestrating the pipeline workflows, ensuring that tasks are executed in sequence and at specific intervals.

## Architecture Flow
1. **Data Extraction**: Data is extracted from Snowflake.
2. **Data Transformation**: dbt performs transformations on the staged data in Snowflake to prepare it for analytics.
3. **Scheduling & Monitoring**: Airflow schedules and monitors the workflow, handling dependencies and execution order.

## Setup Instructions

1. **Snowflake Setup**:
   - Configure your Snowflake environment, including the creation of necessary roles (RBAC) and warehouses.
   - Set up database schemas and initial tables required for the pipeline.

2. **dbt Setup**:
   - Install dbt and configure it to connect to your Snowflake account.
   - Define your dbt models and tests in SQL scripts.

3. **Airflow Setup**:
   - Set up an Airflow environment.
   - Configure Airflow to manage workflow orchestration, ensuring connectivity to both dbt and Snowflake.

### Integration

   - Use the dbt profile to establish a connection to Snowflake, ensuring that dbt can execute SQL transformations in the warehouse.
   - Develop Airflow DAGs (Directed Acyclic Graphs) to manage the pipeline tasks. These should define the sequence of operations, starting from data extraction, loading, transformation, and any post-processing steps.

Once setup, trigger your Airflow DAGs to run the pipeline. Airflow's UI can be used to monitor the pipeline's progress and troubleshoot any issues.

## Conclusion

This project template provides a robust scalable framework for building an ELT pipeline with Snowflake, dbt and Airflow, suitable for scalable data operations in modern data environments.
