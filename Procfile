release: cd src; python3 manage.py migrate
web: cd src; gunicorn monitor.wsgi -b 0.0.0.0:$PORT
celery: cd src; celery worker --app=monitor -l info
beat: cd src; celery -A monitor beat -l info