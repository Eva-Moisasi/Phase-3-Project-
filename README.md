
# Tanzanian Water Wells Classification
### Business Problem
Tanzania, is a developing country, struggles with providing clean water to its population of over 57,000,000. There are many water points already established in the country, but some are in need of repair while others have failed altogether.

As a data scientist working for an NGO, I am required to build a classifier to accurately predict the condition of water wells in Tanzania, with the aim of improving access to clean water for the country's growing population. The classifier will be used on locating wells in need of repair and finding patterns in non-functional wells to inform repair of wells and construction of new wells. The information used to make these predictions includes factors such as the type of pump and the installation date. The ultimate goal is to improve the maintenance operations of water pumps and ensure the availability of clean potable water for communities by predicting the functional status of water pumps.

### Data & Methodology
The data for this project was sourced from Taarifa and the Tanzanian Ministry of Water and includes variables such as type of pump, installation date, and management information.Data regarding Tanzania water wells was given in three separate files. Our primary dataset contains roughly 59,400 rows and 40 columns.The description of the column names can be found in the jupyter notebook.

### Water well status
Functional - supplies adequate water to the population

Functional needs repair - has less than 3 months of interruption in service.

Nonfunctional  - has more than 3 months of interruption


![download (3)](https://user-images.githubusercontent.com/113707140/217998615-29b81921-0846-464b-b17c-bb86c42f1e59.png)

In order for the classification models to correctly predict the target, i change the labels from strings to integers.

'functional' : 0, 

'non functional' : 1, 

'functional needs repair' : 2

## Models
Some of the models that i used were: Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbor, XGBoost Classifier. 

Metrics used: Accuracy, Precision, Recall, and F1 Score. These are performance metrics used to evaluate the accuracy of the classification models. They measure different aspects of the model's performance, such as the proportion of correct predictions, the proportion of correct positive predictions, and the balance between precision and recall.


![Screenshot (5)](https://user-images.githubusercontent.com/113707140/218021196-87bf1e21-d238-45ba-9340-8456e9556f88.png)



![download (4)](https://user-images.githubusercontent.com/113707140/218000368-613373e5-bbd9-4840-adb6-c5ccb348e590.png)

## Final Model
The best performing model is XGBoost with waterpoint_type, quantity_seasonal and extraction_type having the most importance, we are able to best predict the functionality of water wells in Tanzania to 80% accuracy

![download (5)](https://user-images.githubusercontent.com/113707140/218001143-36127a0d-b112-4d91-ae6d-0323de9a033f.png)

![download (6)](https://user-images.githubusercontent.com/113707140/218001204-28bbaebf-4408-474e-8a10-564d3c2eea98.png)


## Conclusions / Next Steps
Based on the results, the XGBoost model has shown better performance compared to other models with an accuracy of 0.79 and a balanced precision, recall, and F1 score. The confusion matrix also shows that the XGBoost model has correctly classified more observations compared to the other models.

The model had the best performance at predicting functional wells, but struggled with accurately predicting those that were functional but in need of repairs. Meanwhile, its results for non-functional wells were adequate.

#### To improve the model's predictions, the following steps are recommended:

Feature engineering by creating new features from existing ones to help the model better understand the relationship between input and output variables. This can lead to improved accuracy.

Hyperparameter tuning by adjusting the parameters of the model to optimize its performance.

We can also use Cross-validation to evaluate the performance of machine learning models. It helps to avoid overfitting and can lead to improved accuracy.

Ensemble methods can also be used to combine the predictions of multiple models to produce a more accurate result.

#### Further Analysis:
I would like to examine the following relationships in the data set:

* Does water quality contribute to the likelihood of a well failing/needing repair?
* How is the status of a well associated with the population using the well?
* is there a relationship between failure/repair and the type of pump?
* Does the age of the well indicate liklihood of needed repair or failure?


