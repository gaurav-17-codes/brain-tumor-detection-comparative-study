# Brain Tumor Detection using Transfer Learning (Stage-1)

## Project Overview
This project focuses on Brain Tumor Classification from MRI images using Transfer Learning with Pretrained CNN models.
Stage-1 of this project aims to:
Benchmark multiple pretrained deep learning models
Compare their performance
Identify the best-performing architecture
Establish a strong baseline for Stage-2 hybrid model development

## Objective
To classify MRI brain images into the following tumor categories:
Glioma
Meningioma
Pituitary
No Tumor
The goal of Stage-1 is to achieve maximum classification accuracy using transfer learning before moving to custom hybrid architecture development in Stage-2.

## Dataset
Dataset Used: Brain Tumor MRI Dataset (Kaggle)
Training images organized class-wise
Separate testing directory
4 tumor categories
RGB MRI images

## Model Architecture (Stage-1)
We used Transfer Learning with:
Pretrained ResNet50 (ImageNet weights)
Custom fully connected classification head
Softmax output layer
Architecture Flow:
Input Image (224×224×3)
→ ResNet50 (feature extractor)
→ Global Average Pooling
→ Dense Layer
→ Dropout
→ Softmax Output (4 Classes)

## Training Configuration
Image Size: 224 × 224
Optimizer: Adam
Loss Function: Categorical Crossentropy
Batch Size: 32
Epochs: 20+
Callbacks:
EarlyStopping
ReduceLROnPlateau
ModelCheckpoint

## Results
Best Performing Model: DenseNet  
Reason: Higher feature reuse and deeper architecture  
Observation: Transfer learning models outperformed custom CNN.
### Final Performance (Stage-1)
Training Accuracy: ~96%+
Validation Accuracy: ~96%+
Test Accuracy: ~96% (Best Achieved)
Additional Evaluation:
Confusion Matrix
Precision, Recall, F1-score
ROC-AUC Curves
The model demonstrated strong generalization across all tumor classes.
### Performance Visualization
The following graphs were generated:
Training vs Validation Accuracy
Training vs Validation Loss
Accuracy Comparison Bar Chart
Confusion Matrix
ROC Curve
### Key Learnings from Stage-1
Transfer learning significantly improves medical image classification.
Fine-tuning pretrained models boosts validation accuracy.
Proper augmentation reduces overfitting.
ResNet50 performs strongly on MRI-based classification tasks.

### Next Stage (Stage-2)
Stage-2 focuses on:
Designing a Custom Hybrid Model
Combining CNN + Pretrained Backbone
Improving robustness
Enhancing model interpretability
Performance optimization
### Technologies Used
Python
TensorFlow / Keras
NumPy
Matplotlib
Seaborn
Scikit-learn
### Author
Final Year Major Project
Department of Electronics & Comm. Engineering

### How to Run
git clone <repository_link>
cd brain-tumor-stage1
pip install -r requirements.txt
python train.py

### Conclusion
Stage-1 successfully establishes a high-accuracy baseline model using transfer learning.
This foundation enables further experimentation with hybrid architectures in Stage-2.
