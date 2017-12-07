
# Restaurant-Search-Bot
Simple restaurant search bot using natural language understanding(NLU) but we can customize and train the model according to usecase.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

## Prerequisites
1. pip install -U spacy
2. python -m spacy download en
3. pip install -U scikit-learn scipy sklearn-crfsuite


### Installing
Repository already contains compiled rasa_library and dont install directly using pip otherwise it will result in errors
To install rasa_nlu
1.cd rasa_nlu
2.pip install -r requirements.txt
3.python setup.py install (open cmd console in admin mode)
if it gets stuck close the cmd window

## Running the tests
1. Train the model:
python -m rasa_nlu.train -c config_spacy.json

--models get automatically generated in project/default (specified in config file)

2. Run the Server:
python -m rasa_nlu.server -c config_spacy.json

3. check the Status:
http://localhost:5000/status

4. Run the Test (on chrome browser):
http://localhost:5000/parse?q=show%20me%20chinese%20restaurants


NOTE: 
If there is JsonDecodeError then fire this command:
iconv -c -f utf-8 -t ASCII demo.json > demoEncoded.json


## Built With
RASA_NLU

## Deployment:
Integrate with Node_red to create API and connecting the generated api to slack or twilio for dummy frontend framework (will commit soon)
