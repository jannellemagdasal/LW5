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

# GUIDE QUESTIONS (FINAL REFLECTION)
A. Model Performance
1. MobileNetV2 achieved the highest test accuracy (0.9818); it likely generalized best due to efficient architecture and training.
2. EfficientNetB0 had the lowest performance (test accuracy 0.0938); likely due to poor convergence, possible data or configuration issues.
3. Loss values were lowest for the best models (MobileNetV2: 0.1199); poorly performing models had much higher loss.
B. Evaluation Metrics
4. Accuracy alone ignores class imbalance and does not reveal performance differences across classes.
5. DenseNet121 and MobileNetV2 both had the best F1-score (0.97), indicating strong balance of precision and recall.
6. Precision and recall were very high and nearly identical for the top models, but dropped in weaker models.
C. Confusion Matrix Analysis
7. Classes with lower precision/recall (e.g., from baseline/Teachable Machine) were likely misclassified frequently.
8. Misclassifications were concentrated in classes with similar features; best models showed few such errors.
D. ROC and AUC
9. DenseNet121, MobileNetV2, and EfficientNetB0 had the highest (≈0.99) AUC scores.
10 High AUC reflects excellent discrimination between classes, even under varying thresholds.
E. Explainability (Grad-CAM)
11. Grad-CAM showed models like DenseNet121 focused on correct, relevant image regions.
12. Yes, the best models focused on the features distinguishing each class.
13. DenseNet121 produced the most meaningful (focused) heatmaps.
F. Model Comparison & Improvement
14. MobileNetV2 is recommended for deployment due to highest test accuracy and stability.
15. Improvements could include more data, regularization, fine-tuning, or data augmentation.
G. Real-World Application
16. The model can automate species or object identification (e.g., plant recognition) in real time.
17. Risks include misdiagnosis or incorrect identification leading to user error or harm.
18. The system can be integrated into a mobile/web app using ONNX/TensorFlow Lite or REST APIs for real-time predictions.


## notebook links: https://drive.google.com/drive/folders/1q-5hsxk4evcmVyZQAkaKGTnmnAnNHxMg?usp=sharing







