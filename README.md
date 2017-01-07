﻿# Maps4All [![Circle CI](https://circleci.com/gh/hack4impact/maps4all.svg?style=svg)](https://circleci.com/gh/hack4impact/maps4all)  [![Code Climate](https://codeclimate.com/github/hack4impact/maps4all/badges/gpa.svg)](https://codeclimate.com/github/hack4impact/maps4all) [![Test Coverage](https://codeclimate.com/github/hack4impact/maps4all/badges/coverage.svg)](https://codeclimate.com/github/hack4impact/maps4all/coverage) [![Issue Count](https://codeclimate.com/github/hack4impact/maps4all/badges/issue_count.svg)](https://codeclimate.com/github/hack4impact/maps4all)

## Team Members

- Elizabeth Hamp
- Natasha Narang
- Arman Tokanov
- Veronica Wharton
- Daniel Zhang
- Annie Meng
- Stephanie Shi
- Sanjay Subramanian
- Ben Sandler
- Brandon Obas
- Kyle Rosenbluth
- Rani Iyer

## Synopsis

A Flask application template with the boilerplate code already done for you.

## What's included?

* Blueprints
* User and permissions management
* Flask-SQLAlchemy for databases
* Flask-WTF for forms
* Flask-Assets for asset management and SCSS compilation
* Flask-Mail for sending emails
* Automatic SSL + gzip compression

## Setting up

##### Clone the repo

```
$ git clone https://github.com/hack4impact/maps4all.git
$ cd maps4all
```

##### Initialize a virtualenv

```
$ pip install virtualenv
$ virtualenv env
$ source env/bin/activate
```
(If you're on a mac) Make sure xcode tools are installed
```
$ xcode-select --install
```

##### Install the dependencies

```
$ pip install -r requirements/common.txt
$ pip install -r requirements/dev.txt
```

##### Other dependencies for running locally

You need to install [Foreman](https://ddollar.github.io/foreman/) and [Redis](http://redis.io/). Chances are, these commands will work:

```
$ gem install foreman
```

Mac (using [homebrew](http://brew.sh/)):

```
$ brew install redis
```

Linux:

```
$ sudo apt-get install redis-server
```

##### Create the database

```
$ python manage.py recreate_db
```

##### Other setup (e.g. creating roles in database)

```
$ python manage.py setup_dev
```

##### [Optional] Add fake data to the database

```
$ python manage.py add_fake_data
```

## Running the app

```
$ source env/bin/activate
$ foreman start -f Local
```

## Project Structure


```
├── Procfile
├── README.md
├── app
│   ├── __init__.py
│   ├── account
│   │   ├── __init__.py
│   │   ├── forms.py
│   │   └── views.py
│   ├── admin
│   │   ├── __init__.py
│   │   ├── forms.py
│   │   └── views.py
│   ├── assets
│   │   ├── scripts
│   │   │   ├── app.js
│   │   │   └── vendor
│   │   │       ├── jquery.min.js
│   │   │       ├── semantic.min.js
│   │   │       └── tablesort.min.js
│   │   └── styles
│   │       ├── app.scss
│   │       └── vendor
│   │           └── semantic.min.css
│   ├── assets.py
│   ├── decorators.py
│   ├── email.py
│   ├── main
│   │   ├── __init__.py
│   │   ├── errors.py
│   │   ├── forms.py
│   │   └── views.py
│   ├── models.py
│   ├── static
│   │   ├── fonts
│   │   │   └── vendor
│   │   ├── images
│   │   └── styles
│   │       └── app.css
│   ├── templates
│   │   ├── account
│   │   │   ├── email
│   │   │   ├── login.html
│   │   │   ├── manage.html
│   │   │   ├── register.html
│   │   │   ├── reset_password.html
│   │   │   └── unconfirmed.html
│   │   ├── admin
│   │   │   ├── index.html
│   │   │   ├── manage_user.html
│   │   │   ├── new_user.html
│   │   │   └── registered_users.html
│   │   ├── errors
│   │   ├── layouts
│   │   │   └── base.html
│   │   ├── macros
│   │   │   ├── form_macros.html
│   │   │   └── nav_macros.html
│   │   ├── main
│   │   │   └── index.html
│   │   └── partials
│   │       ├── _flashes.html
│   │       └── _head.html
│   └── utils.py
├── config.py
├── manage.py
├── requirements
│   ├── common.txt
│   └── dev.txt
└── tests
    ├── test_basics.py
    └── test_user_model.py
```

## License
[MIT License](LICENSE.md)
