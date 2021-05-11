# Dog Breed Image Classification via Convolutional Neural Networks

## Introduction

53% of Americans households include a dog, creating a huge market and need for canine care products. A strong dog image classification model can have many applications including creating more custom/personalized product recommendations to pet parents. Dog classification would also allow for more personalized marketing of these products. 

Additionally, a dog image classification model could be a tool to help identify lost dogs and help reunite them with their owners through facial recognition.

Barking Data Inc. would like to develop this model in order to sell the various applications that will come out of it to pet product companies, veterinary offices, animal rescues and other companies who may benefits from these tools.

To begin the development of the model we will eventually sell, we will start by building a model using the 50 most popular dog breeds. Additionally, we will generate our own dataset using Selenium to scrape Google Images.

## Data Sources

Notebooks 1 and 2 concentrate on scraping Google Images for images of the top 50 dog breeds to develop our own dataset. 

In later notebooks, we combine our original dataset with the Stanford Dog dataset. This can be downloaded [here](https://render.githubusercontent.com/http://vision.stanford.edu/aditya86/ImageNetDogs/). Be sure to rename the downloaded folder to "stanford-dog-Images". For simplicity, we also narrowed the Stanford dataset to dog breeds only included in our original list of top 50 dog breeds. Because some of the dog breeds did not exist in the Stanford dataset, we remain with 37 breeds. We're including this list below for quicker reproduction. Please only keep these folders (and re-name them accordingly) in the "stanford-dog-Images" dataset. Finally, add this folder to the repo.

**Dog breed list**

* Basset Hounds
* Beagles
* Belgian Malinois
* Bernese Mountain
* Bloodhounds
* Border Collies
* Boston Terriers
* Boxers
* Brittanys
* Chesapeake Bay Retrievers
* Chihuahuas
* Cocker Spaniels
* Doberman Pinschers
* English Springer Spaniels
* French Bulldogs
* German Shepherd
* German Shorthaired Pointers
* Golden Retrievers
* Great Danes
* Labrador Retrievers
* Maltese
* Mastiffs
* Miniature Schnauzers
* Newfoundlands
* Pembroke Welsh Corgis
* Pomeranians
* Poodles
* Pugs
* Rhodesian Ridgebacks
* Rottweilers
* Shetland Sheepdogs
* Shih Tzu
* Siberian Huskies
* Vizslas
* Weimaraners
* West Highland White Terriers
* Yorkshire Terriers

## Notebook Guide

1. Dataset Creation via Google Image Scrape  - Clean.ipynb
    * Google Image webscrape via Selenium
2. Image Organization.ipynb
    * Image organization into sub-folders to prepare for modeling. 
3. Baseline Model.ipynb
    * Baseline Model
4. CNN Models.ipynb
    * CNN Model development (multiple models gridsearch, tuning, etc.)
5. CNN Pre-Trained Model.ipynb
    * VGG19 and Inceptionv3
6. Combining Data with Stanford Dogs Dataset.ipynb
    * The Stanford Dog dataset is added to our existing images in order to increase our sample size for better model performance. 
7. Step by Step CNN Model.ipynb
    * A simple CNN model is built and tuned in a step-by-step fashion. Our final model is generated in this notebook.

## Results

## Conclusions & Next Steps

The best model generated is Model 4 from our last notebook - the original dropout regularization model. The accuracy of this model was 55% for our training data and 53% for our test data. Loss was roughly 1.8 for both groups. 

While some of our other models demonstrated greater accuracy, like Model 5 which had an ~86% accuracy, all of our models demonstrated more overfitting.

* Increase the size of our dataset. We saw strong improvements after combining our data with the Stanford Dog dataset.
* Test leveraging K-fold cross validation to improve our model. This may help prevent some of the overfitting we're seeing.
* Once we have an improved model, we should try to expand our model to provide predictions for mixed-breed dogs. 
