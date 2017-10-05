web: newrelic-admin run-program gunicorn --pythonpath="$PWD/encuestas-backend-django" wsgi:application
worker: python encuestas-backend-django/manage.py rqworker default