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
 
"Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.

For the analysis of chest x-ray images, all chest radiographs were initially screened for quality control by removing all low quality or unreadable scans. The diagnoses for the images were then graded by two expert physicians before being cleared for training the AI system. In order to account for any grading errors, the evaluation set was also checked by a third expert."

Sources: [original image source](https://data.mendeley.com/datasets/rscbjbr9sj/2), [data download source/Kaggle competition](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia)

### Classifier

Full analysis: [Colab Notebook](/project_4_notebook.ipynb)

TODO: Target metric, results, conclusions/considerations for best model

TODO: 3 Visuals nexplaining model

<img alt="confusion" src="/images/class_report.png" width="600"/>

<img alt="confusion" src="/images/confusion.png" width="400"/>

<img alt="ROC/AUC" src="/images/ROC.png" width="400"/>

### Reccomendations

    - Continue collecting labeled images to progressively train the model.
    - Store image data at 128 x 128 to conserve storage memory (this is up to a 10% reduction in original image size).
    - 

#### Future Work

    - Collect more images or continue data augmentation to increase training set from ~5,000 images.
    - Try transfer learning - use an established x-ray classifier and build model on top of that.
    - Progressively resize the model input image size to find the smallest possible input size without sacrificing performance.

#### Thank you for viewing my project!

Please review the full analysis in the [Colab Notebook](/project_4_notebook.ipynb) or view my presentation [slideshow](/Mod0_presentation.pdf) or [video]().

