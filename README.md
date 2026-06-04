#  MNIST Digit Classifier

In this project, I built a simple **Neural Network** with **TensorFlow/Keras** to classify handwritten digits from the famous **MNIST dataset**.  
The main goal was to compare two popular activation functions: **ReLU** vs **Tanh**. 

---

##  What I Did

1. **Data Loading & Preprocessing**
   - Loaded the MNIST dataset (60k training + 10k test images).  
   - Normalized pixel values to `[0, 1]` so the model trains faster.  
   - Converted labels to **one-hot encoded vectors**.

2. **Model Architecture**
   - A Sequential model with layers:  
     `128 → 64 → 32 → 10` neurons.  
   - Built two versions: one with **ReLU**, one with **Tanh**.  

3. **Training**
   - Trained both models for **10 epochs**.  
   - Used **Adam optimizer** and **categorical crossentropy loss**.  

4. **Evaluation**
   - Calculated accuracy on the test set.  
   - Plotted confusion matrices.  
   - Drew training curves (accuracy & loss).  
   - Displayed examples of **misclassified digits**.  

---

##  Results in Simple Words

- 🔹 **ReLU** learned faster and reached higher accuracy.  
- 🔹 **Tanh** also worked but trained slower and made a few more mistakes.  
- 🔹 Digits like `3 vs 5` or `4 vs 9` were often confused. 

---

##  Tools Used
- Python   
- TensorFlow / Keras  
- NumPy  
- Matplotlib & Seaborn (for plots & confusion matrices)  
- Scikit-learn  

---
## Results

| Model | Test Accuracy |
|-------|--------------|
| ReLU  | 97.62%       |
| Tanh  | 97.29%       |

**Key Findings:**
- ReLU converged faster and achieved higher accuracy
- Tanh showed greater stability with less validation loss fluctuation
- Most common misclassification: digit 9 confused with 7 (28 cases in ReLU)
- Dataset: 70,000 MNIST images (60K train / 10K test), 10-class classification
- Architecture: Sequential neural network (128→64→32→10 neurons)
