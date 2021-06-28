# Learn some points about Google Big Query


## Let's get started!

This guide presents some concepts about Google Big Query.

**Time to complete**: About 10 minutes

Click the **Start** button to move to the next step.

## Set the GCP Project

Pick up your project

<walkthrough-project-setup></walkthrough-project-setup>

Run the following command in Cloud Shell to confirm that you are authenticated:

```bash
gcloud auth list
```

If it is not, you can set it with this command:

```bash
gcloud config list project
```

```bash
gcloud config set project <PROJECT_ID>
```

## Load Sample Data to BigQuery

Create a dataset to contain your tables.

What is a dataset?
A BigQuery dataset is a collection of tables. All tables in a dataset are stored in the same data location. You can also attach custom access controls to limit access to a dataset and its tables.

Create a dataset
In Cloud Shell, use the bq mk command to create a dataset called "bq_sandbox."

```bash
bq mk bq_sandbox
```

```bash
bq load \
    --source_format=CSV \
    --skip_leading_rows=1 \
    bq_sandbox.place_name \
    ./place_name.csv \
    place_name:string,state_name:string
```


## Query the data

Now that your data is loaded, you can query it by using the BigQuery web UI, the bq command, or the API. Your queries can join your data against any dataset (or datasets, so long as they're in the same location) that you have permission to read.

```bash
bq query --nouse_legacy_sql '
SELECT * 
FROM `bq_sandbox.place_name`
'
```

## Congratulations

<walkthrough-conclusion-trophy></walkthrough-conclusion-trophy>

You’re all set!

You can now explore more functionalities from BigQuery


