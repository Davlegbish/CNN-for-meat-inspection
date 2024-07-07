# Improving Meat Inspection with Convolutional Neural Networks (CNNs)

# Objective:
To develop a Convolutional Neural Network (CNN) model capable of determining whether meat is fresh or rotten using image classification techniques.

# Dataset:

1.Total Size: 5.8GB.
2.Training Dataset: 2,288 images (balanced across two classes: fresh and rotten).
3.Testing Dataset: 980 images (balanced across two classes: fresh and rotten).

Processes Involved:

# A. Data Preprocessing:

1. Image Resizing: Standardize all images to a consistent size (e.g., 64x64 pixels) for uniformity and to fit the input size required by the CNN.
Normalization: Scale pixel values to a range of 0 to 1 for better convergence during training.
Data Augmentation: Apply transformations like rotations, zooming, horizontal flips, and shifts to increase the diversity of the training data and improve the model's robustness.
Feature Extraction with Convolutional Layers:

2.Convolutional Layers: Apply multiple convolutional layers to extract features from the images. Each layer will detect different patterns such as edges, textures, and more complex features as the depth increases.
Activation Function: Use Rectified Linear Units (ReLU) to introduce non-linearity into the model.
Dimensionality Reduction with Max Pooling:

3. Max Pooling Layers: Apply max pooling to reduce the spatial dimensions of the feature maps, keeping the most important information and reducing computational load.

4. Flattening Layer: Convert matrix of the images  into a 1D vector to prepare for the fully connected (dense) layers.
Classification with Fully Connected Layers:

5. Dense Layers: Use one or more dense layers to perform the final classification. Each neuron in these layers will have a connection to every neuron in the previous layer, allowing the model to combine features extracted by the convolutional layers.
6. Output Layer: Use a softmax activation function in the final layer to produce probability scores for each class (fresh or rotten).


Loss Function: Use categorical cross-entropy as the loss function, which is suitable for multi-class classification problems.
Optimizer: Use an optimizer like Adam for efficient training and faster convergence.

 # B.Model Training:

  ![meat(60)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/51006981-116a-4ea1-bae9-e4f8cd0c781b)


# C.Model Evaluation
Accuracy and Loss Metrics: Evaluate the model on the testing dataset using metrics such as accuracy and loss.

![meat (56)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/fb1ae62f-2e58-461e-b8f7-8e760f97a380)


![meat (52)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/919ddcb0-3753-4858-a485-0a7b45c40407)



Confusion Matrix: Generate a confusion matrix to analyze the model's performance in more detail.

![meat (53)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/f259d458-08d6-44f2-939d-78433d5a053c)



# D.Save the Model: 
Save the trained model for future use,develop a pipeline for real-time inference where new images can be classified as fresh or rotten.

![Screenshot (59)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/e650aa3b-737f-454a-9547-78f2e070cbaa)


![save (57)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/b828e758-d3a0-4522-b26c-f146ec1d07d6)


![Screenshot (58)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/066b57e0-830b-4931-bc2f-b5d9c074a585)



This outline provides a comprehensive approach to developing and improving a CNN model for meat inspection. Each step is critical for ensuring the accuracy and efficiency of the classification process.






