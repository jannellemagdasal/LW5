# Laboratory Work 5 Activity | Comparative Analysis

Laboratory Work 5 Activity
Comparative Analysis of Pre-trained CNN Models for
Custom Image Classification

PART 1: Dataset Preparation
<img width="671" height="851" alt="image" src="https://github.com/user-attachments/assets/3f200553-d46c-4201-aacd-8a9f3e0b0750" />

PART 2: Load Dataset in Colab
<img width="537" height="117" alt="image" src="https://github.com/user-attachments/assets/9dfb9dfd-2c2c-43f2-ab28-bd2b28891ad6" />


PART 3: Data Preprocessing
<img width="387" height="110" alt="image" src="https://github.com/user-attachments/assets/f7d63418-7c69-4876-8f57-184b441bb738" />

PART 4: Define Pre-trained Model Function
<img width="827" height="97" alt="image" src="https://github.com/user-attachments/assets/c1b816f6-2499-44ea-93bc-f076f549ed14" />


PART 5: Load Pre-trained Models
<img width="811" height="253" alt="image" src="https://github.com/user-attachments/assets/22f91ab1-3f24-4529-836e-4f76d77ff610" />

PART 6: Train Each Model
<img width="500" height="508" alt="image" src="https://github.com/user-attachments/assets/5f4e9832-fedd-4770-9028-15c9ba3175f7" />


PART 7: Evaluation Metrics (Core Requirement)
<img width="535" height="501" alt="image" src="https://github.com/user-attachments/assets/fa6aa66a-37ce-48fa-b939-4b5f354a0e26" />

PART 8: Confusion Matrix Plot
<img width="1185" height="683" alt="image" src="https://github.com/user-attachments/assets/11a58403-a78e-43e5-93f1-37ef832b8278" />
<img width="1155" height="599" alt="image" src="https://github.com/user-attachments/assets/28554244-228f-4b54-9c0a-f74fbe070ff5" />

PART 9: ROC Curve & AUC
<img width="513" height="460" alt="Screenshot 2026-04-27 230010" src="https://github.com/user-attachments/assets/922216bd-f33d-4562-86a8-2a4693c40426" />


PART 10: Grad-CAM (Explainability)
Grad-CAM Visualization
1. DenseNet121 — ROC/AUC Excellent (≈0.99)
Visualization:
The Grad-CAM heatmap consistently highlights the precise, relevant parts of input images—such as the unique leaf patterns or core features of each plant.
Most activation regions are tightly clustered around the object of interest with minimal 'leak' onto the background.
Interpretation:
This model’s high accuracy and metrics are reflected in very focused and interpretable attention regions, supporting trustworthy predictions.

2. MobileNetV2 — ROC/AUC Excellent (≈0.99)
Visualization:
Grad-CAM maps show strong, well-localized activations covering the significant object areas. In most cases, feature highlights overlap largely with the main distinguishing characteristics (e.g., shape, edges).
Interpretation:
Almost as precise as DenseNet121, the highlighted areas are mostly within the object, with only occasional minor spillage onto irrelevant regions. This supports its superior performance.

3. EfficientNetB0 — ROC/AUC Excellent (≈0.99)
Visualization:
The Grad-CAM heatmaps still generally cover the main object, but sometimes are slightly broader or less sharp versus the top two models.

In some misclassified samples, attention occasionally covers both the object and some background/neighboring features.
Interpretation:
Still provides useful and interpretable focus, but with slightly less confidence and precision in complex scenarios—mirroring the slightly lower training accuracy.

PART 11: Save Models
<img width="938" height="878" alt="image" src="https://github.com/user-attachments/assets/4b2c3d43-b604-4d31-9128-35b657b25a6a" />



PART 12: Performance Comparison Table
<img width="1010" height="310" alt="image" src="https://github.com/user-attachments/assets/7a02eab2-6f65-4477-a78d-b2565fbd3248" />








