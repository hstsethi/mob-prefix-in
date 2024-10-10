Phone numbers in India are a set of unique 10 digit numbers. Out of which, first 4 are network operator/circle code. These prefixes range from 6xxx - 9xxx. Last six are random. This is a dataset, charts, model of first four numbers with their respective state, operator name.

Note: Starting from commit hash `9de66f3f74e465c973f5e2a47241c7627ca94c32`, the dataset is refractored to contain only 3 columns: series, operator, circle. This makes it easier to use/read and eliminates duplicate columns name.

Note: This dataset is provided "as-is" without any warranty of any kind. While I have personally fixed many errors, I still can't guarantee that this dataset is accurate. Use at your own risk.


## Use Cases

- Privacy friendly alternative to reverse phone number lookup services like Truecaller

See the section below for pretrained models, training and inference script.

- Model training

- Spam Detection

## Using Machine Learning To Predict Operator Names

A Python script named, `predict-operator.py` is provided with this project. It works by checking if the operator to predict is in dataset. If not, it will try using the appropriate model for predicting the operator. There are 4 specialized KNN models trained on 4 different set of prefixes using KNN. If appropriate model is not found, it will train model and save the resulting model using Joblib.

To run it simply run: `python predict-operator.py`. 
 
## Sources

Majority of this data is sourced from Wikipedia and Telecom Regulatory Authority of India(TRAI). Rest of it was collected from various sources including web scrapping, personal research and other publicly available resources.
