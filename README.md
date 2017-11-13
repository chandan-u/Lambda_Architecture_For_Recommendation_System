
# About:

An implementation of Recommendation system using Lambda Architecture.

Lambda Architecture design helps in deploying production/real time predictive models. This kind of architecture gives the best of batch and stream processing of data.

This project imitates/mimic production scenario of recommender-systems.

## batch

Code for batch processing

## speed

Code for stream processing

## serving

API exposed to the end user

## Transformations

Each transformation peipleline can be defined by exetending etl.pipline.BasePipeLine

## Scripts

Scripts that process data/play with it are placed in the scripts folder

## Datasets

This is created by the piplelines where result dataset is generated


## Sheduler:

For the now the dag should be triggered externally. Dag's can be scheduled by enabling start_time in default_args or throug CLI



# Setup

**NOTE: This code requires python version 3.5. Not tested for other versions**


## Steps to configure Airflow

export AIRFLOW_HOME = ~/airflow/


## install Requirements:

pip install -r requirements.txt



## Configure ~/airflow/airflow.cfg

dags_folder = /<project-location>/dags/


## Steps To run Airflow server:


airflow webserver -p 8080
airflow scheduler
airflow worker


# steps to run the pipeline


## Using Airflow
airflow trigger_dag ETLPipeLineForMovieLensData

  (or)    

## Using python
python dags/ETL_MovieLensData_pipeline.py    


# A look at the airflow UI:


default address: localhost:8080

## DAG Tree of all the executions of the pipeline

![DAG Tree Image](/docs/img/DAG_tree.png?raw=true)







# Pending tasks/future points
