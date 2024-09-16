# ML COVID Predictor

## Overview

This project involves a machine learning model designed to predict the likelihood of COVID-19 based on responses to 10 specific health-related questions.

### Questions in Portuguese

1. Apresenta febre?
2. Apresenta cansaço?
3. Apresenta tosse seca?
4. Apresenta espirro?
5. Apresenta dores no corpo?
6. Está corizando?
7. Apresenta dor de garganta?
8. Apresenta diarréia?
9. Apresenta dor de cabeça?
10. Apresenta falta de ar?

### Questions in English

1. Do you have a fever?
2. Are you feeling tired?
3. Do you have a dry cough?
4. Are you sneezing?
5. Do you have body aches?
6. Are you experiencing a runny nose?
7. Do you have a sore throat?
8. Do you have diarrhea?
9. Do you have a headache?
10. Are you experiencing shortness of breath?

## Project Explanation

1. **Data Preparation**: 
   - The `training_data.py` file contains the basic information, including the results and questions to be used for training the model.
   - The data, including features (`atributos`) and results (`resultados`), is extracted and stored in a SQLite database.
   - The data is then fetched from the database and transformed into a Pandas DataFrame.

2. **Data Transformation**:
   - The DataFrame is adjusted as needed for the model.
   - The DataFrame is converted to a NumPy array using the `to_numpy()` method for further processing.

## Running the Model

1. **Install Dependencies**:
   - Ensure you have all necessary packages installed by running:
     ```bash
     pip install -r requirements.txt
     ```

    - Pandas, Scikit Learn

2. **Run Jupyter Notebook**:
   - Launch Jupyter Notebook to interact with the model and analyze results.

## Saving and Loading the Trained Model
After training the model, you can save it for future use using the pickle library. This allows you to avoid retraining the model each time you want to make predictions. Here's how to do it:

Saving the Model:

Add the following code to save the trained model to a file:

`import pickle`

Assuming `model` is your trained model

```
with open('trained_model.pkl', 'wb') as file:
    pickle.dump(model, file)
```

Loading the Model:

To load the model later for making predictions, use the following code:

```
import pickle

with open('trained_model.pkl', 'rb') as file:
    model = pickle.load(file)
```
By saving the model, you can quickly reload it and use it for making predictions without the need to retrain it.

## Author

**Antero Júnior**

_Full Stack Developer @ Mesha Tecnologia_

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/antero-arcanjo)