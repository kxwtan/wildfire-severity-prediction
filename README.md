# wildfire-severity-prediction

These notebooks try to understand the factors that exacerbate wildfires (sizes). The dataset being used is provided by the [Government of Alberta](https://open.alberta.ca/dataset/a221e7a0-4f46-4be7-9c5a-e29de9a3447e/resource/1b635b8b-a937-4be4-857e-8aeef77365d2/download/af-historic-wildfires-2006-2018-data-dictionary.pdf) which gives data of over 20000 wildfires from 2006 to 2021, each with 50 describing features like location, wind, humidity, temperature, etc. 

The `eda.ipynb` notebook goes over the data and visualizes it to provide a better understanding of how the features relate to determining the size and severity of the wildfire. 

The `models.ipynb` file creates a data processing pipeline using scikit-learn where it one-hot encodes various categorical columns, normalizes numerical values, and performs feature engineering to better extract information from the features. At the end, it uses **Random Forest**, **XGBoost**, **Decision Trees** (Balanced or balanced with bagging), **Support Vector Machines**, **K-Nearest Neighbors**. GridsearchCV is also used to perform cross validation, determining the best hyperparameters to use for each model.

The best of the models (XGBoost) was able to achieve a testing accuracy of 92% with an F1 score of 0.71.
