# 🤖 K-Nearest Neighbors (KNN) Algorithm - From Scratch

**Day 1 of My Machine Learning Algorithms Learning Challenge**

> This project implements the K-Nearest Neighbors (KNN) classification algorithm from scratch in Python. No machine learning libraries are used for the core algorithm—everything is built from first principles to understand how KNN really works!

---

## 📖 What is KNN?

**K-Nearest Neighbors (KNN)** is one of the simplest and most intuitive machine learning algorithms. It's used for **classification tasks**, where the goal is to predict which category (class) a new data point belongs to.

The main idea is simple:
- **To predict a new data point, look at its K nearest neighbors in the training data**
- **Use the class labels of those neighbors to make a prediction**
- **Choose the class that appears most frequently (majority vote)**

Think of it like asking your closest friends for advice—the more similar the friends are to you, the better their advice!

---

## 🔄 How the Algorithm Works (Step by Step)

1. **Training Phase**: Store all the training data (features and labels)
   - KNN doesn't actually "learn" in the traditional sense—it just memorizes the data

2. **For Each Test Sample**:
   - Calculate the distance from the test sample to **every** training sample
   - Find the **K nearest** samples (smallest distances)
   - Look at the class labels of those K neighbors

3. **Make a Prediction**:
   - Count which class appears most often among the K neighbors
   - Assign that class to the test sample
   - This is called a **majority vote**

**Example**: 
- If you set K=5 and the 5 nearest neighbors have labels: [Setosa, Setosa, Versicolor, Setosa, Versicolor]
- You predict **Setosa** because it appears 3 times (majority)

---

## ✅ Why This is a Classification Problem (Not Regression)

**Classification vs. Regression:**

| Classification | Regression |
|---|---|
| Predicts **categories** (discrete classes) | Predicts **continuous numbers** |
| Example: "Is this email spam?" → Yes/No | Example: "What's the price of this house?" → $250,000 |
| Outputs: discrete labels | Outputs: any real number |

**This project uses classification** because:
- We're predicting **flower species** (Setosa, Versicolor, Virginica)
- The output is a **category**, not a number
- We use **accuracy** to measure performance (% of correct predictions)

---

## 📊 Dataset: The Iris Dataset

The **Iris dataset** is one of the most famous datasets in machine learning. It contains measurements of iris flowers.

### Dataset Details:
- **Total Samples**: 150 iris flowers
- **Total Features**: 4 measurements per flower
  - Sepal Length (cm)
  - Sepal Width (cm)
  - Petal Length (cm)
  - Petal Width (cm)
- **Target Classes**: 3 species
  - Class 0: **Setosa**
  - Class 1: **Versicolor**
  - Class 2: **Virginica**

### Data Split:
- **Training Data**: 120 samples (80%) — used to teach the model
- **Testing Data**: 30 samples (20%) — used to evaluate how well it learned

---

## 📁 Project Structure

```
KNN-Algorithm-ML-From-Scratch-01/
│
├── knn.py              # Main script - loads data and runs the model
├── knntest.py          # KNN class implementation (core algorithm)
├── requirements.txt    # Python dependencies
└── README.md           # This file
```

### File Explanations:

**`knn.py`** (Main Entry Point)
- Loads the Iris dataset
- Splits data into training and testing sets
- Creates a KNN classifier with K=5
- Makes predictions on test data
- Calculates and prints accuracy

**`knntest.py`** (Core Algorithm)
- Contains the `KNN` class
- Implements `fit()` method to store training data
- Implements `predict()` method to classify new samples
- Includes helper functions:
  - `euclidean_distance()`: Calculates distance between two points
  - `_predict()`: Predicts class for a single sample

---

## 🚀 How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/KNN-Algorithm-ML-From-Scratch-01.git
cd KNN-Algorithm-ML-From-Scratch-01
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Program
```bash
python knn.py
```

That's it! The script will:
- Load the Iris dataset
- Train the KNN model
- Make predictions on test data
- Print the accuracy

---

## 📈 Example Output

```
KNN classification accuracy: 0.967
```

This means **96.7% of predictions were correct**! Out of 30 test samples, the model correctly classified 29 of them.

---

## 💡 What I Learned From This Project

✅ **Understanding KNN from scratch**
- How distance calculation is fundamental to KNN
- Why the Euclidean distance formula works
- The importance of the K parameter

✅ **Core ML Concepts**
- The difference between training and testing data
- Why we split data (to avoid overfitting)
- How to measure classification performance with accuracy
- Majority voting and decision making

✅ **Python Programming**
- Working with NumPy arrays
- Using list comprehensions and loops efficiently
- Implementing classes and methods
- Using built-in functions like `Counter` for voting

✅ **Classification vs. Regression**
- When to use classification (categorical predictions)
- How classification differs from regression
- Evaluating classification models

---

## 🔮 Future Improvements

Here are features I can add to extend this project:

1. **Visualization**
   - Plot the decision boundary
   - Create scatter plots of the classified points
   - Show which neighbors were selected for a prediction

2. **Performance Optimization**
   - Test different K values and plot accuracy
   - Find the optimal K value
   - Compare performance metrics

3. **More Datasets**
   - Implement KNN on other datasets (MNIST, Breast Cancer, etc.)
   - Compare performance across datasets

4. **Advanced Metrics**
   - Add precision, recall, and F1-score
   - Create a confusion matrix
   - Plot ROC curves

5. **Code Enhancements**
   - Add unit tests
   - Handle edge cases
   - Optimize with KD-Tree for faster neighbor search
   - Add cross-validation

6. **Distance Metrics**
   - Implement Manhattan distance
   - Implement Cosine similarity
   - Compare different distance metrics

---

## 📚 Resources & Learning Materials

- [Wikipedia: K-Nearest Neighbors](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm)
- [Scikit-learn KNN Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)
- [Iris Dataset Info](https://en.wikipedia.org/wiki/Iris_flower_data_set)

---

## ✨ Key Takeaway

KNN is simple but powerful. By implementing it from scratch, I've learned that:
- **Simple algorithms can be very effective** when applied correctly
- **Understanding the basics is crucial** before using library implementations
- **Distance and similarity** are fundamental concepts in machine learning

---

**Happy Learning! 🚀**

---

*This is Day 1 of my ML Algorithms Challenge. Each day I'll implement a new algorithm and improve this project.*

