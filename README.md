# 🌿 Mango Leaf Disease Classification – MLOps Project  
**Higher National Diploma in Data Science (24.2f)**  
**Machine Learning 02 – Course Work 2**  
**Student: Senaya**

---

## 📌 Project Overview  
This project implements a **Deep Learning model** and a complete **MLOps workflow** for Mango Leaf Disease Classification.  
The work follows the CW2 guidelines:

- Problem definition & dataset explanation  
- Deep learning model development with **MLflow tracking**  
- MLOps components: **Git + GitHub**, **DVC**, **CI/CD**, **Docker**, **FastAPI**, **Model Monitoring**  
- Documentation & demonstration video  

---

# 🧩 1. Problem Definition  
### **Objective**  
To detect and classify **mango leaf diseases** using a deep-learning image classifier and deploy it using MLOps practices.

### **Assumptions**
- Images are correctly labelled.
- The training data represents real-world leaf conditions.
- The model will be used for decision support—not as a final medical diagnosis.

### **Limitations**
- Dataset size is limited.
- Images may vary in lighting/background conditions.
- Some rare diseases may not be included.

### **Dataset Description**
- A Mango Leaf Disease dataset (images) stored in the **`data/`** folder.
- Tracked using **DVC** to avoid GitHub file-size issues.
- Image classes include (example):  
  - Healthy  
  - Anthracnose  
  - Bacterial Spot  
  - Powdery Mildew  
- Preprocessing: resizing, normalization, augmentation.

---

# 🧩 2. Model Development (Using MLflow)
The model development pipeline includes:

### ✔️ Data Preprocessing  
- Resizing to 224×224  
- Normalization (1/255)  
- Augmentation (rotation, flip, zoom)

### ✔️ Deep Learning Model  
- Built using TensorFlow/Keras  
- CNN architecture with Conv2D, MaxPooling, Dense, Dropout  
- Metrics: accuracy, loss  

### ✔️ MLflow Integration  
- Experiment tracking  
- Hyperparameter logging  
- Metrics logging (train/validation accuracy)  
- Model versioning

### ✔️ Model Saving  
Final model saved as:  
