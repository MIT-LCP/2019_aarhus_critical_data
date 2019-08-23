# Aarhus Critical Care Datathon 2019

## Data Access

Participants of the Datathon are added to the Google Group `aarhus-critical-2019-participants`. Members of this group have access to computation resources through the Google Cloud Platform (GCP) project `aarhus-critical-2019-team` and to datasets via the GCP project `physionet-data`.

You can access the datasets directly on GCP:
1. [Create a free account on GCP](cloud.google.com)
2. [Open `aarhus-critical-2019-team` in the console](https://console.cloud.google.com/home/dashboard?project=aarhus-critical-2019-team)
3. [Open BigQuery](https://console.cloud.google.com/bigquery?project=aarhus-critical-2019-team)
4. Run a query. E.g. count the number of hospital admissions:

   ```SQL
   SELECT count(*)
   FROM `physionet-data.mimiciii_clinical.admissions` 
   ```

## Tutorial Notebooks

You can open the following tutorial notebooks on Colab and get started instantly. Requirements for these notebooks are: (1) you have a Google account, and (2) your Google account has been added to the `aarhus-critical-2019-participants` Google group.

### eICU-CRD
* [01-accessing-the-data.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/eicu/01-accessing-the-data.ipynb)
* [02-explore-patients.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/eicu/02-explore-patients.ipynb)
* [03-severity-of-illness.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/eicu/03-severity-of-illness.ipynb)
* [04-summary-statistics.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/eicu/04-summary-statistics.ipynb)
* [05-prediction.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/eicu/05-prediction.ipynb)

### MIMIC-III
* [mimic-iii-tutorial-aarhus.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/mimic-iii/mimic-iii-tutorial-aarhus.ipynb)

### MIMIC-CXR
* [mimic-cxr-train-aarhus.ipynb](https://colab.research.google.com/github/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/mimic-cxr/mimic-cxr-train-aarhus.ipynb)

## R 

Datasets can also be queried directly from R. This is exemplified in the following R markdown notebook: [mimic-iii-los-aarhus.Rmd](https://github.com/MIT-LCP/2019_aarhus_critical_data/blob/master/tutorials/mimic-iii/mimic-iii-los-aarhus.Rmd)

## Accessing MIMIC-CXR

The dataset used in the MIMIC-CXR tutorial is preprocessed for optimal use with [Tensorflow](https://www.tensorflow.org/). If you use a different library or just want a simpler representation of the data, the MIMIC-CXR dataset is available as JPEG images and CSV tables in the following GCP bucket: `gs://physionet-data-mimic-cxr-jpg`
