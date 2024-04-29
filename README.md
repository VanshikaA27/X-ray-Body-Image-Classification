# X-ray-Body-Image-Classification

Classifying a body part from an x-ray image might seem silly, but having it automated can be a key for all the world around deep learning in medical imaging. In many hospitals, when a physician orders multiple imaging exams one accession number is created for each body part (eg. knee, ankle, and leg), but the registration for the correspondent images are often incorrect within each accession number.
The algorithm should be able to automate the identification of the body part in the image, making it possible to create more datasets and deploy pipelines.

## Challenges in Traditional Classification Methods

Subjectivity: Manual classification is prone to subjective interpretation, leading to inconsistencies in diagnoses.
Human Error: Manual classification is susceptible to human error, especially when dealing with large datasets.
Limited Scalability:  Manual classification becomes impractical with the increasing volume of medical imaging data.
Time-Consuming: Manual classification is time-consuming, causing delays in diagnosis and treatment.

## Benefits of Automated Classification Systems

Efficiency: Automated systems can process large volumes of X-ray images in a short time, improving workflow efficiency.
Consistency: Automated systems provide consistent and standardized analysis, reducing variability between different radiologists.
Scalability: Automated systems are scalable and can handle increasing amounts of data without compromising accuracy.
Accuracy: Machine learning algorithms can learn from vast datasets, leading to highly accurate classification results.

## Data Collection and Preprocessing
Kaggle Dataset: The X-ray image dataset used in this project is sourced from Kaggle. It is available in the "X-ray Body Images in PNG (Unifesp)" dataset.
Link: X-ray Body Images in PNG (Unifesp)
Description: This dataset contains X-ray images in PNG format obtained from the Universidade Federal de São Paulo (UNIFESP) for a competition.
Multi-class Classification: The dataset includes X-ray images labeled with multiple classes, each representing a specific anatomical region or condition.
Examples of classes: "Abdomen," "Ankle," "Cervical Spine," "Thoracic Spine," "Pelvis," etc.
Label Format: Each image may have one or more labels associated with it, indicating the presence of abnormalities or anatomical structures.

## Data Preprocessing Techniques

Normalization: The pixel values of the images are normalized to a range between 0 and 1 to ensure consistency in pixel intensity.

Resizing: Images are resized to a standard size of 224x224 pixels to maintain uniformity for model input.
Grayscale Conversion: Images are converted to grayscale to simplify processing, as color information is not required for classification.

Noise Reduction: Techniques like Gaussian blurring or median filtering may be applied to reduce noise and improve image quality.

      ### Data Augmentation

Purpose: Data augmentation is applied to increase the diversity of the dataset and improve model generalization.

Techniques Used:  Common augmentation techniques include rotation, flipping, shifting, zooming, and brightness adjustment.

Sample Augmented Images: Examples of images before and after augmentation are shown to illustrate the changes made to the dataset.

## Model Architecture

Convolutional Neural Network (CNN): Utilized for image classification tasks, effectively capturing spatial hierarchies in images.
Transfer Learning: Utilizes pre-trained models like Xception or ResNet, leveraging learned feature representations for our task.
Custom Layers: Added on top of the pre-trained model for fine-tuning or task adaptation.

Training Process:
Initialize model and load pre-trained weights.
Compile with optimizer, loss function, and metrics.
Train on training data, monitoring performance on validation set.
Adjust hyperparameters based on validation performance.
Evaluate final model on testing set for performance and generalization.

## Model Evaluation
Calculates evaluation metrics such as accuracy and F1 score.
Generates confusion matrix to visualize model's performance.
Cross-Validation:
Utilizes K-Fold cross-validation to assess model's robustness.
Evaluates performance by averaging across folds.
Performance Comparison:
Compares performance with baseline models.
May include visualizations like ROC curves or precision-recall curves.
Test Accuracy:
Prints the test accuracy score.
Displays the confusion matrix for further analysis.



