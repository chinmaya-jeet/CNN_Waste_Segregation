## **Objective**

The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Provide general information about your project here.
- What is the background of your project?
- What is the business problem that your project is trying to solve?
- What is the dataset that is being used?

## General Information
The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

## Conclusions
**Model Training approach and Results**
The data analysis was conducted with a training and valdation split of 80:20

->Overall Analysis
The training accuracy was ~53% which is not so good and there is room to improve.
Test loss of ~1.32 46 needs improvement, lower test loss means better performance.
The weighted F1-score (0.51) suggests performance is skewed toward more frequent classes.

-> Analysis of Classification Report
For class reference [ 0 = metal, 1 = plastic, 2 = cardboard, 3 = other, 4 = glass, 5 = food_waste, 6 = paper]

Class 6 (paper) performs the best overall: high precision (0.69) and decent recall (0.75), leading to the highest F1-score (0.69).
Class 1 (plastic) has highest recall (0.86), but low precision (0.38), meaning it often misclassifies other classes as 1.
Classes 4 and 5 (glass and food_waste)Moderate precision and low recall, indicating misclassification issues.
Class 2 (Card board) has high precision but low recall, indicating missed detections.

-> Analysis of Confusion Matrix
Class 0 - Mostly predicted as class 1, showing poor differentiation.
Class 1 - Mostly predicted correctly with very few wrong ones.
Class 2 - Moderate and major wrongly predicted as class 6.
Class 3 - 86% predicted correctly but most of wrong predictions creeping into class 1 and 6.
Class 4 - Moderate 54%, rest majorly going to 1 and 6.
Class 5 - Majorly wrong predcitions going to 1,3 and 6.
Class 6 - Highest correct prediction of 257 but still needs improvement.

**Insights from analysis**
No correct prediction in class 0 could be due to fewer examples, class imbalance.
Higher prediction in class 1 as per confusion matrix could be due to high recall and low precision.
Heavy confusion in classes 3 -> 6, Class 2 ↔-> 6, Class 5 -> 3
Model Complexity: The current model may be underfitting or overfitting
Recommendations
To handle class imbalance, Use class weights or oversample minority classes (e.g. Class 0).Consider SMOTE or RandomOverSampler.
Enhance feature extraction by using pretrained models like ResNet, MobileNet.
Investigate misclassified examples to understand if certain classes are visually similar or ambiguous.<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
# numpy version: 1.26.4
# pandas version: 2.2.2
# seaborn version: 0.13.2
# matplotlib version: 3.10.0
# PIL version: 11.1.0
# tensorflow version: 2.18.0
# keras version: 3.8.0
# sklearn version: 1.6.1


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This is an assignment from upgrad.

## Contact
Created by [@chinmayajeet] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->