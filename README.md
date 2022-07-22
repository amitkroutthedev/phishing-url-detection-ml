
# phishing-url-detection-ml

Detection of harmful phished website with the help of ML algorithms.


## Documentation

Phishing is a kind of Cybercrime trying to obtain important or confidential information from users which is usually carried out by creating
a counterfeit website that mimics a legitimate website.
The most common approach is to set up a spoofing web page that imitates a legitimate website. Phishing websites are a serious problem 
against individuals and corporations. 

***DATASET AND FEATURE EXTRACTION***

1.  Dataset
Two types of URL sources are collected for conducting the classification task
- Source I (Phishing URLs)
- Source II (Legitimate URLs)
2. Feature Extraction
Feature extraction refers to the process of transforming raw data into numerical features that can be processed while preserving the 
information in the original data set. It yields better results than applying machine learning directly to the raw data. 
In these datasets, we applied these important features that have been effective in predicting phishing website. 
The values assigned for all feature is 1(phishing), 0(legitimate) and 2(suspicious).
The extracted features are categorized into
- Address Bar based Features
- Domain based Features
- HTML and JavaScript based Features

***MODEL TRAINING AND TESTING***

The features are extracted from both the datasets and stored in different file and both extracted datasets are combined together so to 
train entire dataset consisting of 2000URLs (1000 phishing URLs and 1000 legitimate URLs).
The entire dataset is split into 8:2 ratio from training and testing models. From the above dataset, it is clear that this is a 
supervised machine learning task.
The following models are considered to train the dataset:
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost Classifier
- 	Support Vector Machines
- 	K Nearest Neighbors Classifier
- 	Logistic Regression
- 	Ada Boost
***MODEL EVALUATION AND COMPARISION***

For evaluating phishing classification performance, we use Precision, Recall, F1 Score, Accuracy.

|       ML Model      | Precision | Recall | F1 Score | Accuracy |
|:-------------------:|-----------|--------|----------|----------|
| Decision Tree       | 0.962     | 0.990  | 0.976    | 0.975    |
| Random Forest       | 0.941     | 1.000  | 0.969    | 0.968    |
| XG Boost            | 0.976     | 0.995  | 0.986    | 0.985    |
| SVM                 | 0.961     | 0.966  | 0.964    | 0.962    |
| K Nearest Neighbour | 0.961     | 0.966  | 0.964    | 0.962    |
| Logistic Regression | 0.961     | 0.966  | 0.964    | 0.962    |
| Ada Boost           | 0.961     | 0.966  | 0.964    | 0.962    |

It is clear that the XGBoost Classifier works well with this dataset.
## Tech Stack

**Language**: Python

**Editor**:Google Collab

## Run Locally

Open the file in Google Collab and make an copy in Drive and run the program.

***or***

Create a virtual environment

```bash
  pip install virtualenv 
  virtualenv environment_name
  source environment_name/bin/activate
```

Clone the project in the same folder

```bash
  git clone https://github.com/amitkroutthedev/phishing-url-detection-ml.git
```
Go to the project directory

```bash
  cd phishing-url-detection-ml
```
To check if the virtual environment working or not?

```bash
  pip list
```

To install libraries in a Virtual Environment

```bash
  pip freeze > requirements.txt
```
Then open the file in the jupyter notebook locally and run the program.

To deactivate virtual environment

```bash
  (virtualenv_name)$ deactivate
```
## Screenshots


![image](https://user-images.githubusercontent.com/48612930/180358650-c098e005-817e-4503-a3f6-35d8d11d1049.png)

*Feature Distribution over 2000 urls*

![image](https://user-images.githubusercontent.com/48612930/180358274-dcdd8a7a-7952-4ad5-af5f-0cf3c1a2caee.png)

*Feature Importance in XG Boost*
## Roadmap

- Using the model to build a web applications

- Using more nos. of URLs


## Authors

- [@amitkroutthedev](https://github.com/amitkroutthedev)


## Contributing

Contributions are always welcome!
