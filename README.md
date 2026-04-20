# MNIST Digit Classifier — From Scratch

Multi-class digit classification on the MNIST dataset, built entirely from scratch using **NumPy only** — no scikit-learn, no deep learning frameworks.

---

## What it does

The model takes a 28×28 grayscale image of a handwritten digit (0–9) and predicts which digit it is.  
It achieves **~89% accuracy** on the test set using a logistic regression trained with gradient descent.

---

## How it works

| Step | Description |
|------|-------------|
| **Softmax** | Converts raw scores into probabilities across 10 classes |
| **Cross-Entropy Loss** | Measures how far the predictions are from the truth |
| **Gradient Descent** | Adjusts weights to minimize the loss over 400 epochs |

Everything — forward pass, loss, gradient, weight update — is implemented manually using NumPy.

---

## Project Structure

```
mnist_scratch/
├── data/
│   └── mnist.csv              # Dataset (not versioned)
├── notebooks/
│   └── mnist_scratch.ipynb    # Main notebook
├── outputs/
│   ├── W.npy                  # Trained weights
│   ├── b.npy                  # Trained bias
│   ├── learning_curve.png    # Loss curve
│   └── confusion_matrix.png   # Confusion matrix
├── src/                       # (for future refactoring)
├── requirements.txt
└── README.md
```

---

## Getting Started

**1. Clone the repo**
```bash
git clone https://github.com/Sofyane00/mnist_scratch.git
cd mnist_scratch
```

**2. Create and activate a virtual environment**
```bash
python3 -m venv venv
source venv/bin/activate
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Add the dataset**  
Download `mnist.csv` from [Kaggle](https://www.kaggle.com/competitions/digit-recognizer/data) and place it in the `data/` folder.

**5. Launch Jupyter**
```bash
jupyter notebook --notebook-dir=notebooks/
```

---

## Draw & Predict

At the end of the notebook, a drawing window lets you test the model yourself — draw any digit with your mouse and the model predicts it in real time.

> Requires `Pillow`: `pip install Pillow`

---

## Results

| Metric | Value |
|--------|-------|
| Test Accuracy | ~89.40% |
| Training Epochs | 400 |
| Learning Rate | 0.1 |
| Dataset Size | 42,000 samples |

---

## Dependencies

```
numpy
pandas
matplotlib
jupyter
Pillow
```

---

## Author

**Sofyane** — built as a learning project to understand how logistic regression works under the hood.
