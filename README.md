<img src="https://github.com/fabilya/yacut/blob/master/yacut/static/img/logo.png?raw=true" align="right" height="60" />

# ShortURL - link shortening service
## Content:
- [About the Project](#about-the-project)
- [Key Features](#key-features-of-the-service)
  - [API project](#project-api)
- [Technologies](#technologies-used)
- [Installation instructions](#installation-instructions)
- [Authors](#author-of-the-project)

### About the Project:

<b>ShortURL project</b> — is a tool that allows you to shorten long URLs into shorter, more manageable versions. When you enter a long link into a link shortening service, it generates a unique short URL for it, which can then be used in place of the original long URL.

### Key features of the service:

- generation of short links and their connection with the original long links,
- redirection to the original address when accessing short links.

### Project API

<details><summary>Examples of API requests</summary>

- Generating a short link: 
    ```SQL
  POST /api/id/
    {
      'url': 'string',
      'custom_id': 'string'
    }
    ```

- Getting the original link using the specified short identifier:
    ```SQL
    GET /api/id/{short_id}/
    ```
</details>


### Technologies used:

- `Python 3.9`
- `Flask 2.0.2`
- `SQLAlchemy 1.4.29`
- `REST API`
- `Jinja2 3.0.3`



### Installation instructions
* Clone the repository and go to it on the command line:
```GitBash
git clone git@github.com:fabilya/yacut.git
cd yacut
```

* Create a virtual environment:
```Bash
python -m venv venv
```
* Activate virtual environment:
<details><summary>Linux/macOS</summary>

```Bash
source venv/bin/activate
```
</details>
<details><summary>Windows</summary>

```Bash
source venv/scripts/activate
```
</details>

* Install dependencies from the requirements.txt file:
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```

* An example of an .env file that should be created in the root folder:
```dotenv
FLASK_APP=<project name>
FLASK_ENV=<development>
DATABASE_URI=<sqlite:///db.sqlite3>
SECRET_KEY=<SECRET_KEY>
```

* Creating a database and applying migration:
```Bash
flask db init
flask db migrate -m "db commit"
flask db upgrade
```

* Launching the application:
```Bash
flask run
```

### Author of the project:
[Fabiyanskiy Ilya](https://github.com/fabilya)


