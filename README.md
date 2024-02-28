# Intro to Machine Learning with Snowpark ML for Python

## Overview

This quickstart guide introduces the integration of Snowpark for Machine Learning within Snowflake, demonstrating how to set up both Snowflake and Python environments to build an end-to-end ML workflow. This includes everything from feature engineering to model training and deployment using Snowpark ML, leveraging the power of Snowflake for ML tasks without data movement.

## Step-By-Step Guide

### Setting up the Snowflake Environment

- Run the SQL commands found in `setup.sql` within a Snowflake SQL worksheet to prepare your Snowflake resources, including the creation of a warehouse, database, schema, and stages for model assets.

### Setting up the Python Environment

1. **Environment Setup**: Use Miniconda or another Python environment manager to set up an environment with Python 3.9 or higher.

    - Download Miniconda from [here](https://conda.io/miniconda.html).
    - Create and activate the conda environment:

        ```bash
        conda env create -f conda_env.yml
        conda activate snowpark-ml-hol
        ```

    - Optionally, start a Jupyter notebook server:

        ```bash
        jupyter notebook &> /tmp/notebook.log &
        ```

2. **Prepare Your Connection Configuration**:

   - Update `connection.json` with your Snowflake account details, including the account name, user name, and password.

   **Important**: For security reasons, do not commit `connection.json` with your real credentials to Git. Instead, use placeholders or environment variables, and keep your actual credentials secure.

### Running the Notebooks

- **Data Ingestion**: `1_snowpark_ml_data_ingest.ipynb` guides you through cleaning and ingesting the diamonds dataset into Snowflake.

- **Feature Transformations**: `2_snowpark_ml_feature_transformations.ipynb` demonstrates Snowpark ML Modeling API's capabilities for data transformation.

- **Model Training and Inference**: `3_snowpark_ml_model_training_inference.ipynb` shows how to train an XGBoost model and execute batch inference through Snowpark Model Registry.

## About Snowpark and Snowpark ML

**Snowpark** offers libraries and runtimes for securely processing Python code in Snowflake, including:

- **Client-Side Libraries** for code development and deployment.
- **Elastic Compute Runtimes** for secure code execution in Snowflake using Python, Java, and Scala.

**Snowpark ML** focuses on end-to-end ML workflows, enabling:

- **Feature Engineering and Model Training** with popular Python ML frameworks directly in Snowflake.
- **Model Management and Batch Inference** through the Snowpark Model Registry, supporting scalable and secure model management.

## Advantages of Using Snowpark ML

- **No Data Movement**: Perform ML tasks within Snowflake, ensuring data security and governance.
- **Streamlined Model Management**: Manage ML models with versioning and role-based access control, suitable for both Python and SQL users.
- **Scalable and Secure**: Leverage Snowflake's computing power for efficient ML workflows.

## Getting Started

- Begin with setting up your Snowflake environment as per the instructions in `setup.sql`.
- Follow the steps to configure your Python environment securely.
- Proceed with the Jupyter notebooks to explore feature engineering, model training, and inference within the secure and scalable framework of Snowpark ML.

## Credits

This project builds upon the invaluable hands-on labs and materials provided by Snowflake. For more resources and examples, visit [Snowflake Labs on GitHub](https://github.com/Snowflake-Labs), and [Snowflake Documentation](https://docs.snowflake.com/en/developer-guide/snowpark-ml/index).
