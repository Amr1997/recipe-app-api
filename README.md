# Recipe App API

## Introduction

This repository contains the source code for a Recipe App API built using Django REST Framework. The API allows users to create and manage recipes, as well as authenticate and authorize users to access the app.

## Features

- User authentication and authorization
- Create, retrieve, update, and delete recipes
- Filter and search recipes by tags and ingredients
- Upload recipe images
- Tag and manage ingredients

## Requirements

- Python 3.6+
- Django 3.0+
- Django REST Framework 3.11+
- PostgreSQL (optional)

## Installation

1. Clone the repository:
```
git clone https://github.com/Amr1997/recipe-app-api.git
```

2. Install the required packages:
```
pip install -r requirements.txt
```

3. Set up the database (optional):
```
python manage.py migrate
```

4. Create a superuser:
```
python manage.py createsuperuser
```

## Running the app

1. Start the development server:
```
python manage.py runserver
```

2. Access the app at `http://localhost:8000/`

## API endpoints

- `/api/user/create/` - create a new user
- `/api/user/token/` - get a user's authentication token
- `/api/recipe/tags/` - list all availablerecipe tags
- `/api/recipe/ingredients/` - list all available recipe ingredients
- `/api/recipe/recipes/` - list all recipes
- `/api/recipe/recipes/<id>/` - retrieve a specific recipe
- `/api/recipe/recipes/create/` - create a new recipe
- `/api/recipe/recipes/<id>/update/` - update an existing recipe
- `/api/recipe/recipes/<id>/delete/` - delete an existing recipe

## Authentication and Authorization

The API uses token-based authentication to authenticate and authorize users. To access protected endpoints, users must provide a valid authentication token in the request headers. Tokens can be obtained by sending a POST request to `/api/user/token/` with a valid username and password.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

This project was built using the Django REST Framework tutorial by [Mark Winterbottom](https://github.com/markwinterbottom). Special thanks to Mark for providing such a great resource for learning Django REST Framework!
