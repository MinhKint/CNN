# I. Introduction

Inception is a famous convolutional neural network (CNN) architecture developed by Google in 2014 in the paper "Going Deeper with Convolutions" and used in the Inception-v1 model, also known as GoogLeNet. 

# II. Model structure

### 1. Architecture:

<img><\img>
![image](https://github.com/MinhKint/CNN/blob/main/Inception/Inception%20v1/Image/Architecture.png)

### 2. Key features of the Inception model:**

- **Inception Modules:**
  - The Inception module is a basic block of the Inception network, allowing transformations with different filter sizes (1x1, 3x3, 5x5) to be performed in parallel.
  - Multi-scale processing: The use of different filter sizes (multi-scale) helps the network capture both small detailed features (with small filters like 1x1) and larger, more comprehensive features (with larger filters like 5x5).
  - The results are then concatenated into a single tensor. This allows the neural network to capture features at different levels of detail simultaneously.
  - Each Inception module also includes pooling layers (max pooling) to reduce size and increase computational efficiency.

- **Reduction in Computational Cost:**
  - The use of 1x1 filters helps reduce the number of parameters and computations compared to larger filters.
  - 1x1 transformations not only reduce the number of parameters but also enhance the non-linearity of the network (Increase non-linearity because each 1x1 transformation is followed by a non-linear activation function (such as ReLU)). 

- **Grid Size Reduction:**
  - Inception often reduces the output size after a certain number of layers by using pooling or convolution layers with stride > 1.
  - This size reduction helps keep the network from becoming too large and difficult to train.

- **Auxiliary Classifiers:** The Inception model uses auxiliary classifiers during training. These classifiers are attached in the middle of the network layers and help provide additional training signals. This helps improve gradient flow and allows the network to learn faster and more efficiently.
- **Deep architecture:** The Inception model is very deep and complex, with many layers and consecutive Inception modules. This allows it to learn complex features from input data.
- **Batch Normalization:** Batch normalization is applied to stabilize and accelerate the training process. This helps the model learn more efficiently and reduces the risk of overfitting.

# III. Experimental results:

### 1. Loss and accuracy: 

![Training Results]("C:\D\Github\CNN\Inception\Inception v1\Image\result.png")

### 2. Nhận xét: 

- **Valid Accuracy** Reached 0.9 after 10 epochs.
- **Epoch 25:** The model reached an accuracy of 0.94, demonstrating the effectiveness of the improvements.

# IV. Reference code:

- **Jupyter Notebook:** [Inception v1.ipynb]("C:\D\Github\CNN\Inception\Inception v1\Inception v1.ipynb")
