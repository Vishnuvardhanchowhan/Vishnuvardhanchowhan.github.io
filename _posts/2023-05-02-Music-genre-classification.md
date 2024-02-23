---
layout: post
title: Music Genre classifier
subtitle: Music genre claassification using Machine learning models
cover-img: /assets/img/mgenre/mgenre_wall.jpg
thumbnail-img: /assets/img/mgenre/mgenre_complete.jpg
share-img: /assets/img/path.jpg
tags: [ML, AI]
---

Developed a music genre classifier that classifies or categorizes audio datasets into one of eight different categories like jazz, pop, rock, etc by training four traditional machine learning classifiers such as SVM (support vector machine), logistic regression, random forest classifier, etc and choosing the best among them by comparing their metrics as well as following another approach by training deep learning model VGG16 which has an architecture based on CNN.
The VGG16 model is trained on audio spectrogram images extracted from the Audio dataset using the YouTube command.
Finally combined best-performing models from both of these approaches, with their combined strengths, they gave us the best performance with a ROC value of 0.864, higher than any individual ML models.

> Why did I choose VGG16 instead of others? What is a VGG16 model? 

VGG16 is a type of CNN (Convolutional Neural Network) that is considered to be one of the best computer vision models to date. The creators of this model evaluated the networks and increased the depth using an architecture with very small (3 × 3) convolution filters, which showed a significant improvement on the prior-art configurations. They pushed the depth to 16–19 weight layers making it approximately — 138 trainable parameters. 
VGG16 is object detection and classification algorithm which is able to classify 1000 images of 1000 different categories with 92.7% accuracy. It is one of the popular algorithms for image classification and is easy to use with transfer learning.
The model consists of 5 convolutional blocks (conv base), followed by a set of densely connected layers, which outputs the probability that a given image belongs to each of the possible classes.

 
> What is an audio spectrogram?
A spectrogram is a 2D representation of a signal having time on the x-axis and frequency on the y-axis. A colormap is used to quantify the magnitude of a given frequency within a given time window.

What pre-processing steps did you follow before starting training on the deep learning model?
* Loading and Resizing: Load the spectrogram images and resize them to a consistent size. This ensures uniformity for model input.
* Normalization: Normalize pixel values to a specific range (e.g., [0, 1] or [-1, 1]) to facilitate model training.
* Augmentation: Apply data augmentation techniques such as rotation, zooming, or flipping to artificially increase the diversity of your training dataset. This helps the model generalize better.
* Filtering and Denoising: Apply filters or denoising techniques to reduce noise in the spectrogram images, especially if the recording environment introduces unwanted artifacts.
* Handling Imbalanced Classes: If your dataset has imbalanced classes, consider strategies like oversampling, under-sampling, or using class weights during training.

> What is ROC value?
This evaluation criterion known as the area under the receiver operator characteristics (ROC) curve is a common way to judge the performance of a multi-class classification system. The ROC is a graph between the true positive rate and the false positive rate. A baseline model that randomly predicts each class label with equal probability would have an AUC of 0.5, and hence the system being designed is expected to have an AUC higher than 0.5.

> Different metrics used in machine learning and confusion metrics.

A mammogram is a test that identifies whether someone has breast cancer. A false positive result would incorrectly diagnose that a patient has breast cancer, while a false negative one would fail to detect a patient who does have it. True positive is when there is breast cancer and it correctly detects it whereas true negative is when there is no breast cancer and it correctly identifies it.  
Accuracy:
* Pros: Accuracy is a helpful metric when you deal with balanced classes and care about the overall model “correctness” and not the ability to predict a specific class. Accuracy is easy to explain and communicate. 
* Cons: If you have imbalanced classes, accuracy is less useful since it gives equal weight to the model’s ability to predict all categories. Communicating accuracy in such cases can be misleading and disguise low performance on the target class.

                                                            
1. Precision:
Precision is a metric that measures how often a machine learning model correctly predicts the positive class. You can calculate precision by dividing the number of correct positive predictions (true positives) by the total number of instances the model predicted as positive (both true and false positives).
The accuracy is a whopping 95% (the model is right in 57 cases out of 60), but the precision is 0. To calculate the precision, we must divide the number of correctly predicted spam emails by their total number. However, the number of correctly identified spam emails is 0. There were 3 spam emails in the dataset, and the model missed them all. All the correct predictions were about non-spam emails.
In other words, precision answers the question: how often the positive predictions are correct?
Say, as a product manager of the spam detection feature, you decide that cost of a false positive error is high. You can interpret the error cost as a negative user experience due to misprediction. You want to ensure that the user never misses an important email because it is incorrectly labeled as spam. As a result, you want to minimize false positive errors. 
In this case, precision is a good metric to evaluate and optimize for. A higher precision score indicates that the model makes fewer false positive predictions. It is more likely to be correct whenever it predicts a positive outcome.
                                                                     
2. Recall:
Recall is a metric that measures how often a machine learning model correctly identifies positive instances (true positives) from all the actual positive samples in the dataset. You can calculate recall by dividing the number of true positives by the number of positive instances. The latter includes true positives (successfully identified cases) and false negative results (missed cases).
In other words, recall answers the question: can an ML model find all instances of the positive class?
It works well for problems with imbalanced classes since it is focused on the model’s ability to find objects of the target class.
Recall is useful when the cost of false negatives is high. 
In this case, you typically want to find all objects of the target class, even if this results in some false positives (predicting a positive when it is actually negative).
For example, if an ML model points to possible medical conditions, detects dangerous objects in security screening, or alarms to potentially expensive fraud, missing out might be very expensive. In this scenario, you might prefer to be overly cautious and manually review more instances the model flags as suspicious. 
In other words, you would treat false negative errors as more costly than false positives. If that is the case, you can optimize for recall and consider it the primary metric.
                                                                  
3. F1 Score:
Use Case: Balance between Precision and Recall
F1 score is a good choice when you want a balance between precision and recall. It's especially useful when there's an uneven class distribution.

> For further details head on to my [github][1] repository.

[1]:https://github.com/Vishnuvardhanchowhan/Music-Genre-Classification-IML-Project
