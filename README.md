# RNN Model on Time Series Dataset

This repository contains an implementation of a neural network model trained on a time series dataset related to spine conditions. The dataset used is `Dataset_spine.csv`, which contains various spine-related measurements and a classification target.

## Dataset
The dataset includes the following features:
- **pelvic_incidence**
- **pelvic_tilt**
- **lumbar_lordosis_angle**
- **sacral_slope**
- **pelvic_radius**
- **grade_of_spondylolisthesis**

The target variable is `class_att`, which represents the classification label.

## Preprocessing
- The dataset is read using Pandas and cleaned by stripping column names of whitespace and converting them to lowercase.
- The target variable is label-encoded and then one-hot encoded for categorical classification.
- The data is split into training and test sets (80/20 split).

## Model Architecture
A simple feedforward neural network (not an RNN) is implemented using TensorFlow/Keras:
- **Input Layer**: 64 neurons with ReLU activation.
- **Hidden Layer**: 32 neurons with ReLU activation.
- **Output Layer**: 2 neurons with softmax activation (binary classification).

## Training
The model is compiled with:
- **Optimizer**: Adam (learning rate = 0.001)
- **Loss Function**: Categorical Crossentropy
- **Metric**: Accuracy

The model is trained for **100 epochs** with a batch size of **32** and evaluated on the test set.

## Usage
 Install dependencies:
   ```bash
   pip install pandas numpy tensorflow scikit-learn
   ```





