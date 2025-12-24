# Plant-Disease-Classification
This project implements a deep learning-based plant disease classification system specifically focused on potato diseases using transfer learning with a pre-trained ResNet18 model. The system can classify potato leaves into three categories: Healthy, Early Blight, and Late Blight.
# Task 13: Plant Disease Classification

**Student:** Ahmedli Huseyn 
**ID:** S313  
**Seed:** 20240313

## Presentation
[View Presentation Slides](https://docs.google.com/presentation/d/1elWuudX6OEqHuZrqr_lCaLiBf7vKgkm8/edit?usp=drive_link&ouid=115706297722399056724&rtpof=true&sd=true)

## Dataset
- **Name:** PlantVillage
- **Classes:** (1 plant with 3 conditions)
- **Training samples:** 2152
- **Test samples:** 100

## Model Architecture
- **Type:** ResNet18
- **Convolutional layers:** 17
- **Fully connected layers:** 1
- **Total parameters:**  11,178,563

## Training Comparison

### Version 1
- **Learning rate:** 0.0001
- **Batch size:** 32
- **Optimizer:** Adam
- **Test accuracy:** 95.29%

### Version 2
- **Learning rate:** 0.00001
- **Batch size:** 64
- **Optimizer:** SGD with momentum=0.9, lr=0.001
- **Test accuracy:** 98.78%

### Best Result
- **Best version:** Version 2
- **Final test accuracy:** 98%
- **Target accuracy:** ≥88%
- **Status:** ✓ Achieved 

## Analysis
- **Best performing class:** Potato___Early_blight
- **Worst performing class:** Potato___healthy
- **Key observations:** The experiment demonstrated that **Adam optimizer with moderate learning rate (0.0001) achieved the best validation accuracy**, while SGD struggled to converge effectively within 10 epochs. Transfer learning with frozen ResNet18 backbone proved highly effective, requiring minimal training time while achieving strong performance on the specialized potato disease classification task. The class imbalance between healthy and diseased samples highlighted the importance of proper data distribution for robust model generalization.

## Files
- `notebook.ipynb`: [Colab code](https://github.com/user-attachments/files/24332333/Colab.e_hos_geldiniz_.ipynb)
