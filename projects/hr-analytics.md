[← Portfolio](../README.md) · [Notebook and data](https://github.com/jaychitransh007/HR_Analytics)

# HR analytics: exploring employee attrition

An early exploratory Python notebook examining how attrition appears alongside employee satisfaction, workload, tenure, department, and salary categories.

## The question

What differences appear between employees recorded as having left and employees recorded as having stayed? The notebook uses descriptive summaries and plots to explore that question.

## What is in the repository

| File | Purpose |
| --- | --- |
| [`HR Analytics.ipynb`](https://github.com/jaychitransh007/HR_Analytics/blob/master/HR%20Analytics.ipynb) | Data loading, inspection, visual exploration, and categorical preprocessing. |
| [`HR_Processed_data.xlsx`](https://github.com/jaychitransh007/HR_Analytics/blob/master/HR_Processed_data.xlsx) | The processed workbook read by the notebook. |

The notebook imports NumPy, pandas, Matplotlib, and Seaborn. It compares recorded attrition with variables including satisfaction, average monthly hours, time spent at the company, and salary categories. Later cells encode categorical columns for further analysis.

## How to explore it

Read the notebook on GitHub to inspect its saved outputs, or open it locally in Jupyter with the workbook alongside it. Local execution needs Python, Jupyter, the analysis libraries, and an Excel reader compatible with the selected pandas version.

This is a historical learning notebook. Its saved Python metadata and plotting APIs reflect that period; a modern environment may need compatibility changes. No fresh execution or predictive-model evaluation is claimed here.

## Interpretation and limitations

The written observations concern associations in this dataset. They do not establish why a particular person left, causal effects of working conditions, or a basis for individual employment decisions. The original README attributes the data to IBM, but the exact source, license, and preprocessing history need verification before making a stronger provenance claim.

The value of this project is the visible exploratory workflow: inspect data, compare groups, visualize patterns, and distinguish an observation from a conclusion requiring stronger evidence.
