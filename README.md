# 🥔 Potato Disease Classification using Convolutional Neural Networks (CNN)

A deep learning-based image classification system that detects diseases in potato leaves using a Convolutional Neural Network (CNN) built with TensorFlow and Keras. The model classifies potato leaf images into one of three categories:

- 🌿 Healthy
- 🍂 Early Blight
- 🍁 Late Blight

This project demonstrates the complete deep learning pipeline—from dataset preprocessing and augmentation to model training, evaluation, and visualization.

---

## 📌 Features

- Image classification using a custom CNN architecture
- Automatic dataset loading using TensorFlow
- Data preprocessing and normalization
- Data augmentation for improved generalization
- Train, validation, and test dataset splitting
- Model training with TensorFlow/Keras
- Model checkpointing to save the best-performing model
- Training and validation accuracy/loss visualization

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib

---

## 📂 Project Structure

```
Potato-Disease-Classification/
│
├── potato_disease_classification.ipynb
├── requirements.txt
├── README.md
├── .gitignore
└── Dataset/
    ├── Potato___Early_blight/
    ├── Potato___Late_blight/
    └── Potato___healthy/
```

> **Note:** The `Dataset` folder is **not included** in this repository because of its size.

---

## 📊 Dataset

This project uses the **PlantVillage** dataset, one of the most widely used benchmark datasets for plant disease classification. It contains healthy and diseased leaf images collected under controlled conditions and includes the three potato classes used in this project. :contentReference[oaicite:0]{index=0}

### Download Dataset

You can download the dataset from Kaggle:

**https://www.kaggle.com/datasets/emmarex/plantdisease** :contentReference[oaicite:1]{index=1}

After downloading, extract the potato leaf folders into the following directory structure:

```
Dataset/
├── Potato___Early_blight/
├── Potato___Late_blight/
└── Potato___healthy/
```

---

## 🧠 Model Architecture

The CNN model consists of:

- Image Rescaling
- Multiple Conv2D layers
- MaxPooling layers
- Flatten layer
- Dense hidden layer
- Softmax output layer

Architecture:

```
Input Image (256 × 256 × 3)
        │
Rescaling (1/255)
        │
Conv2D + ReLU
        │
MaxPooling
        │
Conv2D + ReLU
        │
MaxPooling
        │
Conv2D + ReLU
        │
MaxPooling
        │
Conv2D + ReLU
        │
MaxPooling
        │
Conv2D + ReLU
        │
MaxPooling
        │
Conv2D + ReLU
        │
MaxPooling
        │
Flatten
        │
Dense (64)
        │
Softmax (3 Classes)
```

---

## ⚙️ Training Configuration

| Parameter | Value |
|-----------|-------|
| Image Size | 256 × 256 |
| Batch Size | 32 |
| Epochs | 30 |
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Output Activation | Softmax |

---

## 📈 Data Preprocessing

The dataset undergoes the following preprocessing steps:

- Dataset loading using `image_dataset_from_directory`
- Train/Validation/Test split
- Image normalization
- Random horizontal & vertical flipping
- Random rotation
- Dataset caching
- Shuffling
- Prefetching for faster training

---

## 💾 Model Checkpoint

The project uses TensorFlow's `ModelCheckpoint` callback to save the best model based on validation accuracy during training.

---

## 📉 Results

The notebook generates:

- Training Accuracy Curve
- Validation Accuracy Curve
- Training Loss Curve
- Validation Loss Curve

You can optionally include screenshots of these plots in an `images/` folder and reference them here.

Example:

```markdown
![Accuracy](images/accuracy.png)

![Loss](images/loss.png)
```

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/Potato-Disease-Classification.git
```

Move into the project directory:

```bash
cd Potato-Disease-Classification
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

1. Download the dataset.
2. Place it inside the `Dataset/` folder.
3. Open the notebook:

```bash
jupyter notebook
```

4. Run all notebook cells sequentially.

---

## 👤 Author

**Preetham Epuri**

---

## ⭐ If you found this project useful, consider giving it a star!
