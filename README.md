
# Tanzanian Water Wells Classification
### Business Problem
Tanzania, is a developing country, struggles with providing clean water to its population of over 57,000,000. There are many water points already established in the country, but some are in need of repair while others have failed altogether.

The stakeholde for this project is an NGO based in Tanzania, The goal for this project is to develop a classifier to accurately predict the condition of water wells in Tanzania, with the aim of improving access to clean water for the country's growing population. The classifier will be used to focused on locating wells in need of repair and find patterns in non-functional wells to inform the construction of new wells. The information used to make these predictions includes factors such as the type of pump and the installation date. The ultimate goal is to improve the maintenance operations of water pumps and ensure the availability of clean potable water for communities by predicting the functional status of water pumps.

### Data & Methodology
The data for this project was sourced from Taarifa and the Tanzanian Ministry of Water and includes variables such as type of pump, installation date, and management information.Data regarding Tanzania water wells was given in three separate files. Our primary dataset contains roughly 59,400 rows and 40 columns.The description of the column names can be found in the jupyter notebook.

### Water well status
Functional - supplies adequate water to the population

Functional needs repair - has less than 3 months of interruption in service.

Nonfunctional  - has more than 3 months of interruption


![download (3)](https://user-images.githubusercontent.com/113707140/217998615-29b81921-0846-464b-b17c-bb86c42f1e59.png)

## Models
Some of the models that i used were: Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbor, XGBoost Classifier. 

Metrics used: Accuracy, Precision, Recall, and F1 Score. These are performance metrics used to evaluate the accuracy of the classification models. They measure different aspects of the model's performance, such as the proportion of correct predictions, the proportion of correct positive predictions, and the balance between precision and recall.


![Screenshot (3)](https://user-images.githubusercontent.com/113707140/217999702-3510bd83-b1b5-4542-9136-b72610a45e28.png)

![download (4)](https://user-images.githubusercontent.com/113707140/218000368-613373e5-bbd9-4840-adb6-c5ccb348e590.png)

## Final Model
The best performing model is XGBoost with waterpoint_type, quantity_seasonal and extraction_type having the most importance, we are able to best predict the functionality of water wells in Tanzania to 80% accuracy

![download (5)](https://user-images.githubusercontent.com/113707140/218001143-36127a0d-b112-4d91-ae6d-0323de9a033f.png)

![download (6)](https://user-images.githubusercontent.com/113707140/218001204-28bbaebf-4408-474e-8a10-564d3c2eea98.png)



