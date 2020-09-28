
# Operationalizing Machine Learning

In this project, I work with the <a href="https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv">Bank Marketing dataset</a>. I will use Azure to configure a cloud-based machine learning production model, deploy it, and consume it. I will also create, publish, and consume a pipeline.

## Architectural Diagram
![Diagram](MlOps.svg)

## Project Main Steps

### Step 1: Authentication

In this step, I create a Service Principal account and associate it with your specific workspace.

![Authentication](screenshots/1.Authentication/1.Service-Principal.png)
![Authentication](screenshots/1.Authentication/2.ml-share.png)


### Step 2: Auto ML Experiment


In this step, I upload the <a href="https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv">bankmarketing_train.csv</a> to Azure Machine Learning Studio so that it can be used when training the model. Then, I use AutoMl to generate models.



![Auto ML Experiment](screenshots/2.AutoML-Experiment/1.dataset.png)
![Auto ML Experiment](screenshots/2.AutoML-Experiment/2.AutoMl-experiment.png)
![Auto ML Experiment](screenshots/2.AutoML-Experiment/3.AutoML-best-Model.png)


### Step 3: Deploy the Best Model

In this step, I deploy the Best Model that will me allow to interact with the HTTP API service and interact with the model by sending data over POST requests.

![Deploy the Best Model](screenshots/3.Deploy/1.Model-deployed.png)
![Deploy the Best Model](screenshots/3.Deploy/2.Model-Endpoint.png)


### Step 4: Enable Logging

In this step, I  enable logging so that logs can be retrieved.

![Enable Logging](screenshots/4.Logs/1.logs.png)
![Enable Logging](screenshots/4.Logs/2.enable-app-insights.png)
![Enable Logging](screenshots/4.Logs/3.Application-insights.png)


### Step 5: Swagger Documentation

In this step, I consume the deployed model using Swagger.

![Swagger Documentation](screenshots/5.Swagger-Documentation/1.swagger.png)
![Swagger Documentation](screenshots/5.Swagger-Documentation/2.POST-template.png)



### Step 6: Consume Model Endpoints

In this step, I use the `endpoint.py` script provided to interact with the trained model.

![Consume Model Endpoints](screenshots/6.Consume-Endpoint/1.prediction.png)
![Consume Model Endpoints](screenshots/6.Consume-Endpoint/2.benchmark.png)
![Consume Model Endpoints](screenshots/6.Consume-Endpoint/3.benchmark.png)



### Step 7: Create and Publish a Pipeline

In this step, I create and publish a pipeline.

![Create and Publish a Pipeline](screenshots/7.PipeLine/1.pipeline-submit.png)
![Create and Publish a Pipeline](screenshots/7.PipeLine/2.pipeline-completed.png)
![Create and Publish a Pipeline](screenshots/7.PipeLine/3.endpoint-published.png)
![Create and Publish a Pipeline](screenshots/7.PipeLine/4.dataset_and_automl.png)
![Create and Publish a Pipeline](screenshots/7.PipeLine/5.pipeline_status.png)
![Create and Publish a Pipeline](screenshots/7.PipeLine/6.widget_details.png)
![Create and Publish a Pipeline](screenshots/7.PipeLine/7.completed_run.png)


## Screen Recording

Here is a screencast showing the entire process of the working ML application.

<a href="https://youtu.be/xAmBY_D7PpY"> Operationalizing Machine Learning screencast</a>

## Future Enhancement
A great future enhancement for me is to connect gitlab with the azure mazchine learning pipeline I have created.