
---

COFFEE YIELD PREDICTION APPLICATION

---

Overview  
This application is a Django-based web system that uses a machine learning model (trained using XGBoost in Jupyter Notebook) to predict coffee yields. The model has been integrated into a Django web framework where users can input parameters and receive real-time predictions. Django Admin is used to manage the backend database entries.

---

Features

- Predicts coffee yields using a pre-trained XGBoost machine learning model.
- Clean, responsive user interface for data entry and displaying results.
- Admin dashboard for managing prediction records.
- SQLite database support using Django ORM.
- Static file management for front-end assets.

---

Technologies Used

- Backend Framework: Django
- Machine Learning: XGBoost, Pandas (trained externally in JupyterNotebook)
- Frontend: HTML, CSS via Django templates
- Database: SQLite (default Django DB)
- Other Libraries: joblib or pickle for loading ML model

---

Project Structure

- coffeeApp/ – Main Django project directory
- coffee/ – Django app containing views, models, and logic
- staticfiles/ – CSS, JS, and images
- best_xgb_model_bayes.pkl – Pre-trained XGBoost model file
- db.sqlite3 – SQLite database file
- manage.py – Django's project manager script
- requirements.txt – List of project dependencies
- README.md – Project documentation

---

How to Set Up and Run the Project

1. Clone the repository:
   - git clone https://github.com/IvyNyawira/Coffee-Yield-Predictor.git
   - cd into the cloned directory

2. Create a virtual environment:
   - python -m venv venv

3. Activate the virtual environment:
   - On Windows: venv\Scripts\activate
   - On macOS/Linux: source venv/bin/activate

4. Install project dependencies:
   - pip install -r requirements.txt

5. Run database migrations:
   - python manage.py makemigrations
   - python manage.py migrate

6. Start the development server:
   - python manage.py runserver

7. Open your browser and go to:
   - http://127.0.0.1:8000/

---

How It Works (Prediction Flow)

1. The user inputs data into the form on the homepage.
2. The application loads the best_xgb_model_bayes.pkl file.
3. The input data is preprocessed and passed to the XGBoost model.
4. The model predicts the expected coffee yield.
5. The prediction is displayed to the user in the browser.

---

Admin Panel Usage

To access Django's admin interface:

1. Create a superuser:
   - python manage.py createsuperuser

2. Log in at:
   - http://127.0.0.1:8000/admin

---

Dependencies (requirements.txt)

Example list of dependencies:

- Django>=4.0
- xgboost
- pandas
- scikit-learn
- joblib

---

License

This project is licensed under the Apache-2.0 License.

---

Author

Developed by Ivy N Warui (@IvyNyawira on GitHub)

---
