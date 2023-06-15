# Melanoma-Detection

The objective of this project is to develop a CNN-based model capable of accurately detecting melanoma, a potentially fatal type of cancer. Melanoma accounts for 75% of skin cancer-related deaths, making early detection crucial. By creating a solution that can assess images and notify dermatologists about the presence of melanoma, a substantial amount of manual effort required for diagnosis can be reduced.

The dataset for this project can be downloaded from the following link: https://drive.google.com/drive/folders/1tepsbhSECXNbo1PEN_JaVR6P8wGIyqDx?usp=drive_link. 

It comprises 2357 images of malignant and benign oncological diseases obtained from the International Skin Imaging Collaboration (ISIC). The images are classified according to the ISIC categorization, with the exception of melanomas and moles, which have a slightly higher representation.

The dataset includes the following diseases: 
	actinic keratosis,
	basal cell carcinoma,
	dermatofibroma,
	melanoma,
	nevus,
	pigmented benign keratosis,
	seborrheic keratosis,
	squamous cell carcinoma,
	and vascular lesion.

The project pipeline involves several steps:

Data Reading/Data Understanding: The first step is to define the path for the train and test images.

Dataset Creation: Create a train and validation dataset from the train directory using a batch size of 32. It is important to resize the images to dimensions of 180x180.

Dataset Visualization: Develop code to visualize one instance of each of the nine classes present in the dataset.

Model Building & Training: Construct a CNN model capable of accurately detecting the nine classes in the dataset. During model construction, rescale the images to normalize pixel values between 0 and 1. Select an appropriate optimizer and loss function for training the model. Train the model for approximately 20 epochs. After model fitting, analyze for evidence of overfitting or underfitting.

Data Augmentation: Implement an appropriate data augmentation strategy to address underfitting or overfitting issues.

Model Building & Training with Augmented Data: Create a CNN model, similar to the previous step, capable of accurately detecting the nine classes. Rescale the images and choose an appropriate optimizer and loss function. Train the model for approximately 20 epochs. Evaluate the model's performance after training to determine if the earlier issues have been resolved.

Class Distribution: Analyze the current class distribution within the training dataset. Identify the class with the fewest number of samples and determine which classes dominate the dataset in terms of the proportionate number of samples.

Handling Class Imbalances: Address class imbalances in the training dataset using the Augmentor library.

Model Building & Training on Balanced Data: Develop a CNN model capable of accurately detecting the nine classes. Rescale the images, choose an appropriate optimizer and loss function, and train the model for approximately 30 epochs. Evaluate the model's performance after training to determine if the issues have been resolved.

Results:

Accuracy: 91%
Validation Accuracy: 81%
The model does not exhibit overfitting, and the augmentation technique has significantly increased the accuracy. Class rebalancing has proven beneficial in reducing overfitting and minimizing loss.
