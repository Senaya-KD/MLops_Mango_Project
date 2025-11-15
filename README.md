# Mango Leaf Disease Classification – MLOps Project  
Higher National Diploma in Data Science (24.2f)  
Machine Learning 02 – Course Work 2  
---

## 1. Problem Definition

This project aims to classify mango leaf diseases using a deep learning model and apply MLOps concepts for proper version control and experiment reproducibility. The goal of the coursework is to build the model and set up versioning using Git and DVC.

### Problem Statement
To detect mango leaf diseases from images using a deep learning classification model.

### Assumptions
- Images in the dataset represent actual mango leaf diseases.
- Dataset labels are correct.
- The model is intended for educational and research purposes.

### Limitations
- Dataset size is limited.
- Variations in lighting and background may affect model performance.

### Dataset Description
- Dataset contains mango leaf images of different classes (e.g., Healthy, Anthracnose, Bacterial Spot, Powdery Mildew).
- Dataset is stored in the `data/` folder.
- Dataset is large, so it is tracked using **DVC** instead of uploading directly to GitHub.

---

## 2. Model Development (Completed)

Model development was done using Python and Jupyter Notebook.  
The following steps were completed:

### Data Preprocessing
- Image resizing (224×224)
- Normalization
- Augmentation to improve model generalization

### Model Architecture
A CNN model was trained using TensorFlow/Keras with:
- Convolution layers  
- MaxPooling layers  
- Fully connected layers  

### Model Saving
The final model was saved as:models/mango_leaf_model_run2_v2.h5
This `.h5` model file is tracked using **DVC**.
### Notebook
The full model development is available in the notebook:

---

## 3. Version Control (Git + GitHub + DVC)

Version control has been fully set up.

### Git & GitHub
- The complete project structure and source code are stored in a GitHub repository.
- All commits track code changes and project structure.

### DVC (Data Version Control)
DVC is used to track:
- The large dataset (`data/`)
- The trained model file (`models/mango_leaf_model_run2_v2.h5`)

Commands completed:
dvc init
dvc add data
dvc add models/mango_leaf_model_run2_v2.h5
git add data.dvc models/mango_leaf_model_run2_v2.h5.dvc
git commit -m "Track dataset and model with DVC"

Purpose of DVC:
- Avoid GitHub file size limits  
- Enable reproducible dataset/model versions  
- Keep Git repository lightweight

### Git Push Completed
All code, DVC metadata, and configuration files were successfully pushed to GitHub.


📊 Coursework Project — Mango Leaf Disease Classification – MLOps Project  
Institute: National Institute of Business Management (NIBM), Sri Lanka
Programme: Higher National Diploma in Data Science (HNDDS)
Student: Senaya Amarasinghe , Salma Zain. , Angel Fernando.

