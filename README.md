# This is a Simple Python Code that prints Hello World using Flask framework



#Setup Environment
#Install Git
#Install python tools & nginx(Optional)

$ sudo yum update
$ sudo yum install python3 (If not installed already)
$ sudo yum install python-pip3

# Install virtualenv from pip so that the python packages for the flask app will be in isolation.
$ sudo pip3 install virtualenv

# Create the project & setup the virtual environment.
# Create Project
$ cd Hello_Flask_App

# Create virtualenv
$ virtualenv venv

# Activate virtualenv
$ source ./venv/bin/activate

Now the prompt should look like:
(venv)user@host:~/Hello_Flask_App$

# Creating a Flask App: app.py

# Install the dependencies under your virtualenv
(venv)user@host:~/Hello_Flask_App$ pip3 install gunicorn flask

# Test your flask app:
(venv)user@host:~/Hello_Flask_App$ python app.py

Go to your browser and enter the url to your server, appending the port number you specified in app.py. You should see Hello World! displayed

##############################################################################################################################################

# Binding with Gunicorn
Create the WSGI entrypoint ~/Hello_Flask_App/wsgi.py.

# Run app.py
(venv)user@host:~/Hello_Flask_App$ gunicorn --bind 0.0.0.0:8080 wsgi:app

#Note: If you didn't name your app as application, for example as app, use wsgi:app instead of wsgi, since application is the name to be picked up by default.

Go to your browser again and read the Hello World! response


###############################################################

# To perform Test on the app.py using test_app.py
$python test_app.py

# The above will not return anything of success


