# Employee-Salary-Analysis

In this project, the code is a Python script embedded in a Jupyter notebook JSON structure. It showcases how to create, train, and deploy a simple machine learning model to predict employee salaries based on their years of experience and age. The script uses popular Python libraries such as Numpy, Pandas, Scikit-learn for machine learning tasks, and Gradio for creating a web interface to interact with the model.

1. *Library Imports:*
   - numpy and pandas for data manipulation.
   - gradio for creating a web interface to interact with the machine learning model.
   - pickle for saving (serializing) the model and later loading (deserializing) it.

2. *Data Preparation:*
   - Loads an employee dataset from a CSV file named 'Employeess.csv'.
   - Splits the dataset into features (X) and the target variable (y), where X contains all columns except the last one, and y contains the last column (assumed to be the salary or a target variable to predict).

3. *Model Training:*
   - Splits the dataset into training and test sets with a test size of 20% and a random state for reproducibility.
   - Trains a LinearRegression model with the training data.

4. *Model Serialization:*
   - Saves the trained model to a file named 'Employee.pkl' using the pickle library. This process allows the model to be reused without the need to retrain.

5. *Prediction Function:*
   - Defines a function predict that takes in years of experience and age as inputs.
   - Loads the trained model from the 'Employee.pkl' file.
   - Uses the model to predict the salary based on the input features and returns the prediction.

6. *Gradio Interface:*
   - Creates input fields for years of experience and age using Gradio's Number component.
   - Sets up an output textbox to display the model's prediction.
   - Initializes a Gradio app with the predict function as its backend, specifying the input and output components.

7. *App Launch:*
   - Launches the Gradio app, making it available as a web interface where users can input the years of experience and age to get salary predictions.

The metadata and output sections in the JSON are related to the notebook's environment, such as execution counts and outputs of the code cells, including messages about running the Gradio app in a Colab notebook environment and how to create a public link for the Gradio app.
