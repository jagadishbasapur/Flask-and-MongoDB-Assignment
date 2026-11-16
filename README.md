# Flask & MongoDB Assignment

A Flask application that provides a JSON API and a student registration form backed by MongoDB Atlas.

## Features
- `GET /api`: reads `data.json` and returns the records as JSON.
- `GET /`: displays the student registration form.
- `POST /`: validates form data and inserts a student document into MongoDB Atlas.
- Successful submissions redirect to `/success`.
- Submission/database errors are displayed on the form page.

## Project structure
```text
Flask_and_MongoDB_Jagadish/
├── app.py
├── data.json
├── requirements.txt
├── .env.example
├── .gitignore
├── templates/
│   ├── index.html
│   └── success.html
├── Screenshots/
├── Documentation.docx
└── README.md
```

## Setup (Ubuntu / WSL)
```bash
sudo apt update
sudo apt install python3-pip python3-venv -y
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
```

Edit `.env` and replace the placeholders with your MongoDB Atlas connection string. Do not commit `.env` or share your database password.

In MongoDB Atlas, create a database user and allow the public IP address of the machine running Flask in Network Access.

Run:
```bash
python3 app.py
```

Open:
- Form: http://127.0.0.1:5000/
- JSON API: http://127.0.0.1:5000/api

## MongoDB collection
The application writes to:
- Database: `flask_assignment`
- Collection: `students`

Each document contains `name`, `email`, and `course`.

## GitHub repository
After creating your repository, replace this placeholder with your actual repository URL:
https://github.com/YOUR-GITHUB-USERNAME/Flask-and-MongoDB-Assignment
