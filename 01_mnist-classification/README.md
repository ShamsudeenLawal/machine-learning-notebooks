# MNIST Classification: Fully Connected Network vs Convolutional Neural Network

This project implements and compares two neural network architectures for handwritten digit classification using the MNIST dataset:

- Fully Connected Network (FCN)
- Convolutional Neural Network (CNN)

The objective is to analyze the trade-offs between model accuracy, training time, inference time, and model complexity.

---

## Project Overview

Handwritten digit recognition is a classic computer vision task. In this project, two different neural network architectures were implemented and evaluated on the same dataset to understand their performance differences.

The models were trained and tested on the MNIST dataset and compared based on:

- Accuracy
- Training time
- Inference time
- Number of parameters

---

## Dataset

The MNIST dataset consists of grayscale images of handwritten digits.

Dataset characteristics:

- Training samples: 60,000
- Test samples: 10,000
- Image size: 28 × 28 pixels
- Number of classes: 10 (digits 0–9)

Each image is flattened for the Fully Connected Network, while the Convolutional Neural Network processes the images in their original 2D format.

---

## Model Architectures

### Fully Connected Network (FCN)

The Fully Connected Network uses dense layers where each neuron is connected to all neurons in the next layer.

**Model Characteristics**

- Input: 784-dimensional flattened image vector
- Dense layers for feature extraction
- Softmax output layer for classification

**Performance**

- Test Accuracy: **97.88%**
- Parameters: **~243,000**
- Average Training Time per Epoch: **4 seconds**
- Inference Time (10,000 images): **~1 second**

---

### Convolutional Neural Network (CNN)

The CNN architecture uses convolutional layers to automatically extract spatial features from images before classification.

**Model Characteristics**

- Convolution layers for feature extraction
- Pooling layers for dimensionality reduction
- Fully connected layers for classification

**Performance**

- Test Accuracy: **99.08%**
- Parameters: **~107,000**
- Average Training Time per Epoch: **42 seconds**
- Inference Time (10,000 images): **~3 seconds**

---

## Results Comparison

| Metric                      | FCN     | CNN        |
| --------------------------- | ------- | ---------- |
| Test Accuracy               | 97.88%  | **99.08%** |
| Parameters                  | ~243K   | **~107K**  |
| Training Time / Epoch       | **~4s** | ~42s       |
| Inference Time (10k images) | **~1s** | ~3s        |

---

## Key Observations

- **Accuracy**  
  The CNN achieves higher accuracy due to its ability to capture spatial patterns in images.

- **Training Speed**  
  The FCN trains significantly faster per epoch compared to the CNN.

- **Inference Speed**  
  The FCN performs slightly faster inference on the test dataset.

- **Model Size**  
  The CNN has fewer parameters despite achieving higher accuracy.

---

---

## Conclusion

Both models perform well on the MNIST classification task, but they exhibit different strengths:

- The **CNN model** achieves higher accuracy and uses fewer parameters.
- The **FCN model** trains faster and performs slightly faster inference.

The choice of model for production depends on the specific system requirements:

- **Accuracy-critical applications:** CNN
- **Frequent retraining scenarios:** FCN
- **Low-latency inference environments:** FCN

---

## Possible Improvements

Future work may include:

- Hyperparameter tuning
- Data augmentation
- Deeper CNN architectures
- Model compression or quantization
- Deployment as an inference API

---

## License

This project is intended for educational and research purposes.
