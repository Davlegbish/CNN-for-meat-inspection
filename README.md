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

   <img width="996" height="380" alt="Classification_Classes " src="https://github.com/user-attachments/assets/f44955bf-16d1-4b3d-8d95-a2961e296b71" />


 # 📈 Performance & Evaluation
Metric: Categorical Cross-Entropy loss minimized via the Adam Optimizer.

Analysis: <img width="1920" height="806" alt="Confusion_Matrix_Results" src="https://github.com/user-attachments/assets/17ec8e09-05e8-403c-a648-d7f8802bb962" />


Observation: The confusion matrix shows a high sensitivity for the 'Rotten' class, which is critical for food safety to avoid "False Negatives."




# C.Model Evaluation
1.Accuracy and Loss Metrics: Evaluate the model on the testing dataset using metrics such as accuracy and loss.

<img width="1878" height="600" alt="Classfication_report " src="https://github.com/user-attachments/assets/db0dbee3-03c8-42c2-a6c8-af99c7c29483" />





 I am exploring Root Cause Analysis to determine the specific visual 'causes' (e.g., surface oxidation vs. bacterial colonies) that lead the model to a Rotten classification.



# 🔮 Future Research Directions

XAI Integration: Implementing Grad-CAM to visualize neural attention on surface bacteria vs. color changes.

I am interested in exploring how Kolmogorov-Arnold Networks (KAN) could replace traditional Dense layers in this architecture to improve interpretability and parameter efficiency in industrial food-safety models.






