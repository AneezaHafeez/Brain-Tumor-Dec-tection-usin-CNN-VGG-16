# Brain-Tumor-Dec-tection-usin-CNN-VGG-16
This project implements a binary classification model for detecting brain tumors from MRI images. The model uses transfer learning with the VGG16 architecture to classify images as "tumor" or "no tumor."

Dataset
The dataset contains MRI images of brain scans organized into two categories:

No Tumor: Images without brain tumors.
Yes Tumor: Images with visible brain tumors.
Each image is preprocessed to fit the VGG16 model's input size of 224x224 pixels.

Key Steps
Dataset Setup: Images are loaded from Google Drive, resized to 224x224 pixels, and labeled accordingly.

Data Preparation: The dataset is split into training and testing sets (80/20 ratio), normalized, and one-hot encoded.

Model Architecture: The VGG16 model (pre-trained on ImageNet) is used as a feature extractor, with a custom classifier added on top, consisting of dense, dropout, and softmax layers for binary classification.

Training: The model is compiled with the Adam optimizer and categorical crossentropy loss. Early stopping is applied to prevent overfitting, and training is visualized through accuracy and loss plots.

Evaluation and Saving: The trained model is evaluated on test data, and the final model is saved as brain_tumor_vgg16_with_split.h5.
