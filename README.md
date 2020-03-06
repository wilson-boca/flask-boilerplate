# flask-boilerplate

A Python restful-api boilerplate

### Set Environment Variables

Update *src/config.py*, and then run:

```sh
$ export APP_SETTINGS="src.config.DevelopmentConfig"
```

or

```sh
$ export APP_SETTINGS="src.config.ProductionConfig"
```

Set a SECRET_KEY:

```sh
$ export SECRET_KEY="some_secret_code"
```

Set the HOST/PORT:

```sh
$ export FLASK_RUN_HOST="0.0.0.0"
$ export FLASK_RUN_PORT=8000
```

### Create DB

Create the databases in `psql`:

```sh
$ psql
# create database api_db
# create database api_db_test
# \q
```

Create the tables and run the migrations:

```sh
$ python manage.py create_db
$ python manage.py db init
$ python manage.py db migrate
```

### Run the Application

```sh
$ python -m flask run
```

Access the application at the address [http://0.0.0.0:8000/](http://0.0.0.0:8000/)


### Testing

Without coverage:

```sh
$ python manage.py test
```

With coverage:

```sh
$ python manage.py cov
```
