OBJECTIVE:
To perform binary image classification using a Convolutional Neural Network (CNN) with transfer learning.

Importing Libraries:
TensorFlow and Keras are imported for deep learning.
OpenCV (cv2) is imported for image processing.
The VGG16 model is imported from Keras applications.

Loading Pretrained VGG16 Model:
The VGG16 model with pretrained weights on ImageNet is loaded and configured to exclude the top (fully 
connected) layers. The input shape is set to (150, 150, 3).

Creating a Sequential Model:
A new Sequential model is created.
The pretrained VGG16 model is added as the first layer.
A Flatten layer is added to flatten the output.
Two Dense layers are added for classification, with ReLU activation in the first and sigmoid activation in the second.

Freezing Convolutional Layers:
The convolutional base (VGG16) layers are set to be non-trainable to keep their pretrained weights.

Data Augmentation and Generators:
ImageDataGenerator is used for data augmentation (e.g., rescaling, shearing, zooming, horizontal flipping).
Separate generators are created for the training and validation datasets.

Compiling the Model:
The model is compiled with the Adam optimizer and binary crossentropy loss for binary classification. Accuracy is chosen as the evaluation metric.

Training the Model:
The model is trained using the fit_generator function with the specified number of epochs.

Plotting Training History:
Matplotlib is used to plot the training and validation accuracy and loss over epochs.

Testing on New Images:
Images of a dog and a cat are loaded for testing.
The images are preprocessed (resized and reshaped) to match the model's input requirements.
The model's predict function is used to obtain predictions for the test images.

Observations:
Training and validation accuracy/loss plots are displayed.
The accuracy results on new test images are discussed, indicating that the model performed well with a training accuracy of 93% and a validation accuracy of 92%.
