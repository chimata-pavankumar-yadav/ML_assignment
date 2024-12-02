# ML_assignment
improve decision tree model accuracy by adjusting hyperparameters

# Titanic Survival Prediction Using Decision Tree Classifier

This project demonstrates the use of a **Decision Tree Classifier** to predict the survival of passengers aboard the Titanic, based on historical data. The focus of this project is to explore the impact of various hyperparameters on the performance and accuracy of the model.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Hyperparameters Analyzed](#hyperparameters-analyzed)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [How to Run the Code](#how-to-run-the-code)


## Introduction
The goal of this project is to build an interpretable machine learning model using the Titanic dataset. The Decision Tree algorithm was selected for its simplicity, interpretability, and effectiveness in classification tasks. Special emphasis is placed on hyperparameter tuning to understand how adjustments affect the model's accuracy and ability to generalize.

## Dataset
The dataset is the well-known **Titanic dataset** from [OpenML](https://www.openml.org/). It includes features such as:
- Passenger class (`pclass`)
- Gender (`sex`)
- Age (`age`)
- Number of siblings/spouses aboard (`sibsp`)
- Number of parents/children aboard (`parch`)
- Fare (`fare`)
- Embarked port (`embarked`)
- Survival status (`survived`) - Target variable

### Data Preprocessing
- Missing values were handled (e.g., imputed missing ages with the median).
- Categorical variables like `sex` and `embarked` were encoded as numerical values.
- Features were standardized where necessary for consistency.

## Project Workflow
1. **Data Loading**: Load and preprocess the Titanic dataset.
2. **Model Building**: Train a Decision Tree Classifier.
3. **Hyperparameter Analysis**:
   - Evaluate the impact of hyperparameters like `criterion`, `max_depth`, `min_samples_split`, `min_samples_leaf`, and `max_leaf_nodes`.
4. **Visualization**: Plot accuracy metrics for each hyperparameter to identify optimal configurations.
5. **Final Evaluation**: Use the best hyperparameters to maximize model accuracy.

## Hyperparameters Analyzed
The following hyperparameters were analyzed in depth:
- **`criterion`**: Splitting criteria (Gini or Entropy).
- **`max_depth`**: Maximum depth of the tree.
- **`min_samples_split`**: Minimum number of samples required to split an internal node.
- **`min_samples_leaf`**: Minimum number of samples required to form a leaf.
- **`max_leaf_nodes`**: Maximum number of leaf nodes allowed in the tree.

## Results
- **Accuracy Improvement**: By fine-tuning hyperparameters, the model's accuracy improved from 78% to 80%.
- **Optimal Parameters**:
  - `criterion`: Entropy
  - `max_depth`: 5
  - `min_samples_split`: 10
  - `min_samples_leaf`: 5
  - `max_leaf_nodes`: 20

These hyperparameters provided the best balance between complexity and generalization.

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - Pandas, NumPy: Data manipulation and analysis
  - Scikit-learn: Machine learning algorithms and evaluation metrics
  - Matplotlib: Data visualization

## How to Run the Code
1. Clone this repository:
   ```bash
   git clone https://github.com/your_username/titanic-decision-tree.git
   
2. Navigate to the project directory:
```bash   
   cd titanic-decision-tree
```
3. Install the required dependencies:
```bash
   pip install -r requirements.txt
```
4. Run the script:
```bash
   python decision_tree_titanic.py
```

