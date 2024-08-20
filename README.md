# CardioPredictor

CardioPredictor is a web application designed to predict the 10-year risk of heart disease based on various user inputs. Built using Flask and machine learning libraries, this application provides a user-friendly interface to input health data and receive risk predictions.

## Features

- Predicts the risk of heart disease using machine learning models.
- User-friendly web interface for entering health-related information.
- Deployed on Render for easy access and usage.

## Technologies

- **Flask**: Web framework for Python.
- **NumPy**: Library for numerical computations.
- **scikit-learn**: Machine learning library for building prediction models.
- **Gunicorn**: WSGI HTTP Server for Python applications.

## Installation

To run this project locally, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/ashwarytripath/CardioPredictor.git
cd CardioPredictor
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # On Windows use `venv\Scripts\activate`
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
python main.py
```

The application will be accessible at `http://127.0.0.1:5000/`.

## Deployment

### Render

To deploy the application on Render:

1. **Sign Up/Log In**: Go to [Render](https://render.com) and create an account or log in.
2. **Create a New Web Service**:
   - Select **New** > **Web Service**.
   - Connect your GitHub repository.
   - Choose the branch you want to deploy.
   - Set the **Build Command** to `pip install -r requirements.txt`.
   - Set the **Start Command** to `gunicorn -w 4 -b 0.0.0.0:8080 main:app`.
   - Ensure you have a `runtime.txt` file specifying `python-3.12`.

### Example `runtime.txt`

```
python-3.12
```

### Example `Procfile` (Optional)

```
web: gunicorn -w 4 -b 0.0.0.0:8080 main:app
```

## Usage

1. Navigate to the deployed application URL: [CardioPredictor](https://cardiopredictor-1.onrender.com).
2. Fill out the form with the following details:
   - Gender
   - Age
   - Current Smoker (Yes/No)
   - Cigarettes Per Day
   - BP Medications (Yes/No)
   - Prevalent Stroke (Yes/No)
   - Prevalent Hypertension (Yes/No)
   - Diabetes (Yes/No)
   - Total Cholesterol
   - Systolic BP
   - Diastolic BP
   - BMI
   - Heart Rate
   - Glucose Level
3. Click the **Predict** button to get the risk prediction.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, please reach out to [ashwary.040104@gmail.com](mailto:ashwary.040104@gmail.com).
