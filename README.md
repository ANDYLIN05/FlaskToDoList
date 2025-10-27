Flask ToDo List Application

This is a simple, full-stack ToDo list application built using the Flask web framework, SQLAlchemy for database management, and Jinja2 for templating.

It allows users to add new tasks, view existing tasks, delete tasks, and update tasks, with the newest tasks appearing at the top of the list.

Features

Add Tasks: Quickly add new tasks via a simple form.

View Tasks: Displays all tasks in a clean table format.

Delete Tasks: Permanently remove tasks.

Update Tasks: Modify the content of an existing task (and automatically move it to the top of the list).

Persistence: Tasks are stored in a local SQLite database (test.db).

Setup and Installation

Follow these steps to get the application running on your local machine.

1. Clone the Repository

Clone this repository to your local machine:

git clone [https://github.com/YourUsername/FlaskToDoList.git](https://github.com/YourUsername/FlaskToDoList.git)
cd FlaskToDoList


2. Create and Activate a Virtual Environment

It is highly recommended to use a virtual environment to manage dependencies:

# Create the environment
python -m venv env

# Activate the environment (Windows)
.\env\Scripts\activate

# Activate the environment (macOS/Linux)
source env/bin/activate


3. Install Dependencies

This project requires Flask and Flask-SQLAlchemy. You can install them using pip:

pip install Flask Flask-SQLAlchemy


4. Initialize the Database

Since the database file (test.db) is ignored by Git, you must create the database tables required by the Todo model.

Run the Python interpreter in your terminal:

python


Once in the Python shell, run the following commands to initialize the database:

# Import the necessary modules (assuming your main file is named app.py)
from app import db, app

# Push the application context to access the database connection
with app.app_context():
    db.create_all()

# Exit the shell
exit()


5. Run the Application

Start the Flask development server:

python app.py


The application will now be running. Open your web browser and navigate to:

http://127.0.0.1:5000/
