
# **Lifestyle-Based Cervical Cancer Risk Prediction and Population Burden Analysis in West Africa**

## **Objective**
This project aims to analyse lifestyle-related risk factors and predict cervical cancer risk using machine learning models, while also examining the population burden of the disease across West African countries.



## **Dataset Description**
Two main datasets were used:

* **Individual-level dataset:**
  Contains demographic, behavioural, and clinical variables associated with cervical cancer risk (e.g., age, smoking habits, sexual history, contraceptive use, and STD history). The target variable is biopsy-confirmed cervical cancer.

* **Population-level dataset (GBD):**
  Includes incidence and prevalence data across West African countries, enabling regional trend and burden analysis.



## **Models Used**
The following machine learning models were implemented and compared:

* Logistic Regression (baseline model)
* Random Forest (ensemble learning)
* XGBoost (gradient boosting with hyperparameter tuning)

To address class imbalance, **random oversampling** and **threshold tuning** were applied, with a focus on improving recall for positive cancer cases.



## **Key Results**
* The dataset exhibited **severe class imbalance** (very few positive cancer cases).

* **Accuracy was not a reliable metric**, as models could perform well while failing to detect positive cases.
* After applying oversampling and threshold tuning:

  * **Logistic Regression (Oversampled):**
    * Accuracy: ~0.78
    * Recall: ~0.18

  * **XGBoost (Tuned + Threshold = 0.05):**
    * Accuracy: ~0.76
    * Recall: ~0.55

  * **Random Forest (Tuned + Threshold):**
    * Accuracy: ~0.61
    * **Highest Recall: ~0.82**

* **Best model for detection:** Random Forest (highest recall)
* **Best balanced performance:** XGBoost
These results highlight the trade-off between accuracy and recall in imbalanced medical datasets.



## **Key Insights**
* Clinical screening variables showed stronger predictive power than lifestyle factors.
* Lifestyle variables were generally **right-skewed**, indicating lower exposure levels for most individuals.
* Correlation analysis helped identify the most relevant features for prediction.
* Threshold tuning significantly improved the model’s ability to detect positive cases.



## **Population Burden Analysis (West Africa)**
* Cervical cancer remains a significant and persistent public health issue in West Africa.
* Incidence and prevalence trends show regional variation across countries and age groups.
* Higher burden is observed in reproductive and older age groups, highlighting the need for targeted interventions.



## **Conclusion**
This study demonstrates that machine learning can support cervical cancer risk prediction, but performance is heavily influenced by class imbalance.

While ensemble models such as Random Forest and XGBoost improve detection, recall remains the most critical metric in this context.

Improving early detection will require:
* Better data quality and representation
* Enhanced screening programs
* Continued optimisation of predictive models


## **Future Work**
* Explore advanced imbalance techniques (e.g., SMOTE, cost-sensitive learning)
* Incorporate more diverse and higher-quality datasets
* Deploy models in real-world screening support systems


