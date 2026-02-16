# 🥩 Automated Quality Control in Meat Processing
Custom Convolutional Neural Networks (CNN) for Real-time Food Safety Classification

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.15-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

# 🎯 Industrial Objective
To automate the classification of meat freshness using Deep Learning, providing a scalable alternative to manual inspection in food processing environments. This project directly addresses the need for Industrial AI in agricultural logistics.

# 📊 Dataset Insights
A 5.8GB high-resolution dataset was utilized to ensure the model captures subtle textural changes in meat fibers.

| Set      | Images | Class Balance |                |
|----------|--------|---------------|----------------|
| Training | 2288   | 50/50         | (Fresh/Rotten) |
| Testing  | 980    | 50/50         | (Fresh/Rotten) |



# 🏗 Model Architecture & Preprocessing

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
6. Classification: Use a softmax activation function in the final layer to produce probability scores for each class (fresh or rotten).

   ![Screenshot (59)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/e650aa3b-737f-454a-9547-78f2e070cbaa)




 # 📈 Performance & Evaluation
Metric: Categorical Cross-Entropy loss minimized via the Adam Optimizer.

Analysis: <img width="1920" height="806" alt="Confusion_Matrix_Results" src="https://github.com/user-attachments/assets/17ec8e09-05e8-403c-a648-d7f8802bb962" />


Observation: The confusion matrix shows a high sensitivity for the 'Rotten' class, which is critical for food safety to avoid "False Negatives."

  ![meat(60)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/51006981-116a-4ea1-bae9-e4f8cd0c781b)


# C.Model Evaluation
1.Accuracy and Loss Metrics: Evaluate the model on the testing dataset using metrics such as accuracy and loss.

![meat (56)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/fb1ae62f-2e58-461e-b8f7-8e760f97a380)


![meat (52)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/919ddcb0-3753-4858-a485-0a7b45c40407)


"Beyond simple accuracy, I am exploring Root Cause Analysis to determine the specific visual 'causes' (e.g., surface oxidation vs. bacterial colonies) that lead the model to a 'Rotten' classification.


# D.Save the Model: 
Save the trained model for future use,develop a pipeline for real-time inference where new images can be classified as fresh or rotten.

![Screenshot (59)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/e650aa3b-737f-454a-9547-78f2e070cbaa)


![save (57)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/b828e758-d3a0-4522-b26c-f146ec1d07d6)


![Screenshot (58)](https://github.com/Davlegbish/CNN-for-meat-inspection/assets/155652335/066b57e0-830b-4931-bc2f-b5d9c074a585)


# 🔮 Future Research Directions

XAI Integration: Implementing Grad-CAM to visualize neural attention on surface bacteria vs. color changes.
"I am interested in exploring how Kolmogorov-Arnold Networks (KAN) could replace traditional Dense layers in this architecture to improve interpretability and parameter efficiency in industrial food-safety models."






