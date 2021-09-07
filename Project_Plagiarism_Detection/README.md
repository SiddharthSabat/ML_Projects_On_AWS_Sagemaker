# AWS SageMaker Deployment Project
# Plagiarism Project, Machine Learning Deployment using AWS Sagemaker

### Project Overview
This project is part of my Udacity Machine Learning Engineer nando degree. The objective of the project is to build and deploy a plagiarism detector on **AWS Sagemaker** that examines a text file and performs binary classification; labeling that file as either plagiarized or not, depending on how similar the text file is to a provided source text (from Wikipedia).

Amazon SageMaker is a fully-managed service that enables data scientists and developers to quickly and easily build, train, and deploy machine learning models at any scale. Amazon SageMaker includes modules that can be used together or independently to build, train, and deploy the machine learning models

### Project Outline
This project is broken down into three main notebooks:

**Notebook 1: Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.

**Notebook 2: Feature Engineering**
* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* Select "good" features, by analyzing the correlations between different features.
* Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**
* Upload the train/test feature data to S3.
* Define a binary classification model and a training script.
* Train your model and deploy it using SageMaker.
* Evaluate the deployed classifier.

### Steps to run the Jupyter Notebook on Sagemaker
- Create a notebook instance in AWS Sagemaker
- Open a Jupyter Notebook or Jupyter lab environment.
- Clone the below repository into Sagemaker notebook instance
    - git clone https://github.com/SiddharthSabat/ML_Projects_On_AWS_Sagemaker.git                
- Open the `1_Data_Exploration.ipynb`, `2_Plagiarism_Feature_Engineering.ipynb` and `3_Training_a_Model.ipynb` files on jupiter notebook instance.
    - jupyter notebook 1_Data_Exploration.ipynb
    - jupyter notebook 2_Plagiarism_Feature_Engineering.ipynb
    - jupyter notebook 3_Training_a_Model.ipynb
- Read and follow the instructions! Datasets for the project also can be found in the notebook.

### Libraries Used
This project requires Python >= v3.6, an AWS account with required resources to train, transform, deploy and test Machine learning models on AWS Sagemaker and the following Python libraries :
- [Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html)
- [Python 3.7](https://www.python.org/downloads/release/python-370/)
- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [Jupyter Notebook](http://ipython.org/notebook.html)

### Delete Deployed Endpoint
In order to avoid any unexpected large bill, the deployed endoints need to be SHUT DOWN as soon the task is completed. Below is the code to shut down the endpoints or can be done on AWS sagemaker UI.

* `predictor.delete_endpoint()`

### Author
* [Sidharth Sabat](https://www.linkedin.com/in/sidharthsabat88/)

### References
* [Amazon SageMaker Wiki](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html)
* [PyTorch Tutorial](https://pytorch.org/tutorials/)