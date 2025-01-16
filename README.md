# Steel Surface Defect Detection Models Comparison

This repository provides a comparative analysis of three deep learning models implemented for detecting and classifying steel surface defects: YOLO-NAS, ResNet50, and a custom Convolutional Neural Network (CNN).

## Model Overview
```
| Model     | Description                                                  | Defect Classes | Total Images | Test Accuracy                                              |
|-----------|--------------------------------------------------------------|----------------|--------------|-----------------------------------------------------------|
| YOLO-NAS  | Fast object detection model using YOLO framework              | 6              | 1,800        | mAP@0.50: 0.85, Precision: 0.80, Recall: 0.85, F1: 0.82    |
| ResNet50  | Fine-tuned ResNet50 architecture for defect classification    | 6              | 1,800        | ~80%                                                       |
| CNN       | Custom CNN architecture designed for defect classification    | 6              | 1,800        | ~85%                                                       |
```

## Model Architectures

### YOLO-NAS
- State-of-the-art YOLO architecture optimized for speed and accuracy
- Real-time detection capabilities
- Comprehensive augmentation pipeline
- Multiple feature extraction stages with skip connections

### ResNet50
- Modified ResNet50 architecture with fine-tuning layers
- Advanced data augmentation implementation
- Residual connections for improved gradient flow
- Pre-trained weights with custom classification head

### Custom CNN
- Simplified convolutional neural network architecture
- Multiple convolutional layers followed by dense layers
- Focused on robust defect classification
- Optimized for steel surface defect detection

## Training Parameters

### YOLO-NAS
- Batch Size: 16
- Learning Rate: Dynamic 0.0001
- Epochs: 10
- Optimizer: Adam
- Data Augmentation:
  - Random flips
  - Rotations
  - Crops
  - Color jittering

### ResNet50
- Batch Size: 16
- Learning Rate: 0.0001 (with adjustment schedule)
- Epochs: 10 
- Optimizer: Adam
- Transfer Learning: Enabled

### Custom CNN
- Batch Size: 16
- Learning Rate: 0.0001
- Epochs: 10 
- Basic data augmentation techniques

## Performance Metrics

### YOLO-NAS
- Mean Average Precision (mAP) at IoU=0.50: **0.85**
- Precision: **0.80**
- Recall: **0.85**
- F1-Score: **0.82**

### ResNet50
- Test Accuracy: **~80%**
- Good generalization on unseen data
- Stable training performance

### Custom CNN
- Test Accuracy: **~85%**
- Efficient training time
- Good balance of accuracy and complexity

## Model Selection Guide

Choose the appropriate model based on your specific requirements:

1. **YOLO-NAS** is ideal for:
   - Real-time detection requirements
   - High-throughput processing
   - Applications requiring balanced precision and recall

2. **ResNet50** is suitable for:
   - Robust feature extraction
   - Transfer learning applications
   - Stable training process

3. **Custom CNN** is recommended for:
   - Simple deployment scenarios
   - Resource-constrained environments
   - Quick prototyping

## Conclusion

Each model offers distinct advantages:

- **YOLO-NAS**: Best overall performance with superior metrics in precision, recall, and F1-score
- **Custom CNN**: Highest accuracy (85%) with simpler architecture
- **ResNet50**: Robust performance with good transfer learning capabilities


