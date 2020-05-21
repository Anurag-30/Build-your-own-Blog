# Hosting A Sample Web Application Using Flask Framework

To run locally(on centos) do the following steps:<br />

`sudo yum install python3` to install python3 <br />
`sudo yum install python3-pip` to install pip <br />
`cd Build-your-own-Blog/` <br />
`python3 -m venv flaskblog/venv` create a virtual environment <br />
`source flaskblog/venv/bin/activate` activating virtual environment <br />
`pip install -r requirements.txt` Installing dependencies and packages <br />

## Generate a secretkey:

open python interpreter by using pytho3 command <br />

`import secrets` <br />
`secrets.token_hex(16)` <br />

This will be your secret key which will be used by the application.<br />

## Creating Environment Variables: <br />

open ~/.bash_profile file and add the following variables: <br />

`export EMAIL_USER="Your Email"` <br />
`export EMAIL_PASS="Password for your email"` <br />
`export SECRET_KEY="Your Secret Key"` <br />
`export SQLALCHEMY_DATABASE_URI="sqlite:///site.db"` <br />

The EMAIL_USER and EMAIL_PASS are not mandatory but the forgot password featute won't be working without them

`source ~/.bash_profile`

now we are all set to run the application using:<br />
`export FLASK_APP=run.py`<br />
`flask run --host=0.0.0.0`<br />

you can access the application on port 5000 <br />






