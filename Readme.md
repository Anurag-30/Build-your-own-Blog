# Hosting A Sample Web Application Using Flask Framework

To run locally(on centos) do the following steps:
`sudo yum install python3` to install python3
`sudo yum install python3-pip` to install pip
`cd Build-your-own-Blog/` 
`python3 -m venv flaskblog/venv` create a virtual environment
`source flaskblog/venv/bin/activate` activating virtual environment
`pip install -r requirements.txt` Installing dependencies and packages

Generate a secretkey:

open python interpreter by using pytho3 command

import secrets
secrets.token_hex(16)

This will be your secret key which will be used by the application.

We need to have the following parameters to run the project:

open ~/.bash_profile file and add the following variables:

export EMAIL_USER="Your Email"
export EMAIL_PASS="Password for your email"
export SECRET_KEY="770dc8cc0080d058e4edfae57c7e11c1"
export SQLALCHEMY_DATABASE_URI="sqlite:///site.db"

The EMAIL_USER and EMAIL_PASS are not mandatory but the forgot password featute won't be working without them

`source ~/.bash_profile`

now we are all set to run the application using:
`export FLASK_APP=run.py`
`flask run --host=0.0.0.0`

you can access the application on port 5000




