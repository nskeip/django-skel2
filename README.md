# Django skel 2

## About ##
This is a collection of useful templates for django-powered projects. Inspired by [django-project-skel by @amccloud](https://github.com/amccloud/django-project-skel).

## How it works ##
We have several branches and each one of them can be used as a template. Here they are:

### simple template ###
You'll get just a django project with some useful things such as:
* nice settings.py (with PROJECT_DIR and some other stuff)
* south
* media, static, templates and fixtures directories (and settings.py knows them!)
* default templates: base.html, 400.html, 500.html
* readme template
* /admin/ panel
* pythonic .gitignore
* uwsgi.ini

In order to use this template, you need to:
```bash
django-admin.py startproject --template https://github.com/nskeip/django-skel2/zipball/simple --extension py,md,ini YOUR_PROJECT_NAME
cd YOUR_PROJECT_NAME
python manage.py syncdb
```

### favs (favorites) template ###
Favorite packages added to the simple template.
You get (out of the box):
* Admin tools
* PIL
* Sorl.thumbnails
* simple captcha
* pytils
* pymorphy
* Three types of requirements: requirements.txt (common case), requirements-dev.txt (requirements for development only), requirements-production.txt (requirements for production)

In order to use this template, you need to:
```bash
django-admin.py startproject --template https://github.com/nskeip/django-skel2/zipball/favs --extension py,md,ini YOUR_PROJECT_NAME
cd YOUR_PROJECT_NAME
pip install -r ./requirements.txt
pip install -r ./requirements-dev.txt
python manage.py syncdb
python manage.py migrate
```

### Django CMS template ###
Django CMS added to Favorites template.

Usage:
```bash
django-admin.py startproject --template https://github.com/nskeip/django-skel2/zipball/django-cms --extension py,md,ini YOUR_PROJECT_NAME
cd YOUR_PROJECT_NAME
pip install -r ./requirements.txt
pip install -r ./requirements-dev.txt
python manage.py syncdb
python manage.py migrate
```