# Neural Network Analysis – Customer Churn Prediction

## Objective
This project demonstrates the complete workflow of building and analyzing a feed-forward neural network for customer churn prediction.

The project includes:

- Dataset exploration
- Data preprocessing
- Neural network implementation
- Training and evaluation
- Hyperparameter experimentation
- Final analysis and reflection

---

# Dataset Information

Dataset: `customer_churn_nn.csv`

Target Variable:
- `churn`
  - 1 → Customer churned
  - 0 → Customer retained

Categorical Features:
- region
- plan_type
- contract_type
- payment_method

Numerical Features:
- tenure
- monthly_charges
- total_charges
- login_days
- support_tickets
- delivery_delays
- data_usage
- satisfaction_score
- complaint_recency
- discounts_used
- referrals

Identifier Column:
- customer_id (removed during modeling)

---

# Project Structure

part-1-neural-network-analysis/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
└── results/
    ├── model_comparison_table.csv
    └── evaluation_outputs.png

---

# Steps Performed

## 1. Dataset Understanding
- Checked dataset dimensions
- Examined data types
- Identified missing values
- Generated statistical summaries
- Visualized churn distribution

## 2. Data Preprocessing
- Removed identifier column
- Encoded categorical variables using One-Hot Encoding
- Scaled numerical features using StandardScaler
- Split dataset into training and testing sets

## 3. Neural Network Model
A feed-forward neural network was built using TensorFlow/Keras.

Architecture:
- Input Layer
- Hidden Layer(s)
- ReLU activation
- Output Layer with Sigmoid activation

Loss Function:
- Binary Crossentropy

Optimizer:
- Adam

Evaluation Metrics:
- Accuracy
- Confusion Matrix
- Classification Report

---

# Hyperparameter Experiments

Experiments were conducted by changing:
- Hidden layers
- Number of neurons
- Learning rate
- Batch size
- Epochs
- Activation functions

Performance comparison is stored in:
`results/model_comparison_table.csv`

---

# Final Reflection

## Role of Weights and Biases
Weights determine the importance of each input feature, while biases help shift activation values to improve learning flexibility.

## Why Activation Functions are Needed
Activation functions introduce non-linearity, allowing neural networks to learn complex relationships.

## Learning Rate Effects
- Too High → unstable training and overshooting minima
- Too Low → slow learning and long training time

## Underfitting vs Overfitting
- Underfitting occurs when the model is too simple
- Overfitting occurs when the model memorizes training data and performs poorly on unseen data

The experiments helped balance model complexity and generalization performance.

---

# Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
