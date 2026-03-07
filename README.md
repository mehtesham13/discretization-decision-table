## Impact of Discretization on DecisionTable Classifier Performance in WEKA 

This project explores how different data discretization techniques affect the predictive accuracy and interpretability of the **DecisionTable** rule-based classifier. Using the **Pima Indians Diabetes dataset**, we compare baseline performance against several pre-processing methods to determine the most effective approach for rule-based modeling.

##  Project Overview

The primary goal of this study was to evaluate if transforming continuous attributes into categorical "bins" (discretization) improves the performance of the DecisionTable algorithm in WEKA.

##  Experimental Setup

* **Tools Used:** WEKA Data Mining Software.


* **Dataset:** `diabetes.arff` (Pima Indians Diabetes).


* **Classifier:** DecisionTable.


* **Evaluation Method:** 10-fold Cross-validation.



Discretization Methods Tested 

1. **Original Dataset:** No discretization (baseline).


2. **Unsupervised Discretization:** Binning without considering class labels.


3. **Supervised Discretization:** Uses class information to find optimal cut points.


4. **PKIDiscretize:** Proportional k-Interval discretization.



##  Results & Accuracy Comparison

| Dataset Version | Correctly Classified | Incorrectly Classified | Accuracy (%) |
| :--- | :---: | :---: | :---: |
| Original Dataset | 547 | 221 | 71.22% |
| Unsupervised Discretize | 556 | 212 | 72.39% |
| Supervised Discretize | 585 | 183 | 76.17% |
| PKIDiscretize | 568 | 200 | 73.95% |

 Key Findings 

* **Supervised Discretization** yielded the highest accuracy (76.17%), as it maximizes class separation by using label-informed cut points.


* **Rule-based models** like DecisionTable generally perform better on categorical data than raw continuous attributes.


* **Class-informed methods** are significantly more effective for enhancing both predictive performance and model interpretability.



👥 Contributors 

* **Muhammad Ehtesham** 


* Arifa Farhath 


* Bhavesh 


* Shivam 


* Nitish 


* Yogesh 



---
