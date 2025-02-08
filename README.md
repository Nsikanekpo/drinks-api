# Drinks API

A simple REST API built with Django REST Framework to manage a collection of drinks.

## Features
- Retrieve a list of all drinks
- Add a new drink
- Retrieve details of a specific drink
- Update an existing drink
- Delete a drink

## Technologies Used
- Python
- Django
- Django REST Framework (DRF)

## Installation

### 1. Clone the Repository
```sh
git clone https://github.com/YOUR_GITHUB_USERNAME/drinks-api.git
cd drinks-api
```

### 2. Create a Virtual Environment
```sh
python -m venv venv
venv\Scripts\activate  # On Windows
```

### 3. Install Dependencies
```sh
pip install -r requirements.txt
```

### 4. Apply Migrations
```sh
python manage.py migrate
```

### 5. Run the Development Server
```sh
python manage.py runserver
```

## API Endpoints

### 1. Get All Drinks
```http
GET /drinks/
```
**Response:**
```json
[
  {
    "id": 1,
    "name": "Grape Soda",
    "description": "Very Grapey"
  }
]
```

### 2. Add a New Drink
```http
POST /drinks/
```
**Request Body:**
```json
{
  "name": "Pepsi",
  "description": "A popular cola drink"
}
```
**Response:**
```json
{
  "id": 2,
  "name": "Pepsi",
  "description": "A popular cola drink"
}
```

### 3. Get a Single Drink
```http
GET /drinks/{id}
```
**Response:**
```json
{
  "id": 1,
  "name": "Coca Cola",
  "description": "A refreshing soda"
}
```

### 4. Update a Drink
```http
PUT /drinks/{id}
```
**Request Body:**
```json
{
  "name": "Sprite",
  "description": "A lemon-lime soda"
}
```
**Response:**
```json
{
  "id": 1,
  "name": "Sprite",
  "description": "A lemon-lime soda"
}
```

### 5. Delete a Drink
```http
DELETE /drinks/{id}
```
**Response:**
```http
204 No Content
```

## Project Structure
```
drinks-api/
│── core/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── serializers.py
│   ├── tests.py
│   ├── urls.py
│   ├── views.py
│── drinks_api/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│── manage.py
│── requirements.txt
```

## Deployment
To deploy this API, consider using AWS, Heroku, or any cloud provider of your choice.


## Contributing
Feel free to fork this repository and contribute! Submit a pull request with any improvements.

