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

#### Images of dogs
* 8351 images of dogs (train: 6680, test: 836, valid: 835)
* They are stored in folders named by breed, and there are 133 breeds.
* RGB color mode
* The sizes are not uniform, so use them after resizing.

#### Images of humans
* 13234 images of humans (5750 people)
* They are stored in folders named by their name.
* RGB color mode
* The sizes are uniform. (250 x 250)

### Solution Statement

To solve the problem, we use a type of machine learning, the Convolutional Neural Network (CNN).
This is useful for image recognition.

Specifically, we use a transfer-learned model from the Pre-trained VGG-16 Model.
But we can also try other pre-trained networks (Inception-v3, ResNet-50, etc.).

In addition, the images are preprocessed to detect objects before classification.

### Benchmark Model

The CNN model created from scratch.

### Evaluation Metrics

The metrics are "Recall" because the data set may not be balanced.
We can also consider using an "F1 score" to optimize both recall and accuracy.

### Project Design

The workflow is shown in the [Notebook](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/project-dog-classification/dog_app.ipynb) by Udacity.

1. Step 0: Import Datasets  
Download the image datasets for dogs and humans.
2. Step 1: Detect Humans  
Detect human faces in images using OpenCV.
3. Step 2: Detect Dogs  
Detect dogs in images using the Pre-trained VGG-16 Model.
4. Step 3: Create a CNN to Classify Dog Breeds (from Scratch)  
Create a CNN that can classify dog breeds from scratch.
Then we will train and test.
5. Step 4: Create a CNN to Classify Dog Breeds (using Transfer Learning)  
Use Transfer to create a CNN that can identify dog breeds from images.
Then we will train and test.
6. Step 5: Write your Algorithm  
Write an algorithm to solve the problem statement.
The output can be designed freely.
7. Step 6: Test Your Algorithm  
Test the algorithm using any image we like.

We run each step in the Udacity workspace.
It can also be run in sagemaker or locally, if necessary.
