
# Operationalizing Machine Learning

This project is part of the Udacity Azure ML Nanodegree. In this project, I used Azure Machine Learning Studio to create and deploy a machine learning model and consumed its endpoint. I also created, published and consumed a pipeline.

The dataset used to create the model is called **Bank Marketing Data Set** and contains data about marketing campaigns (phone calls) of a Portuguese banking institution. 

It contains 20 input variables related to bank client, last contact information, social and economic attributes and other attributes. The goal is to predict if the client will subscribe a term deposit with the bank. More details can be find at [this link](https://archive.ics.uci.edu/ml/datasets/Bank%20Marketing#).

The best performance model was a VotingEnsemble obtained with the execution of AutoML which resulted in 0.94661 of accuracy. The following 2 images shows the best model obtained by AutoML execution and other models which were evaluated by it:

![Best AutoML model](/docs/deploying_best_model.png?raw=true "Best AutoML model")

![Best AutoML models](/docs/automl_pipeline_models.png?raw=true "AutoML models")

## Architectural Diagram

The following image demonstrate tools and Azure product used during this project:

![Architectural Diagram](/docs/architectural-diagram.png?raw=true "Architectural Diagram from the project")

A Computer Instance was created and used to execute a notebook. This notebook uses azure sdk to create and manipulate computer clusters, experiments, models and other contents. At least other three external tools (Python, docker and Apache Benchmark) are used to generate end point documentation, to test and evaluate deployed models use.


## Key Steps

The following image and sections demonstrates all key steps executed during this project:

![Key Steps](/docs/key_steps_project2.png?raw=true "Key Steps from the project")

1. Authentication (Optional): 

This step involves creating a Service Principal account and associate it with your specific workspace. This was not necessing because Udacity lab was used during the entire project development.

2. Automated ML Experiment:

The first thing necessary to start this step was to create the dataset and the 


3. Deploy the best model:
4. Enable logging:
5. Swagger Documentation:
6. Consume model endpoints:
7. Benchmark endpoint:
8. Create and publish a pipeline:

## Screen Recording

The following video demonstrates the model and pipeline deployment process and the model endpoint test:

[![Video demonstrating the deployed model](https://img.youtube.com/vi/8Wsxr50wCiw/0.jpg?raw=true)](https://www.youtube.com/watch?v=8Wsxr50wCiw)

## Standout Suggestions

