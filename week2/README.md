# Deep Learning & AI – MNIST Handwritten Digit Classification

##  About the Project

This project is part of my **Deep Learning and Artificial Intelligence internship**.

As a first practical implementation, I worked with the **MNIST handwritten digit dataset** to understand how a neural network learns from image data and classifies handwritten digits from **0 to 9**.

The project covers the complete basic workflow of a deep learning model, including data preprocessing, model building, training, evaluation, prediction, and visualization.

---

##  Objectives

- Understand the basic concepts of neural networks.
- Work with an image classification dataset.
- Preprocess and normalize image data.
- Build a neural network using TensorFlow/Keras.
- Train and validate the model.
- Evaluate the model on unseen test data.
- Compare actual and predicted values.
- Analyze model performance using a loss curve.

---

##  Dataset – MNIST

The **MNIST dataset** contains handwritten digits from 0 to 9.

| Feature | Details |
|---|---|
| Training images | 60,000 |
| Test images | 10,000 |
| Image size | 28 × 28 pixels |
| Image type | Grayscale |
| Number of classes | 10 |
| Classes | 0–9 |

The pixel values range from **0 to 255**. They are normalized to **0–1** before being given to the neural network.

---

##  Technologies Used

- **Python**
- **TensorFlow**
- **Keras**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

---

##  Neural Network Architecture

The project uses a basic fully connected neural network.

```text
                  MNIST Image
                  28 × 28
                     │
                     ▼
                  Flatten
                     │
                     ▼
              Dense – 128 neurons
                 ReLU
                     │
                     ▼
              Dense – 64 neurons
                 ReLU
                     │
                     ▼
              Dense – 10 neurons
                Softmax
                     │
                     ▼
             Predicted Digit
                  0 – 9
```

### Model Configuration

```text
Optimizer        : Adam
Loss Function    : Sparse Categorical Crossentropy
Evaluation       : Accuracy
Epochs           : 5
Validation Split : 10%
Output Classes   : 10
```

---

## ⚙️ Data Preprocessing

The MNIST images are originally represented using pixel values between 0 and 255.

To make the data suitable for neural network training, the values are normalized:

```python
x_train = x_train / 255.0
x_test = x_test / 255.0
```

This converts the pixel values into the range:

```text
0 → 0.0
255 → 1.0
```

Normalization helps the neural network train more effectively.

---

##  Model Training

The model is trained using the MNIST training dataset.

During training, a portion of the training data is used for validation:

```python
history = model.fit(
    x_train,
    y_train,
    epochs=5,
    validation_split=0.1
)
```

The training history is used to analyze how the model learns over each epoch.

---

##  Loss Curve

The loss curve compares:

- Training Loss
- Validation Loss

The loss generally decreases as training progresses, indicating that the model is learning patterns from the training data.

This visualization also helps identify possible **overfitting or underfitting**.

---

##  Actual vs Predicted

After training, the model predicts digits from the test dataset.

The predicted class is obtained using:

```python
predicted_digit = np.argmax(predictions[i])
```

The predicted values are then compared with the actual labels.

Example:

```text
Image 1 → Actual: 7 | Predicted: 7
Image 2 → Actual: 2 | Predicted: 2
Image 3 → Actual: 1 | Predicted: 1
Image 4 → Actual: 0 | Predicted: 0
```

When the actual and predicted values are the same, the model has classified the image correctly.

---

##  Results

The trained neural network successfully learned patterns from the MNIST handwritten digit images.

The results were analyzed using:

- Test loss
- Test accuracy
- Training and validation loss curve
- Actual vs predicted values

The model correctly predicts most of the test images, demonstrating that a basic neural network can be effectively used for handwritten digit classification.

---

##  How to Run

The complete implementation is available in the Jupyter Notebook:

```text
week 1.ipynb
```

### Step 1 – Install Dependencies

```bash
pip install tensorflow numpy matplotlib
```

### Step 2 – Open the Notebook

Open:

```text
week 1.ipynb
```

using **Jupyter Notebook** or **JupyterLab**.

### Step 3 – Run the Cells

Run the notebook cells from top to bottom.

The notebook will:

1. Load the MNIST dataset.
2. Normalize the image data.
3. Build the neural network.
4. Compile the model.
5. Train the model.
6. Evaluate test performance.
7. Display actual vs predicted values.
8. Generate the loss curve.

---

##  Project Structure

```text
Deep-Learning-AI/
│
├── week 1.ipynb
└── README.md
```

---

##  Key Learning Outcomes

This project helped me gain practical experience in:

- Fundamentals of Artificial Intelligence and Deep Learning
- Neural network architecture
- Image classification
- Data preprocessing
- Data normalization
- Dense layers
- ReLU activation
- Softmax activation
- Model compilation
- Model training and validation
- Loss functions
- Model evaluation
- Prediction and classification
- Visualization using Matplotlib

---

##  Future Improvements

I plan to extend this project by:

- Implementing a **Convolutional Neural Network (CNN)**.
- Comparing ANN and CNN performance.
- Adding a **confusion matrix**.
- Performing hyperparameter tuning.
- Applying regularization techniques.
- Building a web-based digit recognition application.
- Allowing users to draw handwritten digits and receive predictions in real time.

---

##  Conclusion

This project provided a practical introduction to **Deep Learning and Artificial Intelligence** through handwritten digit classification.

It helped me understand the complete workflow of a neural network — from preparing the dataset and building the model to training, evaluation, prediction, and result visualization.

This project also provides a foundation for moving towards more advanced deep learning techniques such as **CNNs, computer vision, and real-world image classification applications**.

---

##  Author

**K Vinay**

Artificial Intelligence & Machine Learning Student

**Internship:** Deep Learning & Artificial Intelligence

**Project:** MNIST Handwritten Digit Classification
