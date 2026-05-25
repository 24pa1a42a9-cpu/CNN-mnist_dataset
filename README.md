MNIST Image Classification with Convolutional Neural Network (CNN)
Overview
This notebook demonstrates how to build, train, and evaluate a Convolutional Neural Network (CNN) for image classification on the MNIST dataset using TensorFlow/Keras.

Setup
The necessary libraries, including TensorFlow, NumPy, and Matplotlib, are imported at the beginning of the notebook.

Data Loading and Preprocessing
The MNIST dataset, consisting of grayscale images of handwritten digits (0-9), is loaded using tf.keras.datasets.mnist.load_data(). The data is then reshaped to include a channel dimension, suitable for CNN input.

Model Architecture
A Sequential CNN model is defined with the following layers:

Conv2D layers: Extract features from the input images.
MaxPooling2D layers: Reduce the spatial dimensions of the feature maps.
Flatten layer: Converts the 2D feature maps into a 1D vector.
Dense layers: Fully connected layers for classification, with a final softmax activation for output probabilities.
Model Compilation and Training
The model is compiled with the Adam optimizer, sparse_categorical_crossentropy loss function (suitable for integer labels), and 'accuracy' as the evaluation metric. It is then trained on the training data for 5 epochs.

Model Evaluation
The trained model's performance is evaluated on the test dataset to assess its generalization ability.

Visualization of Predictions
A selection of random test images are displayed along with their true labels and the model's predicted labels, providing a visual assessment of the model's performance.
