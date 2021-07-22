# What is Docker?
Docker is an open source containerization platform. It enables developers to package applications into containers—standardized executable components combining application source code with the operating system (OS) libraries and dependencies required to run that code in any environment. Containers simplify delivery of distributed applications, and have become increasingly popular as organizations shift to cloud-native development and hybrid multicloud environments.

Developers can create containers without Docker, but the platform makes it easier, simpler, and safer to build, deploy and manage containers. Docker is essentially a toolkit that enables developers to build, deploy, run, update, and stop containers using simple commands and work-saving automation through a single API.


## Images
Ok, let’s create our own image for something more “real.” How about the Python programming language? We can create an image and container just for Python and later add on to it.

First create a local directory on your computer for our code. I’ve chosen to make a code folder on my Desktop (I’m using an Apple computer) and then a python3.7 folder within that.
```
$ cd ~/Desktop
$ mkdir code && cd code
$ mkdir python3.7 && cd python3.7
```
Now we need to define the image with a Dockerfile. This is similar to a Pipenv or a requirements.txt file; it is a list of all the requirements needed to build our image. It is simpler to have them all in one place rather than install each manually line-by-line.

If you are on a Mac, you can create a new Dockerfile on the command line using the touch command.
```
$ touch Dockerfile
```
With your text editor add the following single line of code to the Dockerfile.

# Dockerfile
FROM python:3.7-alpine
Dockerfiles are read from top-to-bottom. The first instruction must be the FROM command which lets us import a base image to use for our image. This base image could be another Docker image or one we create entirely from scratch.

In this case we’ll be using the official Docker image for Python 3.7, specifically the alpine version which includes only the bare minimum needed to run Python. The alpine version takes up 78MB of space versus full Python’s 923MB so it is a good option to start with!

# Django Rest Framework

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

## How to include django rest framwork into Django project

- After the django project has been created useing the steps you already knew

Then on the command line type the below.
```
(library) $ pipenv install djangorestframework~=3.11.0

```


Add it to the INSTALLED_APPS config in our settings.py file. I like to make a distinction between third-party apps and local apps as follows since the number of apps grows quickly in most projects.

 config/settings.py

 ```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',

    # 3rd party
    'rest_framework', # new

    # Local
    'books',
]

```


Ultimately, our API will expose a single endpoint that lists out all books in JSON. So we will need a new URL route, a new view, and a new serializer file (more on this shortly).

There are multiple ways we can organize these files however my preferred approach is to create a dedicated api app. That way even if we add more apps in the future, each app can contain the models, views, templates, and urls needed for dedicated webpages, but all API-specific files for the entire project will live in a dedicated api app.

Let’s first create a new api app.
```
(library) $ python manage.py startapp api
```
Then add it to INSTALLED_APPS.

 config/settings.py

 ```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',

    # 3rd party
    'rest_framework',

    # Local
    'books',
    'api', # new
]
The api app will not have its own database models so there is no need to create a migration file and run migrate to update the database.
```

- URLs
Let’s start with our URL configs. Adding an API endpoint is just like configuring a traditional Django app’s routes. First at the project-level we need to include the api app and configure its URL route, which will be api/.

 config/urls.py
 ```
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('api/', include('api.urls')), # new
    path('', include('books.urls')),
]
```
Then create a urls.py file within the api app.

```
(library) $ touch api/urls.py
```
And update it as follows:

api/urls.py
```
from django.urls import path
from .views import BookAPIView

urlpatterns = [
    path('', BookAPIView.as_view()),
]
```

- viewa

Next up is our views.py file which relies on Django REST Framework’s built-in generic class views. These deliberately mimic traditional Django’s generic class-based views in format, but they are not the same thing.

To avoid confusion, some developers will call an API views file apiviews.py or api.py. Personally, when working within a dedicated api app I do not find it confusing to just call a Django REST Framework views file views.py but opinion varies on this point.

Within our views.py file, update it to look like the following:

api/views.py
```
from rest_framework import generics

from books.models import Book
from .serializers import BookSerializer


class BookAPIView(generics.ListAPIView):
    queryset = Book.objects.all()
    serializer_class = BookSerializer
 ```   
On the top lines we import Django REST Framework’s generics class of views, the models from our books app, and serializers from our api app (we will make the serializers next).

Then we create a BookAPIView that uses ListAPIView to create a read-only endpoint for all book instances. There are many generic views available and we will explore them further in later chapters.

The only two steps required in our view are to specify the queryset which is all available books, and then the serializer_class which will be BookSerializer.