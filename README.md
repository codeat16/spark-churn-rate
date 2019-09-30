# Spark Machine Learning Analysis for User Churn Rate

This project analyzed data about user's activities for music listening website, and to predict what will lead to user churn, e.g., canceling the service.

## Project Definition

This project is similar to oridinary machine learning classification project except that it uses Spark MLlib to build machine learning models with large datasets, far beyond what could be done with non-distributed technologies like scikit-learn.

## Libraries Used

This project uses Spark as primary tools for the manipulation, analysis and machine learning of the dataset. Specicially, `PySpark` is used, including modules such as `pyspark.sql`, `pyspark.ml`, `pyspark.mllib`. Some basic python modules are also used, including `matplotlib` and `numpy`.

## Motivation

In subscription based service offerings, retaining customer is as important, if not more important than gaining new users. New users acquisition usually have higher cost such as advertiing, coupon offerings. While user retention could have very little cost if done properly. When running subscription based service, the activitiy user interacts with the service, is the best information to peek into how user engage with the service. It could be more accuray and cost effective, than for example, performing a survey. However, the activities usually have a large amount and use a large storage. How to effectively manipulate the data from such a large dataset and extract useful info is a critical skill to get this analysis right.

Spark is a distributed, fast, data platform. It's speed is so impressing that it can provide analysis in real time, e.g., as new data come in. The distributed nature also enable Spark to analyze a much larger dataset that a single machine can handle.

This project demonstrative the data analysis process using Spark.

## Analysis

With some Exploratory Data Analysis, we decided to extract the following data, per user:

- Number of records, e.g., the number of activities user interact with the serivce.
- Number of actions, for each type of action as indicated by page type. For example, how many times the user perform "NextSong", "Add to Playlist", - "Add Friend", and all other actions.
- The average time spent on listening.
- The averge, of total amount of time spent, each day.


## Conclusion

We experimented three machine learning classifiers: Decision Tree, Random Forest, and Gradient-Boosted Tree.

We found Gradient-Boosted Tree has best overall scoring, achieving F1 scores of 0.79 on training and 0.71 for testing.

We also found some activities contribute more to the churn rate. The most importat features activities are: Logout, Daily Averge Length spent on the service, and Thumbs Down.

The important features analysis give additional insight to look for earning warning that user might not be happy about the service, and could be analyed further, to help improve the service to reduce churn rate.

## Files

- `README.md`: this file
- `Sparkify.html`: html verion of the Jupyter Notebook
- `Sparkify.ipynb`: Jupyter Notebook for the analysis and reporting

