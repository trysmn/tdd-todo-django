# Example TDD todo application with Django

## Getting started

- Clone the repository.
- Install [pyenv](https://formulae.brew.sh/formula/pyenv) to manage python versions.
- Install python version `3.7.12` using pyenv and use it:
  ```bash
  pyenv install 3.7.12
  pyenv use 3.7.12
  ```
- Create and enter a virtual environment:
  ```bash
  python -m venv venv
  source venv/bin/activate
  ```
- Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```
  
## Running the functional tests

- Generate an example django project:
  ```bash
  django-admin.py startproject superlists .
  ```
- Extract the `SECRET_KEY` and `DEBUG` values defined in the `superlists/settings.py` file
- Create a `.env` file and put the values for `SECRET_KEY` and `DEBUG` in there:
  ```env
  # .env
  SECRET_KEY="example_secret_key"
  DEBUG=True
  ```

- Run a server locally:
  ```bash
  python manage.py runserver
  ```

- Then run the functional tests:
  ```bash
  python functional_tests.py
  ```
