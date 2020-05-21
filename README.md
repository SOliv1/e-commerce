# Django Ecommerce Project

## An Ecommerce app usig Django

`pip3 install django==1.11.29`

`pip freeze > requirements.txt`

`django-admin startproject blog .`

`pip3 install django`

`python3 manage.py migrate`

`python3 manage.py runserver`

`git init`

`.gitignore`
ignore all unwanted files below with following command:
`echo -e "*.db.sqlite3\n*.pyc\n_pycache_/" > .gitignore`

#travis
https://travis-ci.org

1.  click sign-in with GitHub
1.  signed in, 
1.  click on your name and the accounts menu.
1. scroll down the list of available repositories and hit the toggle switch there on our Django blog repository.
1.  So this is going to synchronize it with Travis.
1.   click on the repository name again because what we actually want to do now is to grab some markup here.
1.   no builds for the repository yet.
1.  click on where it says build unknown, then choose markdown from the drop-down menu, and copy the code that appears.
1.  add in our README.md file, and this is going to allow us to continually keep track of whether our project is passing the tests or not.
1.  paste it in at the bottom of our README.md file.
1.  save.
1.  create a new file to integrate with Travis.
1.   .travis.yml
1.   put some markup in here as well.
1.   language is Python.
1.   version that we're using is Python ?
1.   install command is `pip3 install -r requirements.txt`.
1.   And then we have the script to run it.
1.   We pass a SECRET_KEY here.
1.  We don't actually need to put our secret key in because we're passing a dummy one.
    This is for when we hide our secret key on Heroku.

`python --version` or `python -V` press enter

`python3 manage.py startapp posts`

`pip3 install pillow`   for images

`pip3 freeze > requirements.txt`

`python3 manage.py makemigrations`

`python3 manage.py migrate`

#create views

1.  Open up views.py in posts directory

`pip3 install django-forms-bootstrap` 
and add this to installed apps in settings.py as django_forms_bootstrap underscores.

`python3 manage.py createsuperuser`
## csrf_token
So let's return to our CSRF token.
This is a protection mechanism provided by Django to make sure that your website isn't vulnerable to cross-site request forgery attacks.
Now, you can read more about that on the Internet if you want.
Bootstrap takes care of this under the bonnet, so we don't have to.
But it's a very good practice to remember to include csrf_token in every form that we create.

login to admin
admin
admain@project.com
Blogsgalore

## Heroku

*secret key ''*
*Procfile*
*requirements.txt*

Heroku login
Dashboard go to create new app
settings page
fill in the environmental vairables
go to rescources and type in searchbox for **Heroku Postgres*
click on create new database - hobbydevelopment freeze
add secret key from env.py to environment variables in config variables
add the localhost 


`pip3 install dj-database-url psycopg2`  : connects our database to our urls

`pip3 freeze > requirements.txt` again to update requirements.txt


Comment out default database and create a new database dictionary not a string:

DATABASES = {
    'default': dj_database_url.parse(os.environ.get('DATABASE_URL'))
}

and then scroll to the top of setting.py to import it.
import dj_database_url

Collect the database url from postgres on heroku vars and add for local testing purposes only they will not go live.
and paste in the env.py file.
os.environ.setdefault(),

now we should be able to deploy:
`python3 manage.py makemigrations`

Deploy locally python3 manage.py runserver - when successfully deployed locally 
install a new libruary called *whitenoise* - allows us to host our static files, such as CSS and JavaScript, correctly on Heroku.

`pip3 install whitenoise`
`pip3 freeze > requirements.txt`
`pip3 install gunicorn`
`pip3 freeze > requirements.txt`

We could, actually, get away without installing these and just add them at the end of our requirements.txt file, but let's install them anyway.





