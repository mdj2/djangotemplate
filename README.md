# Django Quickstart
This is a Django project template that lets you get started on a Django project right away.

Setup some environment variables so you can just copy and paste the rest of the commands:

    DOMAIN="example.com"
    PROJECT_NAME="example"

Create a directory for your django project and start a virtual environment:

    adduser $DOMAIN
    cd $(getent passwd $DOMAIN | cut -d: -f6)
    virtualenv-2.6 --no-site-packages .env
    source .env/bin/activate
    pip install django

Start a new Django project using this git repo as a template:

    django-admin.py startproject --extension=py,conf --template=https://github.com/mdj2/django/archive/master.zip $PROJECT_NAME .

Install the neccessary packages, and make manage.py executable

    pip install -r requirements.txt
    chmod +x manage.py

Update the settings in `$PROJECT_NAME`/local_settings.py. Make sure you create the database it tries to connect to.

    vim $PROJECT_NAME/local_settings.py

And run (assuming 10.0.0.10 is your VM's IP address):

    ./manage.py runserver 10.0.0.10:8000

Point your browser to 10.0.0.10:8000

Write over this file with a README specific to your project. Init a repo:

    echo "# This is my project" > README.md
    git init
    git add .
    git commit -m "Initial commit"


