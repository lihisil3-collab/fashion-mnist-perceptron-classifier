# fashion-mnist-perceptron-classifier

### Multi-class Perceptron with Pocket Algorithm | Computer Vision Project

## Overview
Image classification system built from scratch on the Fashion-MNIST dataset 
a standard computer vision benchmark used in ML research.
Classifies 28×28 grayscale clothing images into 10 categories using a 
multi-class Perceptron with the Pocket Algorithm.

**Final Test Accuracy: 83.1% on 10,000 unseen images**

## The Problem
Given a grayscale image of a clothing item, predict which of 10 categories 
it belongs to: T-shirt, Trouser, Pullover, Dress, Coat, Sandal, 
Shirt, Sneaker, Bag, or Ankle boot.

## What I Built
- Pocket Algorithm implemented from scratch using vectorized NumPy
- One-vs-All strategy extending binary Perceptron to 10-class classification
- Full preprocessing pipeline: normalization, flattening, bias term injection
- Model evaluation: confusion matrix, per-class sensitivity (TPR), 
  learning curves for all 10 classifiers
- Systematic hyperparameter experiments across 4 configurations

## Results
| Class       | TPR (Sensitivity) |
|-------------|-------------------|
| Trouser     | 95.0%             |
| Bag         | 94.9%             |
| Sneaker     | 93.8%             |
| Ankle boot  | 92.8%             |
| Sandal      | 90.2%             |
| T-shirt/top | 85.6%             |
| Dress       | 83.7%             |
| Coat        | 76.5%             |
| Pullover    | 73.0%             |
| Shirt       | 45.3%             |

**Overall accuracy: 83.1%**

Shirt is the hardest class — visually similar to T-shirt, Pullover and Coat. 
No linear boundary in raw pixel space can cleanly separate them. 
This is what motivates moving to deep learning (CNNs).

## Tech Stack
- Python, NumPy, Matplotlib, Seaborn
- TensorFlow/Keras (dataset loading only)
- Google Colab

## Run It
Open in Colab: [Click here](https://colab.research.google.com/drive/10uz9gx2vgWBj7FVZRe1zmfftnHww_woc)

## Key Takeaway
83.1% accuracy is near the practical ceiling for a linear classifier 
on raw pixels. The Shirt/T-shirt confusion is not a tuning problem — 
it's a structural one. The next step is CNNs.

---
*B.Sc. Computer Science | Machine Learning Course Project, 2026*
