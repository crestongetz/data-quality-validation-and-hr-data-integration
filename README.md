# data-quality-validation-and-hr-data-integration

## Overview
This project focuses on the `high-stakes data challenges of a company merger`. The `goal` was to `validate` and `integrate` a messy employee dataset from a newly acquired firm into a parent company’s database while maintaining compliance and `data integrity/quality`.

Using Python (Pandas), I identified and resolved critical anomalies—including extreme age outliers (e.g., 136 years old) and negative employment durations—that would have otherwise skewed corporate reporting and benefits eligibility. The final pipeline successfully merged 93 validated records, ensuring a consistent, single source of truth for the integrated organization.

## Methods and Discussions
### Data Profiling and Quality Dimensions
Before integration, I created a [data quality plan](https://github.com/crestongetz/data-quality-validation-and-hr-data-integration/blob/main/Data%20Quality%20Plan.pdf) to create a governance framework for stakeholders and to introduce them to the importance of data quality.
Following this I made a [Executive Summary Report](https://github.com/crestongetz/data-quality-validation-and-hr-data-integration/blob/main/Executive%20Summary%20Report.pdf) where I evaluated the acquired firm’s data against the six dimensions of data quality (Accuracy, Completeness, Consistency, Timeliness, Validity, and Uniqueness). My primary focus was on Accuracy and Completeness to ensure the integration did not corrupt the parent company's master records.

### Key Anomalies & Resolutions
Using Pandas, I performed a deep dive into the new frims dataset. You can view the [Data Validation Report]() for the full list of findings. Here are some of the critial issues found and resolved:
* Impossible `Outliers` such as an employee with a length of employment of 52,246 days or 136 years. This record was removed as requersted by the stakeholders. This helped prevent the data from being skewed.
* Inconsistent Data such as `Data of Birth columns not matching the age of employees`. Other inststances we found values that where impossible such as `days of employment being negative`. We addressed these by performing cross-validation checks and records that failed to meet these checks where removed as requested from stakeholders to maintain integerity.
* Categorical Standardization: some columns contained mix casing and `standardization for dichotomous variables` such as Yes and yes.
* Schema Alignment: The old firm's dataset had employees full names in one column while our dataset has it in two. We used string splitting logic to create two new columns which let us left join the two datasets.

### Business Impact
By implementing these validation steps, I `prevented dirty data` from entering our dataset. This ensures that downstream processes—such as SOX compliance auditing, benefits eligibility calculations, and workforce diversity reporting—remain accurate and reliable.

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





