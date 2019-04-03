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
For privacy reasons the API keys are removed you need to get your own from Twitter and Telegram! 
### Pre-trained model
The pre-trained model was saved using [Pickle](https://machinelearningmastery.com/save-load-machine-learning-models-python-scikit-learn/) and is available in this repository under the filename "model.sav". It can be easily imported using the following code:
```
import pickle
filename = 'model.sav'
model = pickle.load(open(filename, 'rb'))
```
## Requirements
- Jypiter Notebook
- Python 3
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

training - a training set consisting of 2900 tweets.

extended_training_set - Contains the training set. This was used to train the model it consist of 7900 tweets.

expl_18k - A big set of 18k tweets not contained in the above sets.

all - A combined set of all of the above.
## Setup and Run
Install the reguired packages and set up a Jupyter notebook environment.
### Training a new model
1. Import all the reguired packages
2. Select which training set you want to use
3. Train your model
4. Save the model using pickle.
After training you can perform an evaluation on another set.
The code for live evaluation is provided in the notebook, you
can start the stream and see how your model performs live.
### Launching your own Bot
1. Get your API keys from twitter for accessing the Stream.
2. Create your own Bot using [BotFather](https://core.telegram.org/bots#6-botfather)
3. Get your token from telegram and set it up
```
 updater = Updater(token='')
 ```
4. Set up a collection in [MongoDB](https://docs.mongodb.com/manual/reference/method/db.createCollection/)
5. Make sure all cells in the notebook are inserted before starting
6. Start the Bot
```
updater.start_polling()
```
Now your bot is running!
To talk with it open the Telegram messenger
and enter the command "\start".

## References
- [Keras](https://keras.io/)
- [Telegram Bots](https://core.telegram.org/bots)
- [Twitter Access Tokens](https://developer.twitter.com/en/docs/basics/authentication/guides/access-tokens.html)
- [MongoDB](https://www.mongodb.com/)
