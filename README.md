# Melanoma Detection Using CNN

> A project to build a CNN-based model that can accurately detect melanoma from skin images.

## Table of Contents
* [General Information](#general-information)
* [Dataset Details](#dataset-details)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

## General Information
- **Project Background:**  
  Melanoma is a deadly type of skin cancer responsible for 75% of skin cancer deaths. Early detection significantly increases survival rates. This project aims to build a solution to evaluate images and alert dermatologists about potential melanoma cases, reducing the manual effort required for diagnosis.
  
- **Business Problem:**  
  Develop a CNN model capable of identifying melanoma with high accuracy, assisting dermatologists in early diagnosis and treatment planning.

## Dataset Details
- The dataset comprises **2357 images** of various malignant and benign skin conditions.
- Source: **International Skin Imaging Collaboration (ISIC)**.  
- The dataset includes the following diseases:
  - Actinic keratosis
  - Basal cell carcinoma
  - Dermatofibroma
  - Melanoma
  - Nevus
  - Pigmented benign keratosis
  - Seborrheic keratosis
  - Squamous cell carcinoma
  - Vascular lesion

## Conclusions
- **Key Insights:**  
  1. The training dataset shows significant class imbalance, with Pigmented benign keratosis (462) and Melanoma (438) dominating, while Seborrheic keratosis (77) and Dermatofibroma (95) are underrepresented. 
  2. For Base Model: `Overfitting:` As training continues beyond that optimal point, the validation metrics stop improving and start to worsen, while training metrics continue to improve. This pattern is a sign of overfitting.
`Diverging Loss:` Training Loss consistently decreases, while the Validation Loss does not follow the same trend.  
  3. For Model (With Data Augmentation): `No Overfitting / Improvement compared to previous Model` : `validation accuracy` often matches or even tops the `training accuracy`, and both stay fairly close. This indicates that it’s not heavily overfitting, unlike the previous initial base model, which clearly did. `Low Accuracy`: Still, the model isn’t achieving very high accuracy yet, and performance remains somewhat inconsistent. More tuning, epochs, or architectural changes may help. Compared to the base model, where training accuracy soared while validation stagnated or worsened, the data augmentation has helped bring these metrics into closer alignment. Though the absolute accuracy hasn’t skyrocketed, the improved balance suggests better generalization and less risk of overfitting.  
  4. Final Model (After Augementor): With this third model using Augmentor, the training and validation accuracy lines remain close, and both show steady improvement. The validation accuracy doesn’t lag far behind the training accuracy, suggesting less overfitting than we saw with the base model. Compared to Model 1 and the initial augmented model, this approach shows more balanced performance. The loss curves also indicate improvement, though some fluctuations remain. It’s not a perfect solution, as accuracy could still improve and the curves could smooth out further, but overall, the **use of Augmentor appears to have helped reduce overfitting and move toward more generalizable learning** .

## Technologies Used
- Python version: 3.11.10
- TensorFlow version: 2.17.0
- Matplotlib version: 3.9.2
- NumPy version: 1.26.4
- Pandas version: 2.2.3
- Augmentor version: 0.2.12

## Acknowledgements
- **Credit:**  
  This project is part of the **Executive PG Programme in AI & ML** from **IIIT, Bangalore** & **upGrad**.
  
- **References:**  
  - Data sourced from **ISIC**.  
  - Inspired by lectures from IIITB and upGrad professors.  

## Contact
Created by [@RahulMukeshSingh] - feel free to contact for further information!