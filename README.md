# Image-Classification
Auto-immune disorder detection from antinuclear antibody images


## Results

<img width="406" alt="Capture3" src="https://user-images.githubusercontent.com/38533045/218278770-27a8183e-ca8b-47d1-a776-08462f09cd1d.PNG">




### Project Overview:
The project aims to create an accurate, scalable and deployable ML method that predicts ANA specificity for double stranded DNA (dsDNA), use machine learning to discover new staining patterns, help track disease progression/remission, and potentially lead to drug discovery or cell-specific locations for druggable targets



###  Data Source:
Hospital internal data 


### Solution

First step is to predict dsDNA positivity from images, we want to train the model to learn the antibody specificity

We uploaded our pre-processed and de-identified data to the google cloud storage bucket using google cloud SDK utilities (gsutil)
A dataSet file was prepared in csv format which included file names with bucket path, labels, and split specifications. 7500 images were uploaded in total.

Our first aim was to establish baseline performance metrics using AutoML. Once obtained, our goal was to meet or exceed the performance of the AutoML model.

We also wanted to investigate the performance of different model types ranging in complexity from a simple CNN with only 2 convolutional layers to a way more complexed ResNet architecture.

To develop the CNN, we used a Jupyter notebook on a VM instance with n1 machine type with 16 vCPUs and 1 V100 GPU. Once the CNN was roughed in, we tuned hyperparameters using Vertex AI. Once finalized, we submitted a custom training job on Vertex AI.

We also tried transfer learning by implementing MobileNetV2, which is a ResNet architecture. 

Finally, we deployed our AutoML model


## Tools/technologies 

* Google cloud storage fuse
* TFRecords Creation
* Google Cloud Auto ML
* Convolutional neural network
* MobileNetV2








