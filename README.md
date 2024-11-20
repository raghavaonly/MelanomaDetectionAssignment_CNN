# MelanomaDetectionAssignment_CNN

Multiclass Classification Model Using a Custom Convolutional Neural Network
This project aims to build a CNN-based model for accurately detecting melanoma, a type of cancer that can be fatal if not diagnosed early. Melanoma is responsible for 75% of skin cancer-related deaths. A reliable model capable of evaluating medical images and assisting dermatologists in detecting melanoma could significantly reduce the manual effort required for diagnosis.

Background
In the 10-year period from 2008 to 2018, the annual incidence of melanoma increased by 53%, partly due to higher UV exposure. Despite being one of the most dangerous forms of skin cancer, early diagnosis dramatically improves survival rates.

The initial step in diagnosing a malignant lesion involves a dermatologist visually examining the suspicious area. Accurate diagnosis is challenging due to similarities between some lesion types and depends significantly on the physician's expertise. Dermatologists' diagnostic accuracy for melanoma ranges from 65% to 80% without additional technical support.

To enhance accuracy, dermatoscopic imaging is used, involving high-resolution cameras with controlled lighting and filters to reduce skin reflection and reveal deeper layers. This technology improves diagnostic accuracy by up to 49%. Combining visual examination with dermatoscopic imaging achieves an overall accuracy of 75% to 84% for melanoma detection by dermatologists.

Why Convolutional Neural Networks (CNNs)?
CNNs are a specialized type of neural network proven effective in tasks like image recognition and classification. They have demonstrated superior performance in identifying objects, faces, and other visual elements, surpassing human capabilities in many cases. These networks are widely used in applications such as robotics and autonomous vehicles.

CNNs operate as supervised learning models, requiring labeled datasets for training. They comprise two main components:

Feature Extraction Layers: Hidden layers designed to extract features from input data.
Fully Connected Layers: Perform the classification task based on extracted features.
Unlike traditional neural networks, CNNs limit connections between neurons to local regions, making them more efficient for image-related tasks. Additional pooling layers help summarize local outputs, leading to translation-invariant features, simpler training, and reduced model complexity.

Problem Statement
To develop a CNN-based model capable of accurately detecting melanoma by analyzing dermatoscopic images.

Objective
Build a multiclass classification model using TensorFlow.
Provide a solution that reduces the manual effort in melanoma diagnosis by assisting dermatologists with reliable image evaluations.
Dataset Overview
The dataset comprises 2,357 images representing malignant and benign skin conditions, sourced from the International Skin Imaging Collaboration (ISIC). The data includes several categories of skin lesions:

Actinic Keratosis
Basal Cell Carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented Benign Keratosis
Seborrheic Keratosis
Squamous Cell Carcinoma
Vascular Lesions
Most classes are balanced, except for melanomas and moles, which are slightly overrepresented.

Model Building Process
Data Preprocessing:

Path definition for train/test images.
Batch creation and image resizing.
Dataset splitting for training and validation.
Model Development:

Build a custom CNN model.
Compile with appropriate optimizer and loss functions.
Train the model while visualizing its performance.
Addressing Class Imbalance:

Use data augmentation and rebalancing techniques.
Introduce dropout layers to mitigate overfitting.
Findings
Initial model: 90.46% training accuracy, 52.35% validation accuracy.
With data augmentation: Improved validation accuracy to 57.49%.
Adding a dropout layer: Achieved 62.44% training accuracy, 57.49% validation accuracy.
Class rebalancing: Significantly improved validation accuracy to 82.33%.
Validation accuracy nearing training accuracy (~84%) indicates that the model effectively mitigated overfitting.

Technologies Used
TensorFlow: Version 2.14.0
Keras: Version 2.14.0
Pandas: Version 2.0.3
Augmentor: Version 0.2.12
NumPy: Version 1.24.3
Conclusion
Rebalancing classes and incorporating data augmentation improved overall model performance.
Although data augmentation sometimes reduced accuracy due to image variability, further training over additional epochs can address this issue.
With the current model, validation accuracy of ~84% demonstrates its reliability in assisting dermatologists with melanoma detection.
Acknowledgements
This project was inspired by UpGrad and is based on their learning modules. Further references can be provided upon request.
