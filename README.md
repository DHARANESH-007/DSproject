# Student Performance Prediction

A machine learning web application that predicts student performance based on demographic information, parental education, lunch type, test preparation, and reading and writing scores.

The project demonstrates an end-to-end machine learning workflow, from data preprocessing and model training to deployment through a Flask web application.

## Project Preview

### Homepage

<img width="1600" height="819" alt="WhatsApp Image 2026-10-28 at 9 07 50 PM" src="https://github.com/user-attachments/assets/bc11358a-55de-4c81-bdd5-a408065582da" />


### Student Prediction Form

![Prediction Form](images/prediction-page.png)

### Prediction Result

![Prediction Result](images/prediction-result.png)

## Features

- **Student data input:** Collects student demographic and academic information through a web form.
- **Data preprocessing:** Handles categorical and numerical features using a preprocessing pipeline.
- **Machine learning prediction:** Uses a trained regression model to predict student mathematics performance.
- **Web interface:** Provides a Flask-based interface for submitting inputs and viewing predictions.
- **Reusable pipeline:** Separates prediction logic from the web application.
- **Model persistence:** Saves trained models and preprocessing objects for reuse during inference.

## Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Web Framework | Flask |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Model Persistence | Pickle |
| Frontend | HTML, CSS |
| Development Tools | VS Code, Git |

## Project Structure

```text
Student-Performance-Prediction/
│
├── artifacts/
│   ├── model.pkl
│   └── preprocessor.pkl
│
├── notebook/
│   └── data/
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   │
│   ├── pipeline/
│   │   ├── predict_pipeline.py
│   │   └── train_pipeline.py
│   │
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
│
├── templates/
│   └── home.html
│
├── static/
│   └── style.css
│
├── app.py
├── requirements.txt
├── setup.py
└── README.md
```

*Note: Adjust the structure above to match the files and folders actually present in your repository.*

## How It Works

1. **Data ingestion:** Loads the student performance dataset and separates features from the target variable.
2. **Data transformation:** Processes numerical and categorical features into a format suitable for machine learning.
3. **Model training:** Trains and evaluates regression models to identify a suitable prediction model.
4. **Model serialization:** Saves the trained model and preprocessing pipeline.
5. **User input:** The Flask application collects student details through an HTML form.
6. **Preprocessing:** The submitted inputs are transformed using the saved preprocessor.
7. **Prediction:** The trained model generates the predicted mathematics score.
8. **Result display:** The application displays the prediction to the user.

## Input Features

The application uses the following inputs:

- Gender
- Race or ethnicity
- Parental level of education
- Lunch type
- Test preparation course
- Reading score
- Writing score

**Target variable:** Mathematics score.

## Installation and Setup

### Prerequisites

- Python installed on your system
- Git
- A terminal or command prompt

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_PROJECT_FOLDER>
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

If your project uses editable package installation and your `setup.py` is configured correctly, you can also run:

```bash
pip install -e .
```

### 4. Run the application

```bash
python app.py
```

Open the local URL printed in the terminal, commonly:

```text
http://127.0.0.1:5000/
```

## Usage

1. Open the application in your browser.
2. Enter the student's demographic and academic details.
3. Submit the prediction form.
4. View the predicted mathematics score on the results page.

## Machine Learning Workflow

The project follows a modular machine learning pipeline:

- Data ingestion
- Exploratory data analysis and feature understanding
- Feature preprocessing
- Model training and evaluation
- Model serialization
- Inference through a Flask application

The saved preprocessing object ensures that incoming data is transformed using the same fitted preprocessing steps used during model development.

## Deployment

The Flask application can be deployed to a hosting platform that supports Python web applications. AWS Elastic Beanstalk is one possible option.

Before deployment:

- Confirm that all required dependencies are listed in `requirements.txt`.
- Ensure the model and preprocessor artifacts are available to the application.
- Configure the application to run with a production-ready WSGI server.
- Review cloud resource costs before creating a deployment environment.

## Future Improvements

- Add model evaluation metrics to the application.
- Improve input validation and error handling.
- Add interactive visualizations for student performance.
- Create a prediction history dashboard.
- Deploy the application to a cloud platform.
- Add automated testing and continuous integration.

## Learning Outcomes

Through this project, I gained practical experience with:

- Building a modular machine learning pipeline.
- Preprocessing numerical and categorical data.
- Training and evaluating regression models.
- Saving and loading trained ML artifacts.
- Integrating a machine learning model with Flask.
- Collecting user input and generating predictions through a web interface.
- Structuring a Python project for maintainability.

## Acknowledgements

This project was developed as a hands-on machine learning learning project, following the general workflow demonstrated in educational material by Krish Naik.

## Author

**Dharanesh D. B.**

- GitHub: [DHARANESH-007](https://github.com/DHARANESH-007)

---

If you found this project useful, consider giving the repository a star.
