# Melanoma-Cancer-Detection

# Abstract
Melanoma, the deadliest form of skin cancer, is one of over 200 types of cancer. The diagnostic process for melanoma typically begins with clinical screening, followed by dermoscopic analysis and histopathological examination. When detected early, melanoma is highly treatable. The initial step in diagnosis involves a visual examination of the affected skin area, during which dermatologists capture dermoscopic images using high-resolution cameras. These images alone provide a diagnostic accuracy of 65-80% for melanoma without further technical assistance. With additional visual evaluation by cancer specialists, the accuracy improves to 75-84%. This project aims to develop an automated classification system utilizing image processing techniques to classify skin cancer based on dermoscopic images of skin lesions.

# Problem Statement
In the skin biopsy, the dermatologist takes some part of the skin lesion and examines it under the microscope. The current process takes almost a week or more, starting from getting a dermatologist appointment to getting a biopsy report. The aims to shorten the current gap to just a couple of days by providing the predictive model. The approach uses Convolutional Neural Network (CNN) to classify nine types of skin cancer from outlier lesions images. This reduction of a gap has the opportunity to impact millions of people positively.

# Motivation

The primary goal of this project is to contribute to reducing mortality caused by skin cancer through early and accurate diagnosis. The motivation behind this effort is to leverage advanced image classification technologies to improve public health outcomes. Significant progress in computer vision, driven by machine learning and deep learning, has demonstrated scalability across various domains, offering a promising avenue for enhancing skin cancer detection and ultimately improving patient well-being.

# Dataset

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images.

The data set contains the following diseases:

<img width="187" alt="image" src="https://github.com/user-attachments/assets/d6586fe4-66bb-4fe6-a407-22451d590b74">


<img width="641" alt="image" src="https://github.com/user-attachments/assets/caa70248-4806-4893-abf9-b94ed9b9db5f">



To overcome the issue of class imbalance, used a python package Augmentor (https://augmentor.readthedocs.io/en/master/) to add more samples across all classes so that none of the classes have very few samples.

<img width="330" alt="image" src="https://github.com/user-attachments/assets/55add763-5f21-43c5-8e00-85f9e07ac682">


# Cancer Classification Using CNN
This project aims to classify skin cancer using images of skin lesions. To achieve high accuracy and performance in this classification task, I have developed a custom Convolutional Neural Network (CNN) model.

**Model Architecture:**
* Rescaling Layer: Rescales the input image from the [0, 255] range to the [0, 1] range for efficient processing.

* Convolutional Layer: Applies a convolution operation to the input, effectively reducing the image size by summarizing the pixel values in its receptive field into a single value. This helps in extracting essential features while reducing the dimensions of the data.

* Pooling Layer: Reduces the dimensions of feature maps generated by convolutional layers. Pooling helps lower the number of parameters and computational complexity by summarizing the features in a specific region of the feature map.

* Dropout Layer: Randomly sets a fraction of input units to 0 during training to prevent overfitting, ensuring the model generalizes well on unseen data.

* Flatten Layer: Converts the multidimensional output of convolutional layers into a 1D feature vector, preparing it for the fully connected layers.

* Dense Layer: A fully connected layer where each neuron receives input from all neurons in the previous layer. This is typically used for classification and decision-making.

**Activation Functions:**
* ReLU (Rectified Linear Unit): A piecewise linear function that outputs the input directly if it is positive, and zero otherwise. ReLU is used in hidden layers to overcome the vanishing gradient problem, enabling faster learning and better model performance.

* Softmax: Applied in the output layer, the softmax function generates a probability distribution for multi-class classification, with output values ranging between 0 and 1. The sum of all output probabilities equals 1, making it ideal for classification tasks with multiple categories.

# Model Architecture

<img width="367" alt="image" src="https://github.com/user-attachments/assets/c81267c0-79e2-42db-99a2-3fae02460f4c">


Model Evaluation

<img width="667" alt="image" src="https://github.com/user-attachments/assets/ae99575e-79b4-40ad-b0be-6c8ebb92a978">


