
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

The following image and sections demonstrates all key steps executed during this project. Most of the steps were executed using the [notebook](/udacity-project.ipynb):

![Key Steps](/docs/key_steps_project2.png?raw=true "Key Steps from the project")


1. Authentication (Optional): 

This step involves creating a Service Principal account and associate it with your specific workspace. This was not necessing because Udacity lab was used during the entire project development.


2. Automated ML Experiment:

The first thing necessary to start this step was to create a experiment, register the dataset and create a computer cluster to run AutoML Experiment. The initial cells from the [notebook](/udacity-project.ipynb) and the images bellow demonstrates this process:

![Registered Dataset](/docs/registered_dataset.png?raw=true "Registered Dataset")

After these first creations, a pipeline to execute AutoML Experiment was created using the notebook. Some cell from the [notebook](/udacity-project.ipynb) and images bellow shows the running process and the results from it.

![AutoML Running](/docs/automl_pipeline_running.png?raw=true "AutoML Running")

![AutoML Completed](/docs/automl_pipeline_completed.png?raw=true "AutoML Completed")


3. Deploy the best model:
When the AutoML Experiment completed, the best model was checked using the [notebook](/udacity-project.ipynb) and Azure MAchine Learning Studio. Using the "Deploy" button, the best model was deployed (yes, it is that simple).

The images bellow shows the status from the model after pressing Deploy Button:

![Model deployment after Deploy Button Pressed](/docs/deploying_best_model.png?raw=true "Model deployment after Deploy Button Pressed")

![Model deployment process](/docs/deploying_best_model_2.png?raw=true "Model deployment process")


4. Enable logging:

Both [notebook](/udacity-project.ipynb) and [logs.py script](/logs.py) were used to enable and print logs as showed in the image bellow:

![logs.py running results](/docs/logs_py_results.png?raw=true "logs.py running results").

The option "Enable app insight" could be confirmed accessing the model details as showed by the following image:

![Best model with enabled app insights](/docs/best_model_with_app_insights.png?raw=true "Best model with enabled app insights").


5. Swagger Documentation:

From the deployed model it is possible to generate a swagger documentation. This helps client applications from the endpoint to understand on how to use urls to access and receive results to sent payload. The swagger documentation was created and viewed using docker and [serve.py script](/swagger/serve.py). The image bellows shows the swagger docker image running, [serve.py script](/swagger/serve.py) running to serve [swagger.json](/swagger/swagger.json) static file and Swagger UI showing the content.

![Swagger Documentation](/docs/swagger-documentation.png?raw=true "Swagger Documentation").


6. Consume model endpoints:




7. Benchmark endpoint:

After the best model was deployed and tested using [endpoint.py python script](endpoint.py), the apache benchmark tool was used to evaluate the healthy and performance from the model. The following image and the file [/benchmark/benchmark-output.txt] demonstrates output from the tool execution.

![Apache benchmark tool](/docs/apache-benchmark-output.png?raw=true "Apache benchmark tool")


8. Create and publish a pipeline:

At the end of the project, the pipeline used to run the AutoML Experiment was used to pubish a pipeline. This publish operation was done using the [notebook](/udacity-project.ipynb) and its result is demonstrated by the following images:

![Pipeline after deployment completition](/docs/pipeline_endpoint.png?raw=true "Pipeline after deployment completition")

![Pipeline after deployment completition](/docs/pipeline_endpoint_2.png?raw=true "Pipeline after deployment completition")

## Screen Recording

The following video demonstrates the model and pipeline deployment process and the model endpoint test:

[![Video demonstrating the deployed model](https://img.youtube.com/vi/8Wsxr50wCiw/0.jpg?raw=true)](https://www.youtube.com/watch?v=8Wsxr50wCiw)

## Standout Suggestions

