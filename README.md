# feedback_pipeline
1.	Load multiple files from URL endpoints
2.	Check for NULLs in customer info columns
3.	Standardize column names
4.	Deduplicate based on user_id, user_name, etc. Assumption - Each user gives feedback only on one product as we product information is not given
5.	Merge datasets
6.	Check again for duplicates + nulls
7.	Save to Parquet, partitioned by source

Probelms:
Some records have null values in the user_id, user_email, and user_name columns because user information is missing. Additionally, each file uses different columns to represent user information.

Databricks Notebook - https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3896924895233349/436592318406451/7978228461053878/latest.html
