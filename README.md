# Hand Gesture Recognition Project

This project focuses on recognizing American Sign Language (ASL) gestures using a combination of Convolutional Neural Networks (CNN) and Fuzzy Logic for enhanced prediction accuracy. The system is designed to predict 25 ASL letters (A-Y) from hand gesture images, ensuring robustness and reliability even in challenging or uncertain scenarios.

# Dataset

Link to the Dataset:- https://www.kaggle.com/datamunge/sign-language-mnist

The dataset used in this project consists of grayscale images representing different ASL letters. These images were preprocessed to standardize their size to 28x28 pixels, enabling efficient computation and uniformity across the inputs. The preprocessing steps also included normalizing pixel values to a range of 0 to 1, reshaping the images to a 28x28x1 format suitable for CNN input, and applying data augmentation techniques such as rotation, shifting, and zooming to improve the model's generalization capability.


# Preprocessing
The CNN architecture employed consists of three convolutional layers, each extracting meaningful features from the input images, followed by pooling layers to reduce spatial dimensions and focus on significant patterns. Dropout layers were added to prevent overfitting, ensuring that the model generalizes well to new data. The dense layers towards the end of the network perform high-level decision-making, with the final layer predicting the class of the input image. The model was trained using the Adam optimizer for efficient weight updates and categorical cross-entropy as the loss function to handle the multi-class classification problem. Over 20 training epochs, the model demonstrated excellent accuracy in learning to classify ASL gestures.

# Interfernce
For inference, the CNN generated probability scores for each class. To refine these predictions, Fuzzy Logic was applied, introducing a decision-making layer that adjusts probabilities based on defined rules. This process improved the confidence and reliability of predictions, especially in cases where the CNN probabilities were ambiguous or borderline. By mapping the CNN outputs to refined confidence scores, the system ensured better handling of uncertain scenarios, enhancing overall performance.

# Training and Testing
This project demonstrates a robust approach to ASL recognition by combining the strengths of CNNs for feature extraction and Fuzzy Logic for refined decision-making, making it a practical solution for real-world gesture recognition applications.
