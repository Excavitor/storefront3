# storefront3

Django Project: storefront \
Django Apps: store, tags, playground, likes, core

core - use for users related tasks (see in settings)
```bash
URLS

    "products": "http://127.0.0.1:8000/store/products/",
    "collections": "http://127.0.0.1:8000/store/collections/",
    "carts": "http://127.0.0.1:8000/store/carts/",
    "customers": "http://127.0.0.1:8000/store/customers/",
    "orders": "http://127.0.0.1:8000/store/orders/"

    "hello": "http://127.0.0.1:8000/playground/hello/"
```

📧 Visit the [http://127.0.0.1:8000/playground/hello/](http://127.0.0.1:8000/playground/hello/) to trigger a fake email using SMTP.

📮 SMTP Admin Dashboard: [http://localhost:5000](http://localhost:5000)

### 1️⃣ Install Dependencies

```bash
pipenv install
pipenv shell
```

This activates a virtual environment.

To configure VS Code with the virtual environment:

```bash
where python
```

Copy the Python path (should end with `Scripts/python.exe`), then:

* Open Command Palette (`Ctrl+Shift+P`)
* Select `Python: Select Interpreter`
* Choose or paste the copied path
* Restart the terminal

---

### 2️⃣ Database Setup

(Optional: Delete old migrations if needed)

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py seed_db
```

> `seed_db` populates the database with test data.
> Command located in: `store/management/commands/seed_db.py`

---

### 3️⃣ Create Superuser & Run Server

```bash
python manage.py createsuperuser
python manage.py runserver
```

Your development server will start at: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## ⚙️ Celery & Redis Configuration

### 🔁 Redis (Message Broker)

Start Redis via Docker:

```bash
docker run -d -p 6379:6379 redis
```

Check if Redis is running:

```bash
docker ps
```

Install Redis Python client:

```bash
pipenv install redis
```

---

## 📁 Project Structure Overview

```
storefront3/
├── store/               # Main app
├── tags/
├── playground/
├── likes/
├── core/
├── manage.py
├── Pipfile
├── .env
└── README.md
```
---
