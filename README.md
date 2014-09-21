docker-django
---------------

Docker django server base image source. This is based on `devoto13/docker-gunicorn` image.

Image
-----

You can `pull` a ready to use image from Docker
[index](https://index.docker.io/u/devoto13/) running:

```
$ docker pull devoto13/django
```

Or build this repository:

```
$ git clone https://github.com/devoto13/docker-django.git
$ cd docker-django/
$ docker build -t devoto13/django .
```

Change `devoto13/django` to your Docker index username.

Container
---------

This image uses volumes and environment variables to control the django configuration.

Volumes:

* `/root/app/media`: Files uploaded by users.

You pass with `-v` docker option. Don't forget to use absolute path here.

Environment variable:

Also you need to specify all environment variables required by [docker-gunicorn](https://github.com/devoto13/docker-gunicorn) image.

* `DJANGO_SETTINGS_MODULE`: Django settings module.

You pass with `-e` docker option.

Usage
-----

Image intended to be used as base image for another `Dockerfile`. Take a look at the `example/` directory.
