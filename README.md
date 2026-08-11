# Disease Prediction Project

This project aims to develop a machine learning model that can predict diseases based on a set of symptoms provided by the user. The core idea is to train a classification model on a dataset linking symptoms to diseases, and then deploy this model as an interactive web application.

## Project Structure and Workflow

The project follows a standard machine learning workflow, which includes:

1.  **Data Loading and Extraction**: The initial dataset, provided in a zipped format, is extracted and loaded into a pandas DataFrame. This step ensures that the raw data is accessible for further processing.

2.  **Exploratory Data Analysis (EDA)**: Basic analysis is performed to understand the distribution of diseases within the dataset. This helps in identifying potential imbalances and overall data characteristics.

3.  **Data Preprocessing**: This crucial step involves several transformations:
    *   **Handling Missing Values**: Symptoms that are not present are explicitly marked as 'No_Symptom' to ensure consistency.
    *   **Label Encoding**: Both the symptom names and disease names are converted into numerical representations. This is necessary for the machine learning algorithms to process them.
    *   **Feature Engineering**: The raw symptom data is transformed to prepare it for model training.

4.  **Data Resampling (SMOTE)**: To address potential class imbalance, Synthetic Minority Over-sampling Technique (SMOTE) is applied. This technique generates synthetic samples for minority classes, ensuring that the model does not become biased towards majority classes.

5.  **Feature Selection**: To improve model performance and reduce complexity, relevant features (symptoms) are selected using statistical methods. This step identifies the most impactful symptoms for disease prediction.

6.  **Model Training**: A Random Forest Classifier is chosen for its robustness and ability to handle complex datasets. The model is trained on the preprocessed and feature-selected data.

7.  **Model Evaluation**: The trained model's performance is assessed using metrics such as accuracy, precision, recall, and F1-score. This helps in understanding how well the model generalizes to unseen data.

8.  **Model Persistence**: The trained model and all necessary preprocessing tools (like label encoders and scalers) are saved. This allows the model to be loaded and used later without retraining.

9.  **Deployment (Streamlit App)**: The machine learning model is integrated into a Streamlit web application. This application provides an intuitive user interface where users can select symptoms and receive a predicted disease along with relevant recommendations. The app code is written to `app.py` and then executed.

## Getting Started

To run this project, ensure you have the necessary Python libraries installed. The Streamlit application can be run directly from the command line after saving the `app.py` file.

## Dataset

For this project, I used this public dataset shared on Kaggle: [Kaggle Dataset](https://www.kaggle.com/datasets/itachi9604/disease-symptom-description-dataset)

## Acknowledgment
Streamlit UI Development: My colleague **Ridha Burair Hashim**
