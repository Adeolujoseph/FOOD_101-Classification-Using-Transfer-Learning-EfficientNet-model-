# FOOD_101-Classification-Using-Transfer-Learning-EfficientNet-model-
classifying the food101 dataset using cnn

## Dataset Description
Dataset contains 101,000 images of different foods. 101 food categories representing 101 classes, 750 training images and 250 test images for each class. Image Size varies but max is : 512x512 pixels, Channels: RGB (3 channels). The dataset is directly downloaded using the TorchVision library's datasets.Food101 module

## Dependencies
Python 3.x PyTorch Torch Torchvision Matplotlib NumPy sklearn

## Preprocessing
Resized to 256* 256. Random affine transformations including rotation, translation, and scaling. Random resized crop to a size of 256x256 pixels, with a scaling factor ranging from 0.75 to 1 times the original size.

## Model Architecture
Pre trained Efficient Net(which uses compound scaling to achieve computational efficiency and accuracy ) of efficientnet-b0 of 5.3M Params. out_features of the last fully connected layer modified to 101, the number of classes. 

## Training and Evaluation
Loss Criteria: CrossEntropyLoss function, Optimizer: Adam optimizer, Number of Epochs: 20

Evaluation Metric: Validation Loss, Accuracy, Recall(Macro&Micro), Precision(Macro&Micro)  and F1(Macro&Micro)

## Result
Max val accuracy  of 80.17% was achieved at epoch 12. Lowest val loss of 0.802 obtained @ Epoch 7. Best Micro and Macro Recall, Precision and F1 generally lies around 0.8

Training loss and test loss was also  visualized as epoch number progressed to observe overfitting. 

## Project Limitations and Future Work
Hoping to improve the accuracy by trying other higher variants of the architecture and hyperparameter fine tuning. 

