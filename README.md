# ThaparBot

# LIVE DEMO AVAILABLE HERE:
https://thapar-bot2.herokuapp.com/

# DISCRIPTION:
In this project, I have tried to make a chat assisstant for our college. This system can be embedded to the college website and can help in resolving people's general queries.

# WORKING

ML model has been initially trained in train.ipynb file. In this, i have preprocessed the data(textual data in form of intents). Once it is preprocessed, i have divided it into training and testing sets. After that I have made a Neural Netwrok Model to train the training data.The trained model has been saved and used furthur. Then I have used Pickle to get the response for new intents.
#neural networds model
model = Sequential()
model.add(Dense(128, input_shape=(len(train_x[0]),), activation='relu'))
model.add(Dropout(0.5))
model.add(Dense(64, activation='relu'))
model.add(Dropout(0.5))
model.add(Dense(len(train_y[0]), activation='softmax'))
Compiling model. SGD with Nesterov accelerated gradient gives good results for this model
sgd = SGD(lr=0.01, decay=1e-6, momentum=0.9, nesterov=True)
model.compile(loss='categorical_crossentropy', optimizer=sgd, metrics=['accuracy'])

# ABOUT DATASET:

For this bot system, i have manually created the dataset. Since it is manual, it is a very small dataset in form of questions and responses. 

# METHODOLGY:

![project3](https://user-images.githubusercontent.com/43928250/142760663-a1a46cef-69d0-4956-b27f-eb77b7ad3753.png)

# IO IMAGES:

![image](https://user-images.githubusercontent.com/43928250/142760523-3e5d6d3b-154b-42c3-84d5-072257e6ef82.png)


# HOW TO RUN LOCALLY:
install the requirements using: pip install -r requirements.txt
model has been trained and stored in train.ipynb
since it is a flask app, run app.py to run this locally.
