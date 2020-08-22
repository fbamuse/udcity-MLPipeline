# Udcity-MLPipeline
Disaster Response Web-Application

This allocation estimates the message's intent category from the disaster message.
It consists of the following three configurations.

Project Components
1.ETL Pipeline
・Loads the messages and categories datasets
・Merges the two datasets
・Cleans the data
・Stores it in a SQLite database

2. ML Pipeline
    Loads data from the SQLite database
    Splits the dataset into training and test sets
    Builds a text processing and machine learning pipeline
    Trains and tunes a model using GridSearchCV
    Outputs results on the test set
    Exports the final model as a pickle file

3. Flask Web App


Instructions:

    Run the following commands in the project's root directory to set up your database and model.
        To run ETL pipeline that cleans data and stores in database python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
        To run ML pipeline that trains classifier and saves python models/train_classifier.py data/DisasterResponse.db models/disaster_model.pkl

    Run the following command in the app's directory to run your web app. python run.py

    Go to http://0.0.0.0:3001/

