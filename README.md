# Autoencoder-Based Wireless Channel Matrix Estimation

## Overview
This project implements an **autoencoder-based deep learning model** for **wireless channel matrix estimation**. The encoder compresses both real and imaginary parts of the channel matrix, while the decoder reconstructs a **refined matrix** with optimized channel gains. The goal is to improve **spectral efficiency** and ensure robust communication between transmitter-receiver pairs.

## Folder Structure
```
.
├── .idea/                   # PyCharm project settings
├── __pycache__/             # Cached Python files
├── best_model.keras         # Best-performing model checkpoint
├── evaluate_model.py        # Script to evaluate the model on test data
├── final_model.keras        # Final trained model
├── generate_data.py         # Script for generating synthetic data
├── model.py                 # Autoencoder model definition
├── test_user_input.py       # Script to test the model with user-defined inputs
├── train_model.py           # Script to train the autoencoder model
├── X_train.npy              # Training data (real and imaginary parts)
├── X_val.npy                # Validation data
├── X_test.npy               # Test data
├── y_train.npy              # Training labels (refined matrices)
├── y_val.npy                # Validation labels
├── y_test.npy               # Test labels
```

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- TensorFlow/Keras
- NumPy
- Matplotlib

### Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Usage
### Training the Model
To train the autoencoder model, run:
```sh
python train_model.py
```
This will save the trained model as `final_model.keras`.

### Evaluating the Model
To evaluate the model on test data, use:
```sh
python evaluate_model.py
```

### Testing with User Inputs
To test the model with custom input data, run:
```sh
python test_user_input.py
```

## Data
The dataset consists of:
- `X_train.npy`, `X_val.npy`, `X_test.npy`: Channel matrices (real & imaginary parts)
- `y_train.npy`, `y_val.npy`, `y_test.npy`: Refined channel matrices as labels

## Model Architecture
The autoencoder consists of:
- **Encoder**: Compresses real & imaginary channel matrices
- **Decoder**: Reconstructs a refined matrix to improve spectral efficiency
- **Loss Function**: Mean Squared Error (MSE)
- **Optimizer**: Adam

## Results
- Improved spectral efficiency across communication channels
- Robust performance under varying channel conditions
- Reduced complexity compared to traditional estimation methods



