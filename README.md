First Install and Test Redis:
> sudo apt-get update
> sudo apt-get upgrade
> sudo apt-get install redis-server
> sudo service redis-server restart
> redis-cli

Then srt runserver, celery beat and celery worker:
python manage.py runserver
celery -A jokes_project beat -l INFO
celery -A jokes_project worker -l INFO