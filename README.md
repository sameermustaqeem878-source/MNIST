
# MNIST Handwritten Digit Classifier

A deep learning project that recognizes handwritten digits (0–9) using a Convolutional Neural Network (CNN) built with TensorFlow and Keras.

The model is trained on the MNIST dataset and achieves **99.36% test accuracy**. The project also includes model evaluation, training checkpoints, result visualizations, and an interactive drawing canvas that allows users to draw their own digits and get predictions.

## Features

- Handwritten digit classification from 0 to 9.
- CNN-based image classification using TensorFlow and Keras.
- Image preprocessing and pixel normalization.
- Training with dropout layers to reduce overfitting.
- Early stopping to monitor validation performance.
- Automatic saving of the best model checkpoint.
- Training and validation performance tracking.
- Classification report with precision, recall, and F1-score.
- Confusion matrix for model evaluation.
- Visualization of sample images and predictions.
- Interactive drawing canvas for testing custom handwritten digits.
- Google Drive integration for saving trained models and results.

## Model Architecture

The CNN consists of two convolutional blocks followed by fully connected layers.

| Layer | Configuration |
|---|---|
| Convolutional Layer | 32 filters, 3×3, ReLU |
| Convolutional Layer | 32 filters, 3×3, ReLU |
| Max Pooling | 2×2 |
| Dropout | 0.25 |
| Convolutional Layer | 64 filters, 3×3, ReLU |
| Convolutional Layer | 64 filters, 3×3, ReLU |
| Max Pooling | 2×2 |
| Dropout | 0.25 |
| Flatten | Converts feature maps into a vector |
| Dense Layer | 128 neurons, ReLU |
| Dropout | 0.5 |
| Output Layer | 10 neurons, Softmax |

**Total Trainable Parameters:** 197,482

## Model Performance

The model was evaluated on the MNIST test dataset.

| Metric | Result |
|---|---:|
| Test Accuracy | 99.36% |
| Test Loss | 0.0235 |
| Macro F1-Score | 0.9936 |
| Weighted F1-Score | 0.9936 |

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- Google Drive
- HTML
- CSS
- JavaScript

## Project Structure

```text
mnist_project/
│
├── mnist_cnn.keras
├── history.json
├── sample_digits.png
├── confusion_matrix.png
└── sample_predictions.png
```

### Files Description

| File | Description |
|---|---|
| `mnist_cnn.keras` | Trained CNN model saved in Keras format. |
| `history.json` | Training and validation history. |
| `sample_digits.png` | Sample images from the MNIST dataset. |
| `confusion_matrix.png` | Confusion matrix of model predictions. |
| `sample_predictions.png` | Sample predictions on test images. |

## How It Works

1. Load the MNIST dataset containing handwritten digit images.
2. Normalize image pixel values for model training.
3. Prepare the images in the required CNN input format.
4. Build the CNN architecture using TensorFlow and Keras.
5. Train the model using convolutional and dense layers.
6. Apply dropout, early stopping, and model checkpointing.
7. Evaluate the trained model on test data.
8. Generate classification reports and a confusion matrix.
9. Save the best model and training history.
10. Use the interactive drawing canvas to test custom digits.

## Getting Started

This project was developed using Google Colab.

### 1. Clone the Repository

```bash
git clone https://github.com/sameermustaqeem878-source/MNIST_CNN.git
```

### 2. Open the Notebook

Open the project notebook in Google Colab.

### 3. Enable GPU

For faster training, select GPU from the Google Colab runtime settings.

`Runtime → Change runtime type → T4 GPU`

### 4. Mount Google Drive

Run the following code to connect Google Drive.

```python
from google.colab import drive
drive.mount('/content/drive')
```

### 5. Run the Notebook

Execute all notebook cells in order to preprocess the dataset, build the CNN, train the model, and evaluate its performance.

### 6. Test Your Own Digits

Run the interactive drawing canvas provided in the notebook.

Draw a digit from 0 to 9 and submit it to see the model's prediction and confidence score.

## Project Objective

This project demonstrates how deep learning and Convolutional Neural Networks can be used for handwritten digit recognition. It covers the complete image classification workflow, including data preprocessing, model development, training, evaluation, and interactive prediction.

## Author

**Muhammad Sameer Mustaqeem**

GitHub: [sameermustaqeem878-source](https://github.com/sameermustaqeem878-source)
