# KerasTelegramBot
This repository holds the files accompanying the Master Thesis.
The application consists of multiple files and datasets.
Below im going to guide through the steps of setting up your own
or training your own model.
The environment used for developing the application is Jupyter notebook.
## Description
keras.ipynb - Contains the code that was used for training the model. You can use it to train your own model
or perform evaluations.
kerasBot.ipynb - The code for launching the bot. It uses a pretrained model but you can substitute your own. 
For privacy reasons the API keys are removed you need to get your own from twitter!
### Pre-trained model
The pre-trained model was saved using [Pickle](https://machinelearningmastery.com/save-load-machine-learning-models-python-scikit-learn/) and is available in this repository under the filename "model.sav". It can be easily imported using the following code:
```
import pickle
filename = 'model.sav'
model = pickle.load(open(filename, 'rb'))
```
## Requirements
- Keras(with tensorflow backend)
- tensorflow
- pandas
- numpy
- pickle
- pymongo
- twython
- telegram
## Datasets
The datasets used for training the model. The data needs to be provided in a CSV format.
The sets consist of labelled tweets. The first column contains the label "1" - true
and "0"- false. The second column contains the text of the tweet. These sets were 
not preprocesesed!
Before you use them for training you can use the preprocesing function or you can add your own.
training -
extended_training_set - 
expl_18k - 
all -
## Setup


## Run
## References
