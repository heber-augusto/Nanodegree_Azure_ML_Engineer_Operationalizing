
# Operationalizing Machine Learning

This project is part of the Udacity Azure ML Nanodegree. In this project, I used Azure Machine Learning Studio to create and deploy a machine learning model and consumed its endpoint. I also created, published and consumed a pipeline.

The dataset used to create the model is called **Bank Marketing Data Set** and contains data about marketing campaigns (phone calls) of a Portuguese banking institution. 

It contains 20 input variables related to bank client, last contact information, social and economic attributes and other attributes. The goal is to predict if the client will subscribe a term deposit with the bank. More details can be find at [this link](https://archive.ics.uci.edu/ml/datasets/Bank%20Marketing#).

The best performance model was a VotingEnsemble obtained with the execution of AutoML which resulted in 0.94661 of accuracy. The following 2 images shows the best model obtained by AutoML execution and other models which were evaluated by it:

![Best AutoML model](/docs/deploying_best_model.png?raw=true "Best AutoML model")

![Best AutoML models](/docs/automl_pipeline_models.png?raw=true "AutoML models")

## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. An architectural diagram is an image that helps visualize the flow of operations from start to finish. In this case, it has to be related to the completed project, with its various stages that are critical to the overall flow. For example, one stage for managing models could be "using Automated ML to determine the best model". 

## Key Steps
*TODO*: Write a short discription of the key steps. Remeber to include all the screenshots required to demonstrate key steps. 

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
