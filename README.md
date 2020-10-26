# Deep-Learning-Based-Disease-Prediction-from-Chest-Radiography

Introduction

With approximately 2 billion diagnostic examinations performed annually, chest X-rays are the most widely used medical imaging tool in practice, often 2x-10x more than
other advanced imaging methods such as MRI, CT scans, PET scans. These scans are critical for the screening, diagnosis, and management of many respiratory diseases. However, reading chest X-Rays can be quite an exacting task for radiologists and physicians alike. Our goal of the project is to build a predictive model that helps in detecting respiratory diseases using chest X-ray images. Deep learning technology has demonstrated great success in the medical imaging domain. This project aims at developing a deep learning framework that can detect several different classes of respiratory diseases, given a dataset of chest X-ray images. It’s an interesting Big Data problem because this project involves a dataset of chest X-rays 42 GB large. There is a need to use Machine Learning techniques to analyze such a big dataset on a distributed cluster for effective computation time. The two main research questions that we aim to investigate are: 

(1) How high is the accuracy of the models used?

(2) Given a chest X-ray of a patient, can the model predict multiple diseases if they exist? These questions will help confirm the results radiologists have found and also identify the overlooked data. It can help save patients the hassle of getting further tests done if the application can help doctors find the right disease(s). It can also help physicians recommend necessary tests to confirm if more than one disease is found. This project sees its use in hospitals and diagnostic centers.


Approach:

Our primary goal with this project is to train a machine learning model that can identify diseases using patient radiological data such as x-rays. After carefully examining the
dataset, we found some of the images had multiple disease classes attributed to them. So, we decided that a multi-label classifier(i.e, to predict multiple target labels from
multiple classes for a given input feature) would be more suitable for this project rather than a multi-class classifier(i.e, to predict single target label from multiple classes for a given input feature). We chose to build a multi-label classifier using a Convolutional Neural Network (CNN) deep-learning architecture. There are several ways to build a
multi-label classifier and in this project we have decided to use the binary relevance technique. In this technique, we basically treat each label as a separate single
classification problem. As we have about 15 different classes in this dataset, we would build 15 binary classifiers. The target variable fed to the neural-network architecture
will be a vector of 0s and 1s where a ‘1’ indicates that the person has the particular disease and a ‘0’ indicates otherwise.
