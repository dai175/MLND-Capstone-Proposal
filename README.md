# Machine Learning Engineer Nanodegree
## Capstone Proposal
Daisuke Ohba  
May 18th, 2020

## Proposal

### Domain Background

Some breeds have been established by breeders, enthusiasts, breed clubs, etc., as "breed standards" (standards) in order to maintain and reinforce a certain appearance and traits through the generations, and there are hundreds of them.

Until now, we have had to ask an expert to know the exact breed of our dog.
However, with the help of machine learning, which has evolved by leaps and bounds in the last few years, we can easily identify the breed with a single photo of our dog.

This is the assignment that I chose for my Capstone project for "[Udacity Machine Learning Engineer Nanodegree](https://www.udacity.com/course/machine-learning-engineer-nanodegree--nd009t)". ([CNN Project Dog Breed Classifier](https://github.com/udacity/deep-learning-v2-pytorch/tree/master/project-dog-classification))

### Problem Statement

Machine learning is used to identify dog breeds from images of dogs.
Concretely, it outputs the following according to the input image.
* if a dog is detected in the image, return the predicted breed.
* if a human is detected in the image, return the resembling dog breed.
* if neither is detected in the image, provide output that indicates an error.

To identify dog breeds, the machine learning method is classification (supervised).

### Datasets and Inputs

Datasets and Inputs are provided in the [Notebook](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/project-dog-classification/dog_app.ipynb) by Udacity.
We will download and use them.
Also, these are images of dogs or humans, labeled.

### Solution Statement

To solve the problem, we use a type of machine learning, the Convolutional Neural Network (CNN).
This is useful for image recognition.

Specifically, we use a transfer-learned model from the Pre-trained VGG-16 Model.

### Benchmark Model

The CNN model created from scratch.

### Evaluation Metrics

The metrics are "Recall" because the data set may not be balanced.

### Project Design

The workflow is shown in the [Notebook](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/project-dog-classification/dog_app.ipynb) by Udacity.

* Step 0: Import Datasets
* Step 1: Detect Humans
* Step 2: Detect Dogs
* Step 3: Create a CNN to Classify Dog Breeds (from Scratch)
* Step 4: Create a CNN to Classify Dog Breeds (using Transfer Learning)
* Step 5: Write your Algorithm
* Step 6: Test Your Algorithm

We run each step in the Udacity workspace.
It can also be run in sagemaker or locally, if necessary.
