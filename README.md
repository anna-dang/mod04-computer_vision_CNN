Flatiron Data Science Program

Module 4 Project - Neural Networks

December 15th, 2020

---

# *Computer Vision*

*X-Ray Image Classification*

 <img alt="xrays" src="/images/laser_eyes.gif" width="400"/>

---

### Overview

Objective: Build a model that can classify whether a given patient has pneumonia, given a chest x-ray image.

Repository Contents:

    - images : images for display through this analysis
    - project_4_notebook.ipynb : Google Colab notebook containing full analysis/modeling
    - README.md : project summary and contents
    - Mod04_presentation.pdf : presentation slides with comments


### Data

 <img alt="xrays" src="/images/xrays.png" width="800"/>
 
"Chest X-ray images (anterior-posterior) were provided from pediatric patients of Guangzhou Women and Children’s Medical Center, Guangzhou, China. The diagnoses for the images were then graded by two expert physicians before being cleared for training the AI system."

Sources: [original image source](https://data.mendeley.com/datasets/rscbjbr9sj/2), [data download source/Kaggle competition](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia)

### Classifier

Full analysis: [Colab Notebook](/project_4_notebook.ipynb)

For this project I wanted to optimize the model to arrive at as few fasle predictions as possible. False positives could be costly in resources for the provider and patient, or result in unnecessary treatment. False negatives could allow illness to be missed and treatment delayed. Thus I selected **accuracy** and the **AUC** (area under the ROC curve) as target metrics for a balanced model, for both penalize false predictions.

The final model was trained on images with the following preprocessing:
 
    - Images resized to 124 x 124 pixels with 3 RGB color channels
    - Pixel value standardized to 0 - 1 scale
    - To prepare the model to discern noise, four data augmentations were used: rotation, shifting, and zoom
    
The final model arcitecture was a convolutional neural network (CNN) with ************** layers.
    
Resulting in performances scores of:

    - Accuracy:
    - AUC:
    - Precision:
    - Recall:

<img alt="confusion" src="/images/class_report.png" width="600"/>

<img alt="confusion" src="/images/confusion.png" width="400"/>

<img alt="ROC/AUC" src="/images/ROC.png" width="400"/>

### Reccomendations

    - Continue collecting labeled images to progressively train the model.
    - Store image data at 128 x 128 to conserve storage memory (this is up to a 10% reduction in original image size).
    - Use the model to improve efficiency of Xray review.

#### Future Work

    - Collect more images or continue data augmentation to increase training set from ~5,000 images.
    - Try transfer learning - use an established x-ray classifier and build model on top of that.
    - Progressively resize the model input image size to find the smallest possible input size without sacrificing performance.

#### Thank you for viewing my project!

Please review the full analysis in the [Colab Notebook](/project_4_notebook.ipynb) or view my presentation [slideshow](/Mod0_presentation.pdf).

