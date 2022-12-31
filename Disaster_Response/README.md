# Disaster Response Pipeline Project

## Table of Contents
 * [Project Motivation](#project-motivation)
 * [File Descriptions](#file-descriptions)
 * [Components](#components)
 * [Instructions of How to Interact With Project](#instructions-of-how-to-interact-with-project)
 * [Licensing, Authors, Acknowledgements, etc.](#licensing-authors-acknowledgements-etc)
 
### Project Motivation

- This project comprised of both data science and software enginerring skills, its an absolute stiff lerning curve
    - Build Data pipeline and ML pipelines 
    - Categorize real messages sent during disaster events so that they can be channeled toi appropriate relief agency
    - Flask app dashboard where a user can input new message and get classification and visualizations
### File Descriptions
app    

| - template    
| |- master.html # main page of web app    
| |- go.html # Results page for the classification   
|- run.py # Flask app, entry point into the app <code> python3 run.py </code> 


data    

|- disaster_categories.csv # Data used in model bulding   
|- disaster_messages.csv # Unprocessed data   
|- process_data.py # data cleaning pipeline    

-InsertDatabaseName.db # database to save clean data to, to create efficiency durinmg predictions     

Images 

| - 3 screenshots representing working flash dashboard

models   

|- train_classifier.py # machine learning pipeline     
|- classifier.pkl # saved model     


README.md    

Libraries versions

`Numpy version: 1.24.1.`
`sqlalchemy version: 1.4.45.`
`Pandas version: 1.5.2.`
`Matplotlib version: 3.6.2.`

### Components


#### 1. ETL Pipeline
A Python script, `process_data.py`, writes a data cleaning pipeline that:

- Performs the whole ETL process
 
A jupyter notebook `ETL Pipeline Preparation` was used to do EDA to prepare the process_data.py python script. 
 
#### 2. ML Pipeline
A Python script, `train_classifier.py`, writes a machine learning pipeline that:

 - Loads data from the SQLite database
 - Splits the dataset into training and test sets
 - Builds a text processing and machine learning pipeline
 - Trains and tunes a model using GridSearchCV
 - Outputs results on the test set
 - Exports the final model as a pickle file
 
 `ML Pipeline Preparation` notebook used to prepare data for train_classifier.py python script. 

#### 3. Flask Web App
The project includes a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data. The outputs are shown below:

![app3](./images/screenshot1.JPG)

![app1](./images/screenshot2.JPG)


![app2](./images/screenshot3.JPG)


### Instructions of How to Interact With Project:
Instructions to get similar results
    - To run the ETL
        <code> python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db</code>
    - To run the ML pipeline
        <code> python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl <code>

- Fire up the app using this command.
    <code> python run.py<code>

- Go to http://0.0.0.0:3001/


### Licensing, Authors, Acknowledgements, etc.
Big thanks to Udacity for starter code and appen for the data ❤️
