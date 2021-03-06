
PLEASE USE https://github.com/Leo-g/Flask-Scaffold, latest changes and patches will be applied there

Flask-Skeleton allows you to quickly build a Skeleton CRUD application  in python 3.4 with Flask, FLask-SQLAlchemy, marshmallow and PostgreSQL.

Please ensure PostgreSQL is installed with the development libraries. Steps are available [here](http://techarena51.com/index.php/flask-sqlalchemy-postgresql-tutorial/)

For Complete Documentation with screenshots and troubleshooting please see the [wiki](https://github.com/Leo-g/Flask-Skeleton/wiki)

![](https://travis-ci.org/Leo-g/Flask-Skeleton.svg?branch=master)
###Installation Steps
####Step 1:Clone the project to your application folder.

    git clone git@github.com:Leo-g/Flask-Skeleton.git YourAppFolderName

####Step 2: Activate the virtual environment and install the requirements.
 
    cd YourAppFolderName
    virtualenv -p /usr/bin/python3.4 venv-3.4
    source venv-3.4/bin/activate
    pip install -r requirements.txt 

#### Step 3 : Update the config file with your Database Username, Database Password, Database Name and Database Hostname

    vim config.py

#### Step 4 : Run migrations 
   
    python db.py db init
    python db.py db migrate
    python db.py db upgrade
   
####  Step 5 : Start the server.
    python run.py

Crud operations are performed on a user resource.

**You should be able to see the App at  http://localhost:5000/users**

###Create a Scaffold
    python scaffold.py posts
    python db.py db migrate
    python db.py db upgrade
    python run.py

**You should be able to see the App at  http://localhost:5000/posts**

The above command will create a posts module in the app directory along with relevant templates in the templates folder. For complete details on Scaffold see https://github.com/Leo-g/Flask-Skeleton/wiki/Scaffolding

To run tests

      python tests.py
