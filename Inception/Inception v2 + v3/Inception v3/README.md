# I. Introduction

The Inception V2 and V3 architectures are further improvements to the Inception V1 model, designed to improve performance and optimize the model for image processing and image recognition tasks. Both versions were introduced in research papers as part of the development of Deep Neural Networks, with a particular focus on improving computation speed, reducing the number of parameters while maintaining or improving accuracy compared to Inception V1.

# II. Model structure

### 1. Architecture:

| ![image](https://github.com/n1ne1903/Pomodoro-with-camera-detect-distracted/assets/141629048/32c5e64d-b9fc-4673-8dae-ca97404ff03c) | ![image](https://github.com/n1ne1903/Pomodoro-with-camera-detect-distracted/assets/141629048/4e9fe3ee-7a88-4155-9187-08d57ba6bd7f) | ![image](https://github.com/n1ne1903/Pomodoro-with-camera-detect-distracted/assets/141629048/f158813d-6612-4343-a583-240915035202) |
|:------------------------------:|:------------------------------:|:------------------------------:|
| Figure 5              | Figure 6             | Figure 7            |

### 2. Key features of the Inception model:**

- **Goal:** Further improve accuracy and computational efficiency compared to Inception V2, with deeper adjustments in the architecture.
- **Notable techniques:**
  - **Batch Normalization:** Used to improve training speed and help the model converge faster.
  - **Label Smoothing:** A technique to avoid overfitting, improve the accuracy of the model when training by smoothing the labels.

# III. Experimental results:

### 1. Loss and accuracy: 

![Training Results]("C:\D\My Github\CNN\Inception\Inception v2 + v3\Image\result_v3.png")

### 2. Comment: 

- **Valid Accuracy** Reached 0.9 after 6 epochs.
- **Epoch 25:** The model achieved an accuracy of 0.8 val accuracy, although it had previously achieved 0.94 at epoch 24.
- **Analysis:** I also don't know why there is this instability. Personal opinion: The explanation for this may be partly due to Label Smoothing making the model less certain about the prediction results.


# IV. Reference code:

- **Jupyter Notebook:** [Inception v1.ipynb]("C:\D\My Github\CNN\Inception\Inception v2 + v3\Inception v3\Inception v3.ipynb")
- **Notion:**
  - Since Inception V2 uses 1 more Auxiliary Classifiers, there will be 1 more auxiliary outputs: 'output_2_accuracy'
  - The loss function will affect all 2 outputs (Main Output + Auxiliary Classifiers) by setting the weights in the optimizier