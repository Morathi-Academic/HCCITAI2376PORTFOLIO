📁 Project Overview

This folder contains two main components:

Deep Learning Lab Write-Up – A detailed explanation of each task performed during the lab involving the VGG16 pre-trained deep learning model.

Project File(s) – Supporting code/notebooks used during the lab to load images, preprocess data, run predictions, and analyze how input changes affect the model’s behavior.

Together, they document the workflow of using a pre-trained convolutional neural network (CNN) for image classification and provide insights into deep learning model sensitivity.

🧠 Lab Summary — Using VGG16 for Image Classification
1. Introduction

The lab introduces the basics of deep learning workflows using the VGG16 model. The goal was to understand how pre-trained models process images, make predictions, and react to variations in input.

2. Overview of the Pre-Built Model

The VGG16 model (pretrained on ImageNet) was loaded.

Its architecture includes:

Multiple convolutional layers

Max-pooling layers

Fully connected layers

Reviewing the model helped develop an understanding of how neural networks extract features and classify images.

3. Data Loading and Preprocessing

Key preprocessing steps observed:

Resizing images to 224 × 224

Converting the image to a numerical array

Expanding dimensions to simulate a batch

Normalizing pixel values

An initial FileNotFoundError (missing sample.jpg) reinforced the importance of valid input data. A test elephant image provided by Keras was used instead.

4. Making Predictions

Using the interactive widget, an image was uploaded and passed to the VGG16 model.

Example initial result:

Top prediction: African elephant (~93% confidence)

Other predictions: Tusker, Water buffalo with much lower probabilities

This confirmed the model’s strong performance on standard, clear images.

5. Understanding Predictions with Image Modifications

The lab demonstrated how modifying an image affects predictions.

After rotating/enlarging the original image, the model returned:

[('n02437616', 'llama', 0.091),
 ('n02113799', 'standard_poodle', 0.072),
 ('n02488702', 'colobus', 0.060)]


Interpretation:

The confident elephant prediction disappeared.

Confidence dropped significantly (~9% top probability).

Misclassification occurred due to changes in orientation and scale.

This showed:

Pre-trained models are highly sensitive to deviations from the training distribution.

Proper preprocessing and image consistency are essential for reliable predictions.

6. Conclusion

From this lab, we learned that:

Pre-trained CNNs like VGG16 perform well on standard images.

Data preprocessing (resizing, normalization, formatting) is crucial.

Even simple modifications (rotation, scaling, noise) can disrupt predictions and reduce confidence.

Understanding model behavior helps diagnose errors and improve model robustness.

7. Feedback & Assessment

Feedback:

The lab was interactive and clearly demonstrated the capabilities of pre-trained models.

Uploading images and viewing predictions was engaging.

The only minor issue was the missing “sample.jpg,” easily resolved using Keras' built-in image.

Assessment of Understanding:

Confident in explaining VGG16’s architecture and feature extraction process.

Understand the importance of preprocessing pipelines.

Able to interpret prediction outputs and explain why transformed images cause misclassification.