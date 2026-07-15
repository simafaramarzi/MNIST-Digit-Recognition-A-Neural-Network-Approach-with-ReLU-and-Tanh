# MNIST Digit Classifier: ReLU vs. Tanh

A neural network built with TensorFlow/Keras to classify handwritten digits from the MNIST dataset, comparing two activation functions — **ReLU** and **Tanh** — to see how each affects accuracy, convergence speed, and overfitting.

## Results

| Model | Train Accuracy | Validation Accuracy |
|---|---|---|
| **ReLU** | 97.62% | ~97.8% |
| **Tanh** | 97.29% | ~97.7% |

ReLU converged faster and generalized slightly better, with more stable validation accuracy throughout training. Tanh performed comparably overall but showed mild overfitting in later epochs — validation accuracy dipped slightly as validation error increased.

## What I Did

1. **Data Loading & Preprocessing**
   - Loaded the MNIST dataset (60k training + 10k test images)
   - Normalized pixel values to `[0, 1]`
   - One-hot encoded the labels

2. **Model Architecture**
   - Sequential model: `128 → 64 → 32 → 10` neurons (~111,000 trainable parameters)
   - Built two versions: one with ReLU, one with Tanh in the hidden layers

3. **Training**
   - 10 epochs, Adam optimizer, categorical crossentropy loss

4. **Evaluation**
   - Accuracy and loss curves for both models
   - Confusion matrices to see where each model struggled
   - Visualized misclassified digits (commonly confused: 3 vs 5, 4 vs 9)

## How to Run

```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
jupyter notebook mnist_relu_vs_tanh.ipynb
```

## Tools

Python · TensorFlow/Keras · NumPy · Matplotlib · Seaborn · Scikit-learn

## About

Originally built as part of the Artificial Intelligence and Neural Networks module in my M.Sc. Data Science program (Arden University Berlin).
