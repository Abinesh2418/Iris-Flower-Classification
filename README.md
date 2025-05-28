# 🌸 Iris Flower Classification Using Neural Networks

This project focuses on classifying Iris flowers into their respective species using a neural network built with TensorFlow/Keras. The Iris dataset is a classic dataset widely used for multiclass classification problems, consisting of measurements of sepal and petal lengths and widths.

## 📊 Dataset Description

The Iris dataset contains **150 samples** of iris flowers, with **four features**:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width
And a **target** variable which classifies the flower into one of the three species:
- Setosa (0)
- Versicolor (1)
- Virginica (2)
  
## 🧹 Data Preprocessing

- **Loaded the dataset** using `sklearn.datasets.load_iris`.
- **Converted it into a Pandas DataFrame** for easier manipulation.
- **Added the target column** representing the species labels.
- **Checked for missing values** to ensure data integrity.
- **Visualized feature correlations** using a heatmap to understand the relationship between different features.
- **Split** the data into training and test sets using `train_test_split` (70% training, 30% testing).
- **Standardized** the feature values using `StandardScaler` to bring all features to the same scale, which helps the neural network converge faster and perform better.

---

## 🧠 Model Building (Neural Network)

We used `Sequential` from Keras to build a feedforward neural network:

- **Input Layer**: Automatically inferred shape based on training data features.
- **Hidden Layers**:
  - Dense layer with 64 units, ReLU activation.
  - Dense layer with 32 units, ReLU activation.
- **Output Layer**:
  - Dense layer with 1 unit and `softmax` activation (NOTE: For multi-class classification, this should ideally have 3 units instead of 1).

The model was compiled with:
- **Optimizer**: Adam
- **Loss Function**: `categorical_crossentropy` (appropriate for multi-class classification)
- **Metrics**: Accuracy

> ⚠️ The output layer should use `Dense(3, activation='softmax')` and the targets should be one-hot encoded for proper classification. The current setup may not work as expected.

---

## 🏋️ Model Training

- Trained the model for **100 epochs** with a **batch size of 32**.
- Evaluated the model on the test set and obtained:
  - **Test Loss**: `0.0000`
  - **Test Accuracy**: `28.89%` (which indicates the model may not be learning correctly due to the output layer or loss mismatch)

---
## 🔍 Model Evaluation and Prediction

- **Predicted the labels** for the test set.
- Compared the predicted values to the actual values using `np.max(preds[i])` and `y_test`.

---

## 📬 Contact

For any queries or suggestions, feel free to reach out:

- 📧 Email: [abineshbalasubramaniyam@example.com](mailto:abineshbalasubramaniyam@example.com)
- 💼 LinkedIn: [linkedin.com/in/abinesh-b-1b14a1290/](https://www.linkedin.com/in/abinesh-b-1b14a1290/)
