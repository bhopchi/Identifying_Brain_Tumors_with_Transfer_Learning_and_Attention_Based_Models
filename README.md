# Identifying_Brain_Tumors_with_Transfer_Learning_and_Attention_Based_Models
This project utilizes pretrained CNNs with attention mechanisms for brain tumor classification, identifying glioma, meningioma, pituitary, and non-tumor cases. It applies label encoding, oversampling for balance, and evaluates model performance through metrics, achieving high accuracy in tumor detection.


The project focuses on brain tumor detection using deep learning, specifically leveraging pretrained convolutional neural networks (CNNs) integrated with attention mechanisms. It classifies MRI images into four categories: glioma, meningioma, pituitary tumor, and non-tumor, addressing the challenge of accurate and early diagnosis in medical imaging.

### Dataset Preparation and Preprocessing
The data used is structured with distinct categories for each tumor type and non-tumor images. Preprocessing begins with data organization into a labeled dataframe, followed by analysis of class distribution. To counter class imbalance, the project uses oversampling techniques, ensuring each class is adequately represented. Images are resized to a standard input shape (224x224 pixels) and normalized for consistency across the models.

### Model Architecture and Transfer Learning
The project utilizes several pretrained models, including VGG16, VGG19, MobileNet, Xception, and InceptionV3, each configured with an attention mechanism. The architecture freezes pretrained layers to retain learned weights and appends additional layers tailored to this specific classification task. The MultiHeadAttention layer refines feature extraction by focusing on relevant image regions, enhancing model performance. Gaussian noise and dropout layers are also added to improve generalizability.

### Training and Evaluation
Training is conducted with an 80-20 split for the training and validation sets, employing data augmentation through TensorFlow’s `ImageDataGenerator`. Performance is optimized by using sparse categorical cross-entropy as the loss function and monitoring validation loss for early stopping. 

Each model’s performance is evaluated on metrics such as accuracy, precision, recall, and F1-score. These metrics offer insights into model robustness and reliability, essential for clinical applications. The MobileNet model, in particular, achieves high accuracy and balanced performance across categories.

### Results and Analysis
The results are visualized through loss/accuracy plots and confusion matrices. The models display strong classification capabilities, with MobileNet outperforming others in most metrics. This suggests its suitability for computationally efficient and accurate diagnosis, highlighting the potential of attention-augmented transfer learning in medical image analysis.

### Conclusion
This project demonstrates the effectiveness of combining pretrained CNNs and attention mechanisms for brain tumor classification, with significant implications for real-time diagnostics. The approach balances accuracy and computational efficiency, paving the way for AI integration in medical diagnostic workflows.
