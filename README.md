# Churn-Prediction :

This is a group project completed at BeCode Liège. Separate readme are available in the corresponding folders.

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

## Contributors :

- Naci (Data Engineer)

- Meba (Data Analyst)

- Dimitri (ML Engineer - Clustering Part)

- Sébastien (ML Engineer - Classification Part)

## Description

An important financial institution is interested in analyzing its client database to increase the revenue generated from credit cardholders. They are concerned about customers closing their bank accounts after accepting products from other institutions.
The churn rate is above 15% and increasing, the CEO urges the marketing team to start a marketing campaign for client retention.

#### What is Churn Rate ?

_The churn rate, also known as the rate of attrition or customer churn, is the rate at which customers stop doing business with an entity. It is most commonly expressed as the percentage of service subscribers who discontinue their subscriptions within a given time period._

## The Mission

Your data team consists of a data engineer, ML engineer, and data analyst, each of you should collaborate to meet the client requirements:

### Data Engineers

- Build a database from the customer data.
- Deploy an application for the marketing team to predict the churn rate for new client using Docker.
- Create a pipeline that incorporates the work from your colleagues (e.g. deployed app should use the model developed by the ML engineer and dashboard developed by the data analyst).

### ML Engineers

- Predict those clients with more propensity to close their bank account with the financial institution
- Build machine learning models for classification and/or clustering.
- Identify the optimal number of clusters and be able to describe them.
- Find possible groups of clients and define their characteristics alongside the data analyst.

### Data Analysts

- Build a dashboard with data insights and KPIs.
- Clean and explore the data to provide insights to the marketing team and ML engineers.
- Apply some of the tools in Tableau to perform clustering analysis and compare your results with the ML engineers.
- Use the information provided by the ML engineers and your own analysis to create sample client profiles.

### Must-have features

- A fully integrated data pipeline must be created (i.e. data storage, data cleaning, data preprocessing, modeling, visualizations).
- Evaluation of the model's performance and definition of its limitations.
- The dashboard with relevant KPI's is deployed online.
- Results are clearly communicated to client in an business oriented 10 minute presentation.