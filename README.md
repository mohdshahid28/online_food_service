# Online Food Service – Order Management System

A web-based Food Ordering and Order Management System built using Django. The application provides an online platform for managing food products and customer orders through a user-friendly interface.

## Tech Stack

- **Backend:** Python, Django
- **Frontend:** HTML, Django Templates
- **CSS Framework:** Tailwind CSS (CDN)
- **JavaScript:** JavaScript
- **Database:** SQLite
- **Version Control:** Git & GitHub

## Project Structure

Page templates, including shared components, are stored in `pages/templates/` and managed by the `pages` app.

## Prerequisites

Make sure you have installed:

- Python 3.14 or above
- Git
- pip

## Installation and Setup

### 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
```

### 2. Navigate to Project Directory

```bash
cd <PROJECT_FOLDER>
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate Virtual Environment

**Windows:**

```bash
venv\Scripts\activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Configure Environment Variables

Create a `.env` file in the project root directory (the directory containing the `dj` folder).

Add the following configuration:

```env
DJANGO_ENV=development
DJANGO_SECRET_KEY=replace_with_your_secret_key
DEBUG=True
ALLOWED_HOSTS=127.0.0.1,localhost

SQLITE_NAME=db.sqlite3

ADMIN_DEFAULT_USERNAME=admin@example.com
ADMIN_DEFAULT_PASSWORD=replace_with_a_strong_password
```

Replace the example values with your actual configuration.

### 7. Apply Database Migrations

```bash
python manage.py migrate
```

This applies database migrations and creates the initial staff account if it does not already exist.

### 8. Run the Development Server

```bash
python manage.py runserver
```

To use another port:

```bash
python manage.py runserver 7000
```

### 9. Access the Application

Open your browser and visit:

```text
http://127.0.0.1:8000/
```

### 10. Admin Login

Access the custom admin panel:

```text
http://127.0.0.1:8000/admin-login/
```

Use the username and password configured in your `.env` file.

## Database Management

Whenever you make changes to Django models, run:

```bash
python manage.py makemigrations
python manage.py migrate
```

## Git Workflow

### Pull Latest Changes

Before starting new development work, synchronize your local repository:

```bash
git pull origin main
```

### Commit Changes

Add modified files:

```bash
git add .
```

Create a commit:

```bash
git commit -m "Added new application functionality"
```

### Push Changes

Push your local changes to your designated remote branch:

```bash
git push origin main:YOUR_REMOTE_BRANCH
```

Use a meaningful branch name and commit message describing the changes.

## Important Notes

- Always activate the virtual environment before running Django commands.
- Never share your `.env` file or secret key publicly.
- Do not commit passwords or sensitive configuration details.
- Run migrations whenever database models are modified.
- Keep dependencies updated in `requirements.txt`.

## License

This project is intended for educational and development purposes.
