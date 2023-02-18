# ETL-off-a-SQS-Queue

# Your objective is to:
1. read JSON data containing user login behavior from an AWS SQS Queue, that is made
available via a custom localstack image that has the data pre loaded.
2. Fetch wants to hide personal identifiable information (PII). The fields `device_id` and `ip`
should be masked, but in a way where it is easy for data analysts to identify duplicate
values in those fields.
3. Once you have flattened the JSON data object and masked those two fields, write each
record to a Postgres database that is made available via a custom postgres image that
has the tables pre created.
