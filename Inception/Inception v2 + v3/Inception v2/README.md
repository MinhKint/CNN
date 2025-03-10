# I. Introduction

The Inception V2 and V3 architectures are further improvements to the Inception V1 model, designed to improve performance and optimize the model for image processing and image recognition tasks. Both versions were introduced in research papers as part of the development of Deep Neural Networks, with a particular focus on improving computation speed, reducing the number of parameters while maintaining or improving accuracy compared to Inception V1.

# II. Model structure

### 1. Architecture:

| ![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Figure%205.png) | ![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Figure%206.png) | ![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Figure%207.png) |
|:------------------------------:|:------------------------------:|:------------------------------:|
| Inception_F5 module  | Inception_F6 module  | Inception_F7 module  |

| ![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Figure%208.png) | ![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Figure%2010.png)| ![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Figure%209.png) |
|:------------------------------:|:------------------------------:|:------------------------------:|
| After Inception_F6 modul  | Each time the module changes size  | Two basic other ways  |

![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Architecture%20%2B%20Layer%20Inception%20v2.png) ![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v2%20%2B%20v3/Image/Architecture%20%2B%20Layer%20Inception%20v3.png)

**Note:** Inception V3 is the version that uses additional Label Smoothing and Batch Normalization

### 2. Key features of the Inception model:**

- **Goal:** Optimize the computational performance of the model by reducing the number of parameters and increasing the training speed without reducing the accuracy.
- **Notable techniques:**
  - **Factorized Convolutions:** Split large convolutions into smaller convolutions (e.g. split a 5x5 convolution into two 3x3 convolutions). This reduces the computational cost and the number of parameters while maintaining the model's strong representation.
  - **Asymmetric Convolutions:** Use asymmetric convolutions, for example, replacing a 3x3 convolution with 1x3 and 3x1 convolutions. This simplifies the computation while maintaining the performance of the model.
  - **Spatial Separable Convolutions:** Spatial convolution decomposition technique, instead of performing convolution on the entire space, split it into two convolutions in the vertical and horizontal directions. This further reduces the computational cost and makes the model more efficient. - RMSProp Optimizer: A type of optimization algorithm used to train the model, which improves efficiency compared to previous methods.

# III. Experimental results:

### 1. Loss and accuracy: 

![Training Results]("C:\D\My Github\CNN\Inception\Inception v2 + v3\Image\result_v2.png")

### 2. Comment: 

- **Valid Accuracy** Reached 0.9 after 15 epochs.
- **Epoch 25:** The model reached an accuracy of 0.92 val accuracy, demonstrating the effectiveness of the improvements.
- **Analysis:** Because the model architecture is more complex and the dataset is too small, there will be Overfitting here: The difference between train_accuracy and valid_accuracy is 0.05.

# IV. Reference code:

- **Jupyter Notebook:** [Inception v2.ipynb]("C:\D\My Github\CNN\Inception\Inception v2 + v3\Inception v2\Inception v2.ipynb")
- **Notion:**
  - Since Inception V2 uses 1 more Auxiliary Classifiers, there will be 1 more auxiliary outputs: 'output_2_accuracy'
  - The loss function will affect all 2 outputs (Main Output + Auxiliary Classifiers) by setting the weights in the optimizier
