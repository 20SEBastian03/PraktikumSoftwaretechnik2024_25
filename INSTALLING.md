# 1. Dependencies

Python<br>
PIP<br>
PostgreSQL<br>

pipenv<br>
psycopg2<br>
Pillow<br><br>

# 2. Installation (Windows 11)

## 2.1 Install Dependencies

Install:<br>
&nbsp;&nbsp;&nbsp;&nbsp;python<br>
&nbsp;&nbsp;&nbsp;&nbsp;pip<br>
&nbsp;&nbsp;&nbsp;&nbsp;django<br>

## 2.2 Prerequisites

A PostgresSQL Database should be used instead of the Django-default SQLite Database,<br> 
we have to create a Postgres Database accessible by django.<br>
To do this, just open a Terminal anywhere and follow the next steps.<br>
By default, for this App you can use this commands to create the Postgres Database:<br>

**2.2.1** Create the database with the default psql superuser<br>
  `psql -U postgres db`<br> --> after hitting Enter, the command prompt should change and show `db=#` before the cursor<br>

**2.2.2** Create the User "django_user" and give it all necessary privileges for the DB.<br>
Please copy and paste the following commands behind `db=#` to your terminal, one after one:<br>
  `CREATE USER django_user WITH PASSWORD 'IchLiebeGA;'`<br>
  `GRANT USAGE ON SCHEMA public TO django_user;`<br>
  `GRANT CREATE ON SCHEMA public TO django_user;`<br>
  `GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO django_user;`<br>
  `GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA public TO django_user;`<br>
  `GRANT ALL PRIVILEGES ON ALL FUNCTIONS IN SCHEMA public TO django_user;`<br>

## 2.3 Install the Project Files

There are multiple ways to get the Projectfiles from our GitHub Repository.

Here are 2 examples:<br>

&nbsp;&nbsp;&nbsp;&nbsp;a) Please open your terminal at the place where you want to install the projekt files.<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Clone the repo:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`git clone https://github.com/totomate22/SEBackend`<br>

&nbsp;&nbsp;&nbsp;&nbsp;**OR**

&nbsp;&nbsp;&nbsp;&nbsp;b) Download it as a .ZIP from https://github.com/totomate22/SEBackend.<br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Afterwards extract the archive to the desired location on your PC.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Then please open a Terminal at the folder you extracted the .ZIP to and go on to the next step.

If you followed the steps before, you should now have a directory with the project files.

## 2.4 Create a Python Virtual Environment

Inside SEBackend there should be a Folder called DigiDish.<br>
Please open this Folder in a Terminal (or `cd` into it, if your terminal session from the steps before is still active).

**Inside** Digi Dish:<br>
&nbsp;&nbsp;&nbsp;&nbsp;Install pipenv for simply creating a Virtual Environment:<br>
&nbsp;&nbsp;&nbsp;&nbsp;`pip install pipenv`

&nbsp;&nbsp;&nbsp;&nbsp;Install the project dependencies in the Virtual Environment with the following command:<br>
&nbsp;&nbsp;&nbsp;&nbsp;`pipenv install django psycopg2 Pillow`<br><br>


# 3 Getting started

### Important!<br>
To run the project, 
it is required to have the Virtual Environment with the Dependencies installed ***active***<br>

Please open a Terminal **inside** Digi Dish Folder or (`cd` into it)
and activate the Virtual Environment with the following command<br> `pipenv shell`<br>

### With the Virtual Envrionment **active**<br>

&nbsp;&nbsp;&nbsp;&nbsp;Create your Admin Login Credentials:<br>
&nbsp;&nbsp;&nbsp;&nbsp;`python manage.py createsuperuser`

&nbsp;&nbsp;&nbsp;&nbsp;Migrate the Database:<br>
&nbsp;&nbsp;&nbsp;&nbsp;`python manage.py migrate`

&nbsp;&nbsp;&nbsp;&nbsp;Run the server:<br>
&nbsp;&nbsp;&nbsp;&nbsp;`python manage.py runserver`