# Car Damage Assessment and Cost Estimation using Deep Learning

## Overview
The goal of this project is to **automatically detect the severity of a car’s damage** from an image and **estimate the approximate repair cost** based on that severity.  
The system combines **computer vision and machine learning** to provide a fully automated, end-to-end solution for vehicle damage assessment and cost estimation.

---

## Key Features
- Detects and classifies car damage into three severity levels:
  - **Less Damage**
  - **Moderate Damage**
  - **Severe Damage**
- Estimates repair cost based on predicted severity.
- Visualizes uploaded car images with severity and estimated cost.
- End-to-end automated workflow suitable for insurance or automobile applications.

---

## Methodology

### 1. Hybrid Deep Learning Model
A hybrid CNN model combining **ResNet50** and **DenseNet169** architectures was used:

- **ResNet50**: Captures deep hierarchical and global features using residual connections, which prevent vanishing gradients.
- **DenseNet169**: Efficiently reuses features to capture fine local textures and edges.
- **Feature Fusion**: Output feature maps from both networks are concatenated to create a rich, comprehensive feature representation.
- **Additional Layers**: Batch Normalization (stabilizes training), Dense layer (learns complex relationships), and Dropout (prevents overfitting).

**Workflow:**
1. Input image is processed by both ResNet50 and DenseNet169.
2. Feature maps from both networks are concatenated.
3. Concatenated features pass through Batch Normalization, Dense, and Dropout layers.
4. Final output predicts one of the three damage severity classes.

---

### 2. Model Training
- Dataset: Car damage images split into **training, validation, and testing sets**.
- Epochs: 50
- Training Accuracy: ~48% → 88%
- Validation Accuracy: ~60–65% (slight overfitting observed)
- Evaluation Metrics: Confusion Matrix, Classification Report (precision, recall, F1-score)

---

### 3. Cost Estimation
- Linear Regression model maps predicted damage severity to an estimated repair cost.
- Synthetic dataset ranges:
  - **Less Damage**: ₹4000 – ₹8000
  - **Moderate Damage**: ₹8000 – ₹15000
  - **Severe Damage**: ₹15000 – ₹35000
- Regression predicts practical repair costs based on severity, providing actionable results.

---

## Workflow
1. User uploads an image of the damaged car.
2. Hybrid CNN predicts the **damage severity**.
3. Linear Regression estimates the **repair cost**.
4. System displays the car image with:
   - Predicted severity
   - Estimated repair cost

Example output:  
If predicted severity = **Less Damage**, estimated cost might be **₹4700**.

---

## Results
- Achieved high classification accuracy in detecting damage severity.
- Visual output shows severity and estimated repair cost clearly.
- Provides practical, actionable results for mechanics, insurance agents, and car owners.

---

## Future Enhancements
- Train on a larger and more diverse dataset to reduce overfitting.
- Expand damage categories for more granular classification.
- Integrate a **web or mobile interface** for user-friendly image uploads.
- Improve cost estimation using real-world repair data and regression enhancements.

---

## Author
**Navya Sri Kolli**  
- B.Tech CSE (AI & ML)  
- GitHub: [https://github.com/navyasri1112]
- Email: navyasri9292@gmail.com

