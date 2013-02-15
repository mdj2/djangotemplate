# Django Quickstart
This is a Django project template that lets you get started on a Django project right away.

Create a directory for your django project and start a virtual environment:

    adduser example.com
    cd ~example.com
    virtualenv-2.6 --no-site-packages .env
    source .env/bin/activate
    pip install django

Replace `example` with your project name, and execute:

    django-admin.py startproject --template=https://github.com/mdj2/django/archive/master.zip example .

Install the neccessary packages:

    pip install -r requirements.txt

Replace the settings in `example`/local_settings.py

    vim example/local_settings.py

And run

    python manage.py runserver 192.168.1.100:8000

