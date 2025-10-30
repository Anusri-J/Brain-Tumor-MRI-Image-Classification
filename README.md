**🧠 Brain_Tumor_MRI_Image_Classification**

A deep learning–based project that classifies brain MRI scans into four tumor categories — glioma, meningioma, pituitary, and no_tumor — using Custom CNN and Transfer Learning (EfficientNetB0) models.
It also features a Streamlit web application that allows real-time predictions directly from uploaded MRI images.

**📌 Project Overview**

This project focuses on:

🧬 Automatically classifying MRI brain images into multiple tumor types.

⚙️ Building and comparing a Custom CNN and EfficientNetB0 (transfer learning) model.

📊 Evaluating and visualizing model performance with accuracy, confusion matrix, and F1-score.

🌐 Deploying a Streamlit app for real-time predictions.

🏥 Supporting medical imaging workflows for research and diagnostics.

**🧠 Skills Gained**

✅ Deep Learning with TensorFlow / Keras

✅ Image Data Preprocessing and Augmentation

✅ Transfer Learning and Fine-Tuning

✅ Model Evaluation and Comparison

✅ Streamlit App Development and Deployment

✅ Real-Time AI Prediction Interface

**🧩 Steps Involved**

**✅ Step 1: Understand the Dataset**

Explored MRI images belonging to 4 categories — glioma, meningioma, pituitary, and no_tumor.
Checked for class imbalance, resolution consistency, and dataset distribution.

**✅ Step 2: Data Preprocessing**

Resized all images to 224×224, normalized pixel values to [0, 1], and split into training, validation, and test sets.

**✅ Step 3: Data Augmentation**

Applied rotation, zoom, flipping, brightness, and shifting transformations to improve model generalization.

**✅ Step 4: Model Building**

Built two models:

**🧱 Custom CNN:** 3 convolutional layers + dropout + batch normalization.

**⚙️ EfficientNetB0:** Fine-tuned pretrained ImageNet weights for better accuracy.

**✅ Step 5: Model Training**

Trained both models with callbacks like EarlyStopping, ModelCheckpoint, and ReduceLROnPlateau.
Saved best-performing models in .keras format for compatibility with Keras 3.

**✅ Step 6: Model Evaluation**

Measured accuracy, precision, recall, F1-score, and plotted confusion matrices to assess performance.

**✅ Step 7: Model Comparison**

Compared Custom CNN vs. EfficientNetB0 based on validation accuracy and inference speed.

**✅ Step 8: Streamlit Deployment**

Developed a user-friendly web app where users upload MRI images and get instant predictions with confidence scores and probability bars.


**📊 Sample Outputs**

**🎯 Prediction Example:**

Upload MRI image → Model predicts Glioma (96.3%) confidence.

Bar chart displays probabilities for all 4 tumor types.

**📈 Model Results:**

|**Model**	|**Accuracy**	|**Remarks** |
|-----------|-----------|-----------|
|Custom CNN	| ~91%	| Built from scratch, compact architecture|
|EfficientNetB0	|~96%	| Transfer learning, best performing model |

**🛠️ Tech Stack Used**

✅ Python — Core language

✅ TensorFlow / Keras — Deep learning framework

✅ NumPy / Pandas — Data handling

✅ Matplotlib / Seaborn — Visualization

✅ Streamlit — Web app deployment

✅ Pyngrok — Colab integration for live deployment

✅ Pillow — Image handling for uploads and annotations

📂 Dataset

**Source:** Tumour (Updated)

**Classes:**
🧩 Glioma

🧩 Meningioma

🧩 Pituitary

🧩 No_tumor

**Structure:**

```dataset/
 ├── train/
 │   ├── glioma/
 │   ├── meningioma/
 │   ├── no_tumor/
 │   └── pituitary/
 ├── valid/
 └── test/```

**🧩 Streamlit App Features**

✅ Upload MRI image (.jpg, .png, .jpeg)

✅ Choose model — Custom CNN or EfficientNetB0

✅ Display tumor type + confidence percentage

✅ Show probability bar chart and table

✅ Option to download annotated result image

**💻 Run the Streamlit App**

```!nohup streamlit run app.py --server.port 8501 &>/content/streamlit.log &
from pyngrok import ngrok
print("Streamlit App URL:", ngrok.connect(8501))```

**🧮 Key Learnings**

✅ Building custom CNNs for image classification

✅ Fine-tuning pretrained models (transfer learning)

✅ Optimizing models using callbacks and learning rate reduction

✅ Evaluating with multiple metrics for reliability

✅ Creating interactive apps for real-world deployment

**🎯 Business Use Cases**

🏥 AI-Assisted Diagnosis – Helps radiologists classify MRI scans quickly and accurately.

⏱️ Early Detection & Triage – Flags high-risk patients faster for review.

🧬 Clinical Research – Supports dataset segmentation and patient grouping by tumor type.

🌐 Telemedicine / Second Opinion – Enables remote diagnostics via the web.

**🛠️ Tech Configuration**

TensorFlow: 2.17.1

Keras: 3.4.1

NumPy: 1.26.4

ml_dtypes: 0.4.x (stable)

GPU: Enabled

Model Format: .keras

**📎 References**

**TensorFlow Official Docs :** https://www.tensorflow.org/

**Keras Documentation :** https://keras.io/

**Streamlit Documentation :** https://docs.streamlit.io/

**EfficientNet Paper – Tan & Le, 2019:** https://arxiv.org/abs/1905.11946
