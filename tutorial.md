# Learn some points about Google Big Query


## Let's get started!

This guide presents some concepts about Google Big Query.

**Time to complete**: About 10 minutes

Click the **Start** button to move to the next step.

## Set the GCP Project

Pick up your project

<walkthrough-project-setup></walkthrough-project-setup>

## Get Public Data to BigQuery

Create a dataset to contain your tables.

What is a dataset?
A BigQuery dataset is a collection of tables. All tables in a dataset are stored in the same data location. You can also attach custom access controls to limit access to a dataset and its tables.

Create a dataset
In Cloud Shell, use the bq mk command to create a dataset called "bq_load_codelab."

```bash
bq mk bq_load_codelab
```

Next, you will learn how to format the text in a tutorial.


## Writing in Markdown

To write your tutorial, use [Markdown](https://en.wikipedia.org/wiki/Markdown) and follow these guidelines:


### Edit the title

Modify the title of this tutorial ('# Introduction to writing tutorials in Cloud Shell') by changing it to:

```
# Teach me to write a tutorial
```

### Add a new step

Next, add a step just after the title like this:

```
## Step 1
This is a new step I’ve just added.
```

Each 'step' of a tutorial is displayed on one page. To move through steps, users use the 'Back' and 'Next' buttons.


## Congratulations

<walkthrough-conclusion-trophy></walkthrough-conclusion-trophy>

You’re all set!

You can now have users launch your tutorial in Cloud Shell and have them start using your project with ease.


