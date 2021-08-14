# AWS SageMaker Deployment Project
## Creating a Sentiment Analysis Web App for the Movie Review Using PyTorch and SageMaker

### Project Overview

The project aims to deploy a Sentiment Analysis model using RNN on the Amazon AWS SageMaker. Amazon SageMaker is a fully-managed service that enables data scientists and developers to quickly and easily build, train, and deploy machine learning models at any scale. Amazon SageMaker includes modules that can be used together or independently to build, train, and deploy the machine learning models

This project demonstrates entire life cycle of a Machine learning algoritm on Amazon SageMaker platform. The goal of the project is to create a sentiment analysis model using Recurrent neural network using PyTorch. The model is deployed on AWS Sagemaker through lambda function and invoked using an endpoint through public API gateway and finally a simple web interface is created that user interacts and submits the movie reviews, in turn the prediction model behind the scenes will predict whether the review is Positive or Negative. The prediction model is implemented using Pytorch framework and trainned on IMDB dataset.

Below is an architecture of the AWS API Gateway and AWS Lambda functions interacting with the deployed model endpoint is shown.

<img src="Web App Diagram.svg">

### Steps to run the Jupyter Notebook on Sagemaker

- Create a notebook instance in AWS Sagemaker
- Open a Jupyter Notebook or Jupyter lab environment.
- Clone the below repository into Sagemaker notebook instance
    - git clone https://github.com/SiddharthSabat/ML_Projects_On_AWS_Sagemaker.git                
- Open the `SageMaker Project.ipynb` file on jupiter notebook instance.
    - jupyter notebook SageMaker Proejct.ipynb
- Read and follow the instructions! Datasets for the project also can be found in the notebook.

### Project Outline
* Step 1: Downloading the data
* Step 2: Preparing and Processing the data
* Step 3: Upload the data to S3
* Step 4: Build and Train the PyTorch Model
* Step 5: Testing the Model
* Step 6: Deploying the model for testing
* Step 7: Use the model for testing
* Step 6: Deploy the model for the web app
* Step 7: Use the model for the web app

### Libraries Used

This project requires Python >= v3.6, an AWS account with required resources to train, transform, deploy and test Machine learning models on AWS Sagemaker and the following Python libraries :
- [Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html)
- [PyTorch](https://pytorch.org/get-started/locally/) (LSTM classifier)
- [Python 3.7](https://www.python.org/downloads/release/python-370/)
- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [Jupyter Notebook](http://ipython.org/notebook.html)

### Delete Deployed Endpoint
In order to avoid any unexpected large bill, the deployed endoints need to be SHUT DOWN as soon the task is completed. Below is the code to shut down the endpoints or can be done on AWS sagemaker UI.

* `predictor.delete_endpoint()`

### Preview of the Model prediction in Web App

<img src="./Screenshots/Positive Review2.JPG">

### Author
* [Sidharth Sabat](https://www.linkedin.com/in/sidharthsabat88/)

### References
* [Amazon SageMaker Wiki](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html)
* [PyTorch Tutorial](https://pytorch.org/tutorials/)