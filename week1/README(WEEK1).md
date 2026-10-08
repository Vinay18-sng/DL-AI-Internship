# Deep Learning & AI – Numerical Data Prediction

## 📌 About the Project

This project is part of my **Deep Learning and Artificial Intelligence internship**.

The objective of this task is to build a neural network that learns the relationship between input and output values from **generated numerical data** and then uses the learned pattern to predict outputs for **unseen inputs**.

This project helped me understand the basic concept of **regression using neural networks** and the complete workflow of training, testing, prediction, and evaluation.

---

## 🎯 Objective

> Build a model that learns a relationship from generated numerical data and predicts outputs for unseen inputs.

The dataset is generated using a known mathematical relationship:

```text
y = 3x + 5
```

The neural network learns this relationship from the training data and attempts to predict the corresponding output for new input values.

---

## 🧠 How the Project Works

The project follows these steps:

```text
Generate Numerical Data
        ↓
Prepare Training & Testing Data
        ↓
Build Neural Network
        ↓
Compile Model
        ↓
Train Model
        ↓
Test on Unseen Data
        ↓
Generate Predictions
        ↓
Compare Actual vs Predicted
        ↓
Analyze Loss Curve
```

---

## 📊 Dataset

Unlike projects that use a predefined dataset, this project generates its own numerical data.

The relationship used is:

```text
y = 3x + 5
```

For example:

```text
x       y
1       8
2       11
3       14
4       17
5       20
```

The first part of the generated data is used for training, while the remaining data is kept as unseen test data.

---

## 🛠️ Technologies Used

- **Python**
- **TensorFlow / Keras**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

---

## 🧠 Model Architecture

A simple fully connected neural network is used.

```text
Input
  │
  ▼
Dense Layer – 16 neurons
ReLU Activation
  │
  ▼
Dense Layer – 8 neurons
ReLU Activation
  │
  ▼
Output Layer – 1 neuron
  │
  ▼
Predicted Numerical Value
```

### Model Configuration

```text
Optimizer : Adam
Loss      : Mean Squared Error (MSE)
Metric    : Mean Absolute Error (MAE)
Epochs    : 100
```

---

## ⚙️ Training

The generated data is divided into training and testing sets.

The model learns from the training data and adjusts its weights to minimize the prediction error.

```python
model.fit(
    X_train,
    y_train,
    epochs=100,
    validation_split=0.1
)
```

---

## 🔮 Prediction on Unseen Data

After training, the model receives input values that were not used during training.

For example:

```text
Input: 81
Actual Output: 248
Predicted Output: approximately 248
```

The predicted values are compared with the actual values to determine how well the model learned the underlying relationship.

---

## 📈 Actual vs Predicted

The project includes an **Actual vs Predicted graph**.

This graph helps visualize how closely the model's predictions match the real output values.

If the predicted values are close to the actual values, it indicates that the model has learned the relationship effectively.

---

## 📉 Loss Curve

The project also generates a **training and validation loss curve**.

The loss represents the error between the actual and predicted values.

A decreasing loss during training indicates that the model is learning and reducing its prediction error.

---

## 📊 Results

The model successfully learns the relationship between the generated input and output values.

The predictions on unseen inputs are close to the actual outputs, showing that the neural network can learn a simple numerical relationship and generalize it to new data.

The loss curve also shows the model's learning process during training.

### Key Observations

- The model learns the underlying numerical pattern.
- Prediction error decreases during training.
- Predictions are close to actual values for unseen inputs.
- The model demonstrates basic regression using a neural network.

---

## ▶️ How to Run

The complete implementation is available in the Jupyter Notebook:

```text
week 2.ipynb
```

### Step 1 – Install Dependencies

```bash
pip install tensorflow numpy matplotlib
```

### Step 2 – Open the Notebook

Open **`week 1.ipynb`** using Jupyter Notebook or JupyterLab.

### Step 3 – Run the Cells

Run the cells from top to bottom.

The notebook will:

1. Generate numerical data.
2. Split the data into training and testing sets.
3. Build the neural network.
4. Compile the model.
5. Train the model.
6. Evaluate the model.
7. Predict outputs for unseen inputs.
8. Display actual vs predicted values.
9. Generate the loss curve.

---

## 📁 Project Structure

```text
Deep-Learning-AI/
│
├── week 2.ipynb
└── README.md
```

---

## 💡 What I Learned

Through this project, I gained practical experience in:

- Generating synthetic numerical data.
- Understanding input-output relationships.
- Splitting data into training and testing sets.
- Building neural networks using TensorFlow/Keras.
- Understanding regression problems.
- Using Mean Squared Error as a loss function.
- Training a model using the Adam optimizer.
- Making predictions on unseen data.
- Comparing actual and predicted values.
- Visualizing model performance using Matplotlib.
- Understanding how a neural network learns a mathematical relationship.

---

## 🚀 Future Improvements

I plan to improve this project by:

- Adding noise to the generated data.
- Testing different mathematical relationships.
- Comparing different neural network architectures.
- Performing hyperparameter tuning.
- Comparing neural networks with traditional regression models.
- Using real-world numerical datasets.
- Evaluating the model using additional regression metrics such as **RMSE and R² score**.

---

## 📝 Conclusion

This project provided practical experience with **neural network regression**.

By generating numerical data with a known relationship, training a neural network, and testing it on unseen inputs, I was able to understand how a deep learning model learns patterns and uses them to make predictions.

This project forms a foundation for applying regression techniques to more complex **real-world AI and machine learning problems**.

---

## 👨‍💻 Author

**K Vinay**

Artificial Intelligence & Machine Learning Student

**Internship:** Deep Learning & Artificial Intelligence

**Task:** Numerical Data Prediction using Neural Networks
