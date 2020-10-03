
# Operationalizing Machine Learning in Azure

In this project we use the Bank Marketing dataset to showcase how you we can use AutoML for training, deploying the best model, creating an endpooint and publishing the subsequent created pipeline . The classification goal is to predict if the client will subscribe to a term deposit with the bank on the basis of client specific festueres like age, job, marital status, education, housing, loan etc"

We got our best performing model through AutoML. LughtGBM performed the best giving an accuracy of 95.404. 

## Architectural Diagram
![alt text](https://github.com/SudhakarGoyal/Azure-ML/blob/master/screenshots/architecture.png)

The first and foremost step is to create a workspace which is shown at the cetre of the architecture as well. Using a compute instannce for training, testing and deployment of the model is also an important and next step in the pipeline. Training of the model after having loaded the dataset follows next. The best trained model is considered for deployment which creates an endpoint with REST endpoint url along with Swagger.json file. We also enable the app_insights to visualize any server requests or server response time. Next the pipeline is published. 

## Key Steps
THe important stpes in the completion of an end to end model deplyment scenario involves the following steps

1) Authentication of user for use of Azure
2) Creation of a machine learning workspace for carrying out ML related work
3) Creation of a compute instance for training, testing and deployment in which we have options to choose Cpu/ GPU with various options for RAM and cores 
4) Next is the training process for training the model using auto ml
5) The best model is tested and validated. If the performance is fine on the test set, the model can be used for deployment
6) The best model is deplpyed and an endpoint is created.
7) Enabling the app_insights to check the server response and server queries 
8) Creation of a pipeline and publishing the same.
9) The overall process also requires downlaoding of the swagger.json file which is used to check the output of the deployed model in the localhost. Also the REST APi url is also used and consumed for endpoint verifcation and authentication.

## Screen Recording
https://drive.google.com/file/d/1M5PrW2VsOoinjGfSkwo0QO0gK5q7LPgb/view?usp=sharing
It is a long one as udaicty required pretty much everything with audio as well.

## Standout Suggestions
I believe data transformtion should be tried and tested. We haven't really done data exploration which is an important data pre processing step. Finding correlation between data and then either forming more or less feature columns is the key to better performance. 
Also coversion of model is ONNX for deplying/ using models for other frameworks can also be a point for an overall architecture improvement.
