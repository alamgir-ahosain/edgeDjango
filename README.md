

#  Django : To-Do List

  A simple Django-based task manager where users can sign up, log in, and manage their to-do lists with an easy-to-use interface.

##  Project Structure
```plaintext
todo_list/
│
├── base/                          # Core app
│   ├── migrations/                # DB migrations
│   ├── templates/base/            # HTML templates
│   │   ├── login.html             # Login page
│   │   ├── main.html              # Home page
│   │   ├── register.html          # Registration page
│   │   ├── task_confirm_delete.html # Delete task confirmation
│   │   ├── task_form.html         # Task form
│   │   ├── task_list.html         # Task list
│   │   └── task.html              # Task detail
│   │
│   ├── __init__.py                # Package file
│   ├── admin.py                   # Admin settings
│   ├── apps.py                    # App config
│   ├── models.py                  # DB models
│   ├── tests.py                   # Tests
│   ├── urls.py                    # App URLs
│   └── views.py                   # Views
│
├── todo_list/                     # Project config
│   ├── __init__.py                # Package file
│   ├── asgi.py                    # ASGI config
│   ├── settings.py                # Settings
│   ├── urls.py                    # Project URLs
│   └── wsgi.py                    # WSGI config
│
├── db.sqlite3                     # Database file
├── manage.py                      # Django manager
├── Procfile                       # Deployment config
├── requirements.txt               # Dependencies
├── runtime.txt                    # Python version
└── README.md                      # Documentation
```
##  Features

-  Add, update, and delete tasks
-  Mark tasks as complete/incomplete
-  User authentication (login/register/logout)
-  Admin interface
-  Ready for deployment (Heroku-compatible)

---

##  Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/alamgir-ahosain/edgeDjango.git
cd django-TO-DO-List
````

### 2. Create & Activate a Virtual Environment

**Windows:**

```bash
python -m venv env
env\Scripts\activate
```

**macOS/Linux:**

```bash
python3 -m venv env
source env/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply Database Migrations

```bash
python manage.py migrate
```

### 5. Create a Superuser (Optional)

```bash
python manage.py createsuperuser
```

### 6. Run the Server

```bash
python manage.py runserver
```

Visit: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

##  Default Routes

* `/` - Home/Task list view
* `/login/` - User login
* `/register/` - User registration
* `/logout/` - Logout
* `/admin/` - Admin panel (superuser only)

---

##  Deployment

This project is configured for deployment on **Heroku**:

* `Procfile` - Declares the command to run your app
* `runtime.txt` - Specifies Python version
* `requirements.txt` - Lists dependencies

To deploy to Heroku:

```bash
# If you haven't already
heroku login
heroku create your-app-name
git push heroku main
heroku run python manage.py migrate
heroku open
```

---

