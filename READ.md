# Demo App Using Django Celery and Redis for Image Thumbnail Generation

install python requirements

```
pip install -r requirements.txt
```

start redis-server in its own terminal window

```
redis-server
```

start celery worker in its own terminal window with the python virtual env from step 3 activated and in the same directory as the manage.py script

```
 celery worker -A image_parroter --loglevel=info
```

start django dev server, again in its own terminal window with the python virtual env from step 3 activated and in the same directory as the manage.py script

```
(venv) python manage.py runserver
```

Once these are complete you should be able to point your browser to http://localhost:8000 and see the Thumbnailer application
