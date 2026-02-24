# data-quality-validation-and-hr-data-integration

## Overview
This project focuses on the `high-stakes data challenges of a company merger`. The `goal` was to `validate` and `integrate` a messy employee dataset from a newly acquired firm into a parent company’s database while maintaining compliance and `data integrity/quality`.

Using Python (Pandas), I identified and resolved critical anomalies—including extreme age outliers (e.g., 136 years old) and negative employment durations—that would have otherwise skewed corporate reporting and benefits eligibility. The final pipeline successfully merged 93 validated records, ensuring a consistent, single source of truth for the integrated organization.

## Methods and Discussions
### Data Profiling and Quality Dimensions
Before integration, I created a [data quality plan]() `addressing the importance of data quality for stakeholders`.

I evaluated the acquired firm’s data against the six dimensions of data quality (Accuracy, Completeness, Consistency, Timeliness, Validity, and Uniqueness). My primary focus was on Accuracy and Completeness to ensure the integration did not corrupt the parent company's master records.

## Requirements
You will need the following to run this project:
1. Pandas
2. Python
3. Numpy
4. Jupyter Notebook
5. Datasets listed below

### Dataset
This projects uses two data soruces
1. The parent company dataset: This is the "clean" set of data that holds our companies current employee data.
2. New firms dataset: This is a messy dataset holding the new firm's data.

### How to Run
1. Clone the repository
2. Prepare the data and ensure the csv files are in the directory of the notebook
3. Open a Jupyter Notebook IDE run cells as needed





